# Marvelin.AI - Asistente Financiero con Llama3
<img src="https://raw.githubusercontent.com/holasoymalva/malvelin/refs/heads/main/ui/src/assets/logo.png" alt="computer" width="60">

## Descripción
Marvelin.AI es un asistente financiero inteligente impulsado por Llama3, diseñado para proporcionar asesoramiento financiero personalizado a través de una interfaz web y Facebook Messenger. Este proyecto utiliza tecnologías de vanguardia en procesamiento de lenguaje natural para ofrecer respuestas precisas y útiles a consultas financieras.

## Características
- Interfaz web interactiva construida con Streamlit
- Integración con Facebook Messenger para consultas en tiempo real
- API REST para una fácil integración con otras plataformas
- Basado en el modelo de lenguaje Llama3 para respuestas precisas y contextuales
- Enfoque en asesoramiento financiero personalizado

## Requisitos del Sistema
- Python 3.8+
- Llama3
- Streamlit
- FastAPI
- Facebook Messenger API
- Otras dependencias (ver `requirements.txt`)

## Instalación

1. Clonar el repositorio:
   ```
   git clone https://github.com/tu-usuario/marvelin-ai.git
   cd marvelin-ai
   ```

2. Crear y activar un entorno virtual:
   ```
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   ```

3. Instalar las dependencias:
   ```
   pip install -r requirements.txt
   ```

4. Configurar las variables de entorno:
   Crea un archivo `.env` en el directorio raíz y añade las siguientes variables:
   ```
   FACEBOOK_PAGE_ACCESS_TOKEN=tu_token_de_acceso
   FACEBOOK_VERIFY_TOKEN=tu_token_de_verificacion
   LLAMA3_MODEL_PATH=ruta/al/modelo/llama3
   ```

## Uso

### Interfaz Web (Streamlit)
1. Ejecutar la aplicación Streamlit:
   ```
   streamlit run app.py
   ```
2. Abrir un navegador y visitar `http://localhost:8501`

### API REST
1. Iniciar el servidor FastAPI:
   ```
   uvicorn api:app --reload
   ```
2. La API estará disponible en `http://localhost:8000`
3. Documentación de la API disponible en `http://localhost:8000/docs`

### Integración con Facebook Messenger
1. Configurar un webhook en Facebook Developers para tu aplicación
2. Utilizar la URL de tu servidor (o un servicio como ngrok para desarrollo local) como endpoint del webhook
3. Verificar que la aplicación responde correctamente a los mensajes de Facebook

## Estructura del Proyecto
```
marvelin-ai/
├── app.py              # Aplicación Streamlit
├── api.py              # API REST con FastAPI
├── llama_model.py      # Wrapper para el modelo Llama3
├── messenger_handler.py # Manejo de mensajes de Facebook
├── utils.py            # Funciones de utilidad
├── requirements.txt    # Dependencias del proyecto
├── .env                # Variables de entorno (no incluir en el repositorio)
└── README.md           # Este archivo
```

## Contribuir
Las contribuciones son bienvenidas. Por favor, abre un issue para discutir cambios mayores antes de hacer un pull request.

## Licencia
[MIT License](https://opensource.org/licenses/MIT)

## Contacto
Para preguntas o soporte, por favor contacta a [hey@holasoymalva.com](mailto:hey@holasoymalva.com).
