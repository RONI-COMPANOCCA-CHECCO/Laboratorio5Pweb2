<div align="center">
<table>
    <theader>
        <tr>
            <td><img src="https://github.com/rescobedoq/pw2/blob/main/epis.png?raw=true" alt="EPIS" style="width:50%; height:auto"/></td>
            <th>
                <span style="font-weight:bold;">UNIVERSIDAD NACIONAL DE SAN AGUSTIN</span><br />
                <span style="font-weight:bold;">FACULTAD DE INGENIERÍA DE PRODUCCIÓN Y SERVICIOS</span><br />
                <span style="font-weight:bold;">DEPARTAMENTO ACADÉMICO DE INGENIERÍA DE SISTEMAS E INFORMÁTICA</span><br />
                <span style="font-weight:bold;">ESCUELA PROFESIONAL DE INGENIERÍA DE SISTEMAS</span>
            </th>
            <td><img src="https://github.com/rescobedoq/pw2/blob/main/abet.png?raw=true" alt="ABET" style="width:50%; height:auto"/></td>
        </tr>
    </theader>
    <tbody>
        <tr><td colspan="3"><span style="font-weight:bold;">Formato</span>: Guía de Práctica de Laboratorio</td></tr>
        <tr><td><span style="font-weight:bold;">Aprobación</span>:  2023/02/01</td><td><span style="font-weight:bold;">Código</span>: GUIA-PRLD-001</td><td><span style="font-weight:bold;">Página</span>: 1</td></tr>
    </tbody>
</table>
</div>

<div align="center">
<span style="font-weight:bold;">GUÍA DE LABORATORIO</span><br />
</div>


<table>
<theader>
<tr><th colspan="6">INFORMACIÓN BÁSICA</th></tr>
</theader>
<tbody>
<tr><td>ASIGNATURA:</td><td colspan="5">Programación Web 2</td></tr>
<tr><td>TÍTULO DE LA PRÁCTICA:</td><td colspan="5">Django</td></tr>
<tr>
<td>NÚMERO DE PRÁCTICA:</td><td>05</td><td>AÑO LECTIVO:</td><td>2023 A</td><td>NRO. SEMESTRE:</td><td>III</td>
</tr>
<tr>
<td>FECHA INICIO::</td><td>30-May-2023</td><td>FECHA FIN:</td><td>03-Jun-2023</td><td>DURACIÓN:</td><td>04 horas</td>
</tr>
<tr><td colspan="6">RECURSOS:
    <ul>
        <li>https://www.w3schools.com/python/python_reference.asp</li>
        <li>https://docs.python.org/3/tutorial/</li>
        <li>https://developer.mozilla.org/es/docs/Learn/Server-side/Django/Models</li>
        <li>https://tutorial.djangogirls.org/es/django_models/</li>
        <li>https://pear.php.net/manual/en/standards.php</li>
        <li>https://docs.djangoproject.com/en/4.0/</li>
        <li>https://www.youtube.com/watch?v=M4NIs4BM1dk</li>
        <li>https://pypi.org/</li>
        <li>https://pip.pypa.io/en/latest/user_guide/</li>
        <li>https://packaging.python.org/en/latest/tutorials/installing-packages/</li>
    </ul>
</td>
</<tr>
<tr><td colspan="6">DOCENTE:
<ul>
<li>Ing. Anibal Sardon</li>
</ul>
</td>
</<tr>
<tr><td colspan="6">ALUMNO:
<ul>
<li>Roni Companocca Checco</li>
</ul>
</td>
</<tr>
</tdbody>
</table>

# Django

[![License][license]][license-file]
[![Downloads][downloads]][releases]
[![Last Commit][last-commit]][releases]

[![Debian][Debian]][debian-site]
[![Git][Git]][git-site]
[![GitHub][GitHub]][github-site]
[![Vim][Vim]][vim-site]
[![Java][Java]][java-site]

#

## 1. Competencias del curso

