docker network create --driver overlay portainer_edge_agent_network && docker service create --name portainer_edge_agent --network portainer_edge_agent_network -e AGENT_CLUSTER_ADDR=tasks.portainer_edge_agent -e EDGE=1 -e EDGE_ID=af045757-bc27-4a4d-80f4-dcd8663df1c9 -e EDGE_KEY=aHR0cDovLzEwLjAuMi4xNTo3MjAyfDEwLjAuMi4xNTo4MDAwfDBmOjE1OmEyOjM3OjEzOjVhOjNkOjAyOjljOmM1OmIxOmIyOjZhOjQ0OmRjOmRmfDE -e CAP_HOST_MANAGEMENT=1 --mode global --constraint node.platform.os==windows --mount type=npipe,src=\\.\pipe\docker_engine,dst=\\.\pipe\docker_engine --mount type=bind,src=C:\ProgramData\docker\volumes,dst=C:\ProgramData\docker\volumes --mount type=volume,src=portainer_agent_data,dst=C:\data portainer/agent
