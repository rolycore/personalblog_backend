# Personal Blog

## Descripción
Este es un proyecto de blog personal desarrollado utilizando Vue.js para el frontend y Django para el backend. La aplicación permite la creación, edición y visualización de posts y blogs, así como la autenticación de usuarios.

## Estructura del Proyecto

```
personalblog/
├── frontend/
│   ├── public/
│   ├── src/
│   ├── vue.config.js
│   ├── package.json
│   ├── README.md
│   └── ...
├── backend/
│   ├── personalblog/
│   ├── posts/
│   ├── manage.py
│   ├── requirements.txt
│   ├── README.md
│   └── ...
└── README.md
```

## Frontend

### Tecnologías Utilizadas
- Vue.js 3
- Vue Router
- Vuex
- Vuetify
- Axios

### Instalación y Configuración

1. Clona el repositorio:

```bash
git clone https://github.com/rolycore/personal-blog.git
cd personalblog/frontend
```

2. Instala las dependencias:

```bash
npm install
```

3. Configura Vuetify y las rutas en `src/main.js`:

```javascript
import { createApp } from 'vue'
import App from './App.vue'
import vuetify from './plugins/vuetify'
import { createRouter, createWebHistory } from 'vue-router'
import routes from './router/index'

const app = createApp(App)
const router = createRouter({
  history: createWebHistory(),
  routes,
})

app.use(vuetify)
app.use(router)
app.mount('#app')
```

4. Ejecuta el servidor de desarrollo:

```bash
npm run serve
```

El frontend estará disponible en `http://localhost:8080`.

### Estructura de Archivos

```
frontend/
├── public/
├── src/
│   ├── assets/
│   ├── components/
│   ├── plugins/
│   ├── router/
│   ├── store/
│   ├── views/
│   ├── App.vue
│   └── main.js
├── vue.config.js
├── package.json
└── README.md
```

## Backend

### Tecnologías Utilizadas
- Django
- Django REST Framework
- MySQL

### Instalación y Configuración

1. Clona el repositorio (si no lo has hecho ya):

```bash
git clone https://github.com/rolycore/personalblog_backend.git
cd personalblog/backend
```

2. Crea y activa un entorno virtual (opcional pero recomendado):

```bash
python -m venv env
source env/bin/activate  # En Windows usa `env\Scripts\activate`
```

3. Instala las dependencias:

```bash
pip install -r requirements.txt
```

4. Configura la base de datos en `personalblog/settings.py`:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'nombre_de_tu_base_de_datos',
        'USER': 'tu_usuario',
        'PASSWORD': 'tu_contraseña',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```

5. Realiza las migraciones:

```bash
python manage.py makemigrations
python manage.py migrate
```

6. Crea un superusuario para acceder al panel de administración:

```bash
python manage.py createsuperuser
```

7. Ejecuta el servidor de desarrollo:

```bash
python manage.py runserver
```

El backend estará disponible en `http://localhost:8000`.

### Estructura de Archivos

```
backend/
├── personalblog/
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── ...
├── posts/
│   ├── migrations/
│   ├── models.py
│   ├── serializers.py
│   ├── views.py
│   └── ...
├── manage.py
├── requirements.txt
└── README.md
```

## API Endpoints

### Autenticación

- `POST /api/auth/login/`: Iniciar sesión
- `POST /api/auth/register/`: Registrar un nuevo usuario

### Posts

- `GET /api/posts/`: Listar todos los posts
- `POST /api/posts/`: Crear un nuevo post
- `GET /api/posts/:id/`: Obtener detalles de un post específico
- `PUT /api/posts/:id/`: Actualizar un post
- `DELETE /api/posts/:id/`: Eliminar un post

### Blogs

- `GET /api/blogs/`: Listar todos los blogs
- `POST /api/blogs/`: Crear un nuevo blog
- `GET /api/blogs/:id/`: Obtener detalles de un blog específico
- `PUT /api/blogs/:id/`: Actualizar un blog
- `DELETE /api/blogs/:id/`: Eliminar un blog

## Licencia
Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

## Contacto

Para cualquier consulta o problema, puedes contactarme a través de [shalomsolutiontech@gmail.com](mailto:shalomsolutiontech@gmail.com).