- General: C.c. Dise ̃na responsablemente aplicaciones web, sus componentes o procesos para satisfacer necesidades dentro de restricciones realistas: econ ́omicas, medio ambientales, sociales, políticas,  ́eticas, de salud, de seguridad, manufacturación y sostenibilidad.

- Específica: C.m. Construye responsablemente soluciones con tecnolog ́ıa web siguiendo un proceso adecuado llevando a cabo las pruebas ajustada a los recursos disponibles del cliente.

- Específica: C.p. Aplica de forma flexible técnicas, métodos, principios, normas, estándares y herramientas del desarrollo web necesarias para la construcción de aplicaciones web e implementación de estos sistemas en una organización.

## 2. Resultado del estudiante

- RE. 2 La capacidad de aplicar diseño de ingeniería para producir soluciones a problemas y diseñar sistemas, componentes o procesos para satisfacer necesidades espec ́ıficas dentro de consideraciones realistas en los aspectos de salud pública, seguridad y bienestar; factores globales, culturales, sociales, econ ́omicos y ambientales.

- RE. 8 La capacidad de crear, seleccionar y utilizar t ́ecnicas, habilidades, recursos y herramientas modernas de ingeniería y tecnologías de la información, incluyendo la predicción y el modelamiento, con una comprensión de las limitaciones.

## 3. Equipos, materiales y temas

- Sistema Operativo (GNU/Linux de preferencia).
- GNU Vim.
- Python 3.
- Git.
- Cuenta en GitHub con el correo institucional.
- Entorno virtual.
- Django 4.

## 4. Directorio de trabajo

- Cree su directorio de trabajo.
- Luego, diríjase a este directorio, para clonar su repositorio y continuar sus practicas.

    ```sh
                 Listing 1: Creando directorio de trabajo
    $ mkdir -p $HOME/rescobedoq/
    ```

    ```sh
                 Listing 2: Dirij ́ıendonos al directorio de trabajo
    $ cd $HOME/rescobedoq/
    ```

    ```sh
                 Listing 3: Clonando repositorio GitHub
    $ git clone [URL_DE_SU_GITHUB_PRIVADO]
    ```

    ```sh
                 Listing 4: Creando directorio para laboratorio
    $ mkdir -p $HOME/rescobedoq/pw2-lab-23a/lab05/exercises/
    ```

- Siempre evalue utilizar el archivo .gitignore para no considerar algunos archivo innecesarios sobre todo para el repositorio GitHub.
- Pueden haber varios de estos archivos y estar ubicados estrat ́egicamente; por ejemplo sólo para un laboratorio en particular.

    ```sh
                 Listing 5: Creando .gitignore
    $ vim $HOME/rescobedoq/pw2-lab-23a/lab05/.gitignore
    ```

    ```sh
                 Listing 6: Ejemplo de .gitignore
    my_env/bin/*
    my_env/lib/*
    my_env/src/__pycache__/*
    *.pyc
    ```

- Estudie el archivo .gitignore del proyecto Library :
- https://github.com/mdn/django-locallibrary-tutorial/blob/main/.gitignore

## 5. Marco teórico

### 5.1. Django

- Django es un framework web Python con el cu ́al el desarrollo de sitios web son r ́apidos, seguros y sobre todo f ́aciles de mantener.
- Django se ocupa de gran parte de las molestias del desarrollo web, por lo que puede concentrarse en escribir su aplicación sin necesidad de reinventar la rueda.
- Es software libre, tiene una comunidad pr ́ospera y activa, excelente documentaci ́on y muchas opciones de soporte gratuito y de pago.

### 5.2. Crear un directorio para el entorno virtual de Django

- Para crear un ambiente elija en qu ́e directorio se va crear el entorno virtual.

    ```sh
                 Listing 7: Creando directorio para entorno virtual en Unix
    $ mkdir -p $HOME/rescobedoq/pw2-lab-23a/lab05/my_env
    ```

    ```sh
                 Listing 8: Creando directorio para entorno virtual
    $ mkdir -p $HOME/rescobedoq/pw2-lab-23a/lab05/my_env
    ```

