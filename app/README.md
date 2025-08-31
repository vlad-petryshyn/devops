helm upgrade kanban-backend ./app -n kanban --install --values kanban-backend.yaml
helm template kanban-backend ./app -n kanban --values kanban-backend.yaml

helm upgrade kanban-frontend ./app -n kanban --install --values kanban-frontend.yaml

helm test kanban-frontend --namespace kanban