### 5.3. Crear entorno virtual en un directorio

- En este directorio crear un entorno virtual ejecutando el siguiente comando:

    ```sh
                 Listing 9: Creando entorno virtual en GNU/Linux
    $ cd $HOME/rescobedoq/pw2-lab-23a/lab05/my_env
    $ virtualenv -p python3 .
    ```

    ```sh
                 Listing 10: Creando entorno virtual en MS Windows
    C:\>python -m venv c:\rescobedoq\pw2-lab-23a\lab05\my_env
    ```

    ```sh
                 Listing 11: Creando entorno virtual en MacOS
    $ python -m venv $HOME/rescobedoq/pw2-lab-23a/lab05/my_env
    ```

### 5.4. Activando entorno virtual

- En el directorio de trabajo active el entorno virtual ejecutando el script activate.
- Sea cual sea nuestro sistema operativo sabremos que el entorno virtual se ha activado porque su nombre aparece entre par ́entesis delante del promt.

    ```sh
                 Listing 12: Activando entorno virtual en GNU/Linux
    $ cd $HOME/rescobedoq/pw2-lab-23a/lab05/exercises/
    $ source ./../my_env/bin/activate
    (my_env) user@localhost:$
    ```

    ```sh
                 Listing 13: Activando entorno virtual en GNU/Linux
    C:\rescobedoq\pw2-lab-23a\lab05\my_env\scripts\activate.bat
    ```

    ```sh
                 Listing 14: Activando entorno virtual en GNU/Linux
    $ source $HOME/rescobedoq/pw2-lab-23a/lab05/my_env/bin/activate
    ```

### 5.5. Desactivando entorno virtual

- El comando para desactivar el entorno virtual es id ́entico para Windows, macOS y Linux:

    ```sh
                 Listing 15: Desactivando entorno virtual
    $ deactivate
    ```

### 5.6. Instalando Django dentro del entorno virtual

- Siempre hay que estar consientes de los paquetes de nuestro entorno virtual.

    ```sh
                 Listing 16: Mostrando paquetes instalados en el entorno virtual
    (my_env) user@localhost:$ pip list
    Package Version
    ---------- -------
    pip 22.0.4
    setuptools 62.1.0
    wheel 0.37.1
    ```

- Instalamos Django con pip:

    ```sh
                 Listing 17: Instando Django
    (my_env) user@localhost:$ pip install Django
    ```

- Volvemos a listar los paquetes instalados:

    ```sh
                 Listing 18: Mostrando Django instalado en el entorno virtual
    (my_env) user@localhost:$ pip list
    Package Version
    ---------- -------
    asgiref 3.5.2
    Django 4.0.5
    pip 22.0.4
    setuptools 62.1.0
    sqlparse 0.4.2
    wheel 0.37.1
    ```

## 6. Ejercicios

- Cree la aplicación Library paso a paso desde la siguiente url:
- https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Tutorial_local_library_website

## 7. Tarea

- Elabore un primer informe grupal de la aplicaci ́on que desarrollar ́a durante este semestre.
- Utilicen todas las recomendaciones dadas en la aplicaci ́on library.
- Acuerdos :
    • Los grupos pueden estar conformado por 1 a 4 integrantes.
    • S ́olo se presenta un informe grupal.
    • S ́olo se revisa un repositorio. (El  ́unico que est ́e en el informe grupal).
    • Todos los integrantes del grupo tienen una copia del laboratorio e informe en su repositorio privado.
    • Todos los integrantes deben pertenecer al mismo grupo de laboratorio.
    • El docente preguntar ́a en cualquier momento a un integrante sobre el proyecto, codigo fuente, avance.

## 8. Pregunta

- Por cada integrante del equipo, resalte un aprendizaje que adquiri ́o al momento de estudiar Django. No se reprima de ser detallista. Coloque su nombre entre parentesis para saber que es su aporte.

## 9. Entregables

- El informe debe tener un enlace al directorio específico del laboratorio en su repositorio GitHub privado donde esté todo el código fuente y otros que sean necesarios. Evitar la presencia de archivos: binarios, objetos, archivos temporales, cache, librerias, entornos virtuales. Si hay configuraciones particulares puede incluir archivos de especificación como: requirements.txt, o leeme.txt.
- No olvide que el profesor debe ser siempre colaborador a su repositorio (Usuario del profesor @rescobedoq).
- Para ser considerado con la calificaci ́on de m ́axima nota, el informe debe estar elab ́orado en LATEX
- Usted debe describir s ́olo los commits m ́as importantes que marcaron hitos en su trabajo, adjutando capturas de pantalla, del commit, del código fuente, de sus ejecuciones y pruebas.
- En el informe siempre se debe explicar las im ́agenes (c ́odigo fuente, capturas de pantalla, commits, ejecuciones, pruebas, etc.) con descripciones puntuales pero precisas.

## 10. Rúbricas

### 10.1. Rúbrica para entregable Informe

***Tabla 1: Rúbrica para tipo de Informe***
<a href="https://ibb.co/SyHdtdK"><img src="https://i.ibb.co/PjJ9c95/lab51.jpg" alt="lab51" border="0"></a>

### 10.2. Rúbrica para el contenido del Informe y demostración

- El alumno deberá marcar o dejar en blanco en las celdas de la columna Checklist, deacuerdo a si cumplió o no con el ítem correspondiente.
- Si un alumno supera la fecha de entrega, su calificación siempre será sobre la nota mínima aprobada, siempre y cuando cumpla con todos lo items.
- El alumno debe autocalificarse en la columna Estudiante de acuerdo a la tabla de calificación de niveles de desempeño:

***Tabla 2: Niveles de desempeño***
<a href="https://imgbb.com/"><img src="https://i.ibb.co/nPqkGT7/lab52.jpg" alt="lab52" border="0"></a>

***Tabla 3: Rúbrica para contenido del Informe y demostración***
<a href="https://ibb.co/X88Fkc3"><img src="https://i.ibb.co/vYYLv0Q/lab53.jpg" alt="lab53" border="0"></a>

## 11. Referencias

- https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Tutorial_local_library_website
- https://github.com/mdn/django-locallibrary-tutorial
- https://github.com/rescobedoq/pw2/tree/main/labs/lab05
- William S. Vincent. (2022). Django for Beginners: Build websites with Python. Django 4.0. leanpub.com. [URL]

#

[license]: https://img.shields.io/github/license/rescobedoq/pw2?label=rescobedoq
[license-file]: https://github.com/rescobedoq/pw2/blob/main/LICENSE

[downloads]: https://img.shields.io/github/downloads/rescobedoq/pw2/total?label=Downloads
[releases]: https://github.com/rescobedoq/pw2/releases/

[last-commit]: https://img.shields.io/github/last-commit/rescobedoq/pw2?label=Last%20Commit

[Debian]: https://img.shields.io/badge/Debian-D70A53?style=for-the-badge&logo=debian&logoColor=white
[debian-site]: https://www.debian.org/index.es.html

[Git]: https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white
[git-site]: https://git-scm.com/

[GitHub]: https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white
[github-site]: https://github.com/

[Vim]: https://img.shields.io/badge/VIM-%2311AB00.svg?style=for-the-badge&logo=vim&logoColor=white
[vim-site]: https://www.vim.org/

[Java]: https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=java&logoColor=white
[java-site]: https://docs.oracle.com/javase/tutorial/


[![Debian][Debian]][debian-site]
[![Git][Git]][git-site]
[![GitHub][GitHub]][github-site]
[![Vim][Vim]][vim-site]
[![Java][Java]][java-site]


[![License][license]][license-file]
[![Downloads][downloads]][releases]
[![Last Commit][last-commit]][releases]