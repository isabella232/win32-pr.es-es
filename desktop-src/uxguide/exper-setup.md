---
title: Configurar
description: A los usuarios no les gusta instalar software, por lo que las experiencias de configuración modernas deben ser sencillas, eficaces y sin problemas.
ms.assetid: ed0265a6-4c39-4a1f-9493-e316a6519df7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 905411c5ae08d2112943088d514ab300abb19ec2b8081158ebdfd896fc2c61ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119818359"
---
# <a name="setup"></a>Configurar

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

A los usuarios no les gusta instalar software, por lo que las experiencias de configuración modernas deben ser sencillas, eficaces y sin problemas.

El programa de instalación suele hacer referencia a la experiencia de instalar e configurar inicialmente un programa. Sin embargo, el programa de instalación también puede hacer referencia a todo el ciclo de vida de la instalación, incluida la instalación inicial, las actualizaciones incrementales de programas (como actualizaciones de versiones o Service Pack), la reparación y desinstalación.

La mayoría de los usuarios consideran que la configuración es un problema necesario, para realizarse lo antes posible. El punto de instalar el programa es usarlo, no tomar decisiones importantes sobre la configuración y el uso, o, peor aún, dedicar mucho tiempo a responder a preguntas personales usadas con fines de registro o marketing.

![Captura de pantalla que muestra un cuadro de diálogo de configuración con cuatro opciones.](images/exper-setup-image1.png)

Una experiencia de configuración simplificada.

La experiencia de configuración combinada con el primer uso del programa se conoce como la primera experiencia. El programa debe proporcionar una primera experiencia simplificada para los usuarios. Cada pregunta o paso que no es necesario o se puede posponer les retrasa el uso del programa. Los programas de instalación demasiado complejos son relicos de una edad diferente.

**Nota:** Las instrucciones relacionadas con la [primera experiencia](exper-first-exper.md) con un programa y los asistentes se presentan en [artículos](win-wizards.md) independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Aunque todos los programas Windows Microsoft necesitan algún tipo de programa de instalación, puede elegir dónde colocar la configuración del programa:

-   Configurar
-   Primer uso del programa
-   Opciones de programa centralizadas
-   En el contexto del uso de la característica

**Configuración**

Presente la configuración en la configuración si:

-   La configuración correcta es necesaria para usar el programa y se aplica a todos los usuarios.
-   El uso de la configuración predeterminada no es aceptable, ya sea porque no hay ningún valor predeterminado seguro, es probable que los usuarios elijan una configuración que no sea la predeterminada o que la configuración predeterminada requiera el consentimiento del usuario.
-   Los usuarios deben, pero no es probable que lo sean, cambiar la configuración importante después de la configuración.

**Primer uso del programa**

Presente la configuración en el primer uso del programa si:

-   La configuración correcta es necesaria para usar el programa y se aplica a usuarios individuales.
-   El uso de la configuración predeterminada no es aceptable, ya sea porque no hay ningún valor predeterminado seguro, es probable que los usuarios elijan una configuración que no sea la predeterminada o que la configuración predeterminada requiera el consentimiento del usuario.
-   Pero no es probable que los usuarios cambien la configuración importante mediante las opciones del programa.
-   La configuración personaliza una experiencia básica, o una que es fundamental para la identificación personal de un usuario con el programa.

Para esta configuración, es probable que los usuarios realicen mejores opciones en el contexto del programa que dentro de la configuración.

**Opciones de programa centralizadas**

Presente la configuración en el cuadro de diálogo [de opciones del programa](win-property-win.md) si se aplican todas las condiciones siguientes:

-   Hay configuraciones predeterminadas que funcionan bien para la mayoría de los usuarios.
-   Hay muchas configuraciones y se aplican entre características y tareas.
-   Es más probable que los usuarios encuentren la configuración en una ubicación centralizada.

**En el contexto del uso de la característica**

Presente la configuración en el contexto pertinente si se aplican todas las condiciones siguientes:

-   Hay configuraciones predeterminadas que funcionan bien para la mayoría de los usuarios.
-   Hay un pequeño número de configuraciones independientes para una característica específica.
-   Es más probable que los usuarios encuentren la configuración con la característica asociada que una ubicación centralizada.
-   Hay un lugar obvio en la interfaz de usuario (UI) para acceder a la configuración.

Mediante una atención cuidadosa a la ubicación de las opciones de configuración, puede reducir la carga de los usuarios durante su primera experiencia con el programa.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="design-a-lightweight-setup"></a>Diseño de una configuración ligera

Bienvenido, siguiente, siguiente, siguiente, siguiente, instalar, finalizar, enhorabuena. ¿Le parece familiar esta experiencia de configuración? Históricamente, los programas de instalación han adoptado este tipo de diseño ineficaz: una larga secuencia de pantallas que invita a los usuarios a una secuencia de clics sin sentido solo para atravesarla.

Si los usuarios describen la configuración del programa con palabras como rápidas y sencillas, son insociados al pralizar la experiencia. Prefiere usar el programa en lugar de configurarlo.

**Revise el diseño de la configuración para ver preguntas no esenciales, opciones, páginas y rutas de acceso, y no tenga problemas para eliminarlos.** Realice investigaciones de usuario para averiguar qué opciones necesitan realmente los usuarios y asegúrese de que no hacen clic sin sentido en el botón Siguiente en todas las páginas. Aplazar cualquier opción o pregunta que se aborde mejor en el contexto del programa en ejecución.

Muchos programas de instalación ofrecen páginas estándar no porque sean necesarias o útiles, sino porque son estándar. Por ejemplo, las páginas de bienvenida, las páginas de resumen y las páginas de enhorabuena suelen simplemente agregar clics. En su lugar, el programa de instalación solo debe agregar páginas si son necesarias para completar la tarea de instalación. Para obtener instrucciones sobre los tipos de páginas de configuración y cómo evaluarlas, consulte [Tipos de página](#page-types) más adelante en este artículo.

![captura de pantalla de la primera página de configuración de la declaración ](images/exper-setup-image2.png)

En este ejemplo, el programa de instalación elimina la página principal tradicional y pasa directamente a la empresa.

Aunque podría ser necesario ofrecer diferentes ramas de configuración (una experiencia rápida y típica y una experiencia personalizada más controlable), asegúrese de que tiene suficientes opciones personalizadas para garantizar la complejidad adicional. No agregue ramas a menos que tenga que hacerlo. Algunas opciones no importantes de una rama personalizada sugieren la necesidad de reorganizar el diseño de la instalación.

Otra razón para simplificar la configuración es que los usuarios sin experiencia a veces sobreanalizan las opciones, temiendo que una elección incorrecta pueda ser irreversible o destructiva. Obligar a los usuarios a tomar decisiones sobre cosas que no les importan o que no entienden pueden hacer que se sientan cómodos, cómodos e incluso frustrados. No es una buena primera impresión. Es mejor hacerlo rápidamente, sentirse cómodo y seguro a medida que exploran las características del programa y tomar mejores decisiones sobre las opciones de características en ese momento. Para obtener más instrucciones, consulte [Streamlining setup (Configuración de streamlining)](#streamlining-setup) más adelante en este artículo.

Procure que su experiencia de configuración sea [lo más sencilla posible, pero no más sencilla.](/previous-versions//dn742474(v=vs.85)) Los programas dirigidos a usuarios muy técnicos pueden necesitar una configuración compleja. Por ejemplo, el equipo de Microsoft SQL Server ha detectado que los administradores de bases de datos prefieren conservar el control sobre muchas opciones de configuración, como las ubicaciones de archivo. Además, SQL Server es una aplicación empresarial de gran tamaño, con una serie de componentes que difieren ampliamente en propósito y funcionalidad. Por lo tanto, aunque queremos que todo sea sencillo, la configuración debe reflejar la complejidad del producto y las expectativas y necesidades de sus usuarios.

Aun así, estos programas de instalación complejos deben ser la excepción, no la regla. La mayoría Windows programas deben procurar iniciar el proceso de instalación con un solo paso sencillo.

### <a name="setup-phases"></a>Fases de configuración

Los programas de instalación bien diseñados permiten a los usuarios realizar otras actividades durante la tarea lenta de descargar y copiar archivos. Para ejecutar desatendido, los programas de instalación están diseñados para tener cuatro fases independientes:

-   **Fase de decisión.** Los usuarios indican cómo quieren que el programa esté instalado y configurado.
-   **Fase de descarga.** Para los programas descargados de Internet. Si el programa tiene varias aplicaciones o versiones, los usuarios indican qué descargar durante la fase de decisión.
-   **Fase de instalación.** El programa de instalación copia los archivos y realiza los cambios de configuración adecuados.
-   **Fase de finalización.** Se abordan los detalles restantes, los pasos o los problemas.

Dado que la fase de instalación puede tardar mucho tiempo, esta fase debe diseñarse para que se ejecute hasta su finalización sin intervención del usuario. Esto significa que todas las preguntas deben realizarse durante la fase de decisión y los problemas que surjan se deben poner en cola y tratarse en la fase de finalización. **Si la fase de instalación tarda más de un minuto en completarse, suponga que los usuarios harán otra cosa durante las fases de descarga e instalación.**

**Incorrecto:**

![captura de pantalla de € ¿Instalar informes automáticos? diálogo ](images/exper-setup-image3.png)

En este ejemplo, el programa de instalación interrumpe el progreso para hacer una pregunta que se debería haber hecho durante la fase de decisión.

### <a name="present-helpful-progress"></a>Presentar progreso útil

Si los usuarios esperan pacientemente a través de la fase de instalación de la experiencia de instalación, quizás viendo una barra de progreso hasta su finalización aparente, solo para ver el restablecimiento de la barra de progreso y volver a empezar, hay una sensación real de desasociación. El progreso notificado era engañoso y, en última instancia, sin sentido.

Una variación en este escenario complicado es la instalación "brinksmanship": los usuarios ven un alcance de progreso, por ejemplo, el 99 % completo, pero se ven obligados a esperar una cantidad de tiempo desproporcionada antes de llegar finalmente al 100 % completo. Por lo tanto, en términos de lo que es más importante para el usuario, una promesa implícita sobre la cantidad de tiempo de espera, la notificación del 99 % de completado es falsa.

Durante las fases de descarga e instalación, los usuarios suelen tener dos cosas que quieren saber: si esperan o hacen otra cosa, y la configuración se va a realizar pronto. Aunque hay suficientes variables en el proceso de configuración para evitar que proporcione información de progreso perfectamente precisa, los comentarios sobre el progreso deben ser lo suficientemente precisos como para responder a estas dos preguntas y establecer las expectativas adecuadas. Además de una barra de progreso, puede incluir una breve instrucción sobre el tiempo total esperado para el proceso.

![captura de pantalla del cuadro de diálogo que muestra el progreso de la instalación ](images/exper-setup-image4.png)

En este ejemplo, la página de progreso incluye una breve declaración general sobre cuánto tiempo podría tardar la instalación.

Los programas de buena instalación usan barras de progreso de forma eficaz para proporcionar a los usuarios información útil sobre el progreso del programa de instalación. Para obtener más instrucciones, vea [Barras de progreso](progress-bars.md).

### <a name="design-for-all-setup-scenarios"></a>Diseño para todos los escenarios de configuración

Los programas de instalación moderna deben estar diseñados para controlar diversos escenarios de instalación:

-   El usuario del programa lo instala desde un disco o recurso compartido de archivos de red.
-   El usuario del programa lo descarga desde la Web.
-   Un fabricante de equipos originales (OEM) incluye el programa en el equipo de la fábrica.
-   Un profesional de IT está instalando el programa en muchos equipos de una organización.
-   Alguien que no sea el usuario está instalando el programa (por ejemplo, un elemento primario en nombre de un secundario o un compañero de trabajo que usa el mismo equipo que otro compañero de trabajo).

En estos escenarios, no debe suponer que los usuarios siempre instalan el programa por sí mismos (lo que hace que las opciones sobre las preferencias personales sean inapropiadas), vaya a supervisar el proceso de forma estrecha (lo que hace que la configuración desatendida sea importante) o incluso quiere una interfaz gráfica de usuario para la tarea.

### <a name="dont-forget-the-uninstall-experience"></a>No olvide la experiencia de desinstalación

Para completar el ciclo de vida de instalación de software, los usuarios deben poder quitar el software que no desean o ya no necesitan. Esto es especialmente importante si no instalaron el programa por sí mismos (por ejemplo, si se cargó previamente en el equipo).

### <a name="handle-technical-support-strategically"></a>Control del soporte técnico estratégicamente

La instalación del programa es la única tarea que todos los usuarios deben completar correctamente. Si los usuarios no pueden instalar el programa, debe proporcionarles soporte técnico costoso o ya no son los usuarios.

Diseñe el programa de instalación para proporcionar al equipo de soporte técnico las características e información que necesitan para ayudar a los usuarios a instalarse correctamente. Normalmente, estos detalles no deben exponerse a los usuarios, pero deben ser fácilmente accesibles cuando sea necesario.

**Incorrecto:**

![captura de pantalla de la etiqueta que muestra el nombre del servidor com ](images/exper-setup-image5.png)

En este ejemplo, la barra de progreso muestra detalles significativos solo para el soporte técnico.

Mantenga la experiencia normal del usuario sencilla: no la abarrote con información que solo tenga valor para el soporte técnico. En su lugar, registre la información de soporte técnico en un archivo de registro de instalación. Y, lo que es más importante, ayudar a los usuarios a evitar la necesidad de soporte técnico con mensajes de error claros y concisos que explican bien los problemas y proporcionan soluciones prácticas. Proporcione vínculos a artículos de Ayuda cuando sea necesario. Considere la posibilidad de proporcionar una opción de reparación al programa de instalación para reparar archivos o configuraciones que faltan o dañados.

**Si solo hace tres cosas...**

1.  1. Haga que la configuración sea lo más sencilla y ligera posible. Recuerde que los usuarios no disfruten de la configuración, ya que la sufren. Mire detenidamente cada pregunta, opción, página y ruta de acceso, y recorte todo lo que no es esencial para completar la configuración.
2.  2. Diseño para todos los escenarios de instalación, incluidas las instalaciones desatendidas, las instalaciones con scripts y la desinstalación. Para instalaciones desatendidas eficaces, asegúrese de que hay una separación limpia entre las fases de instalación.
3.  3. Diseñe el programa de instalación para que los usuarios puedan resolver los problemas de configuración por sí mismos, pero también registren la información necesaria para el soporte técnico por si fuera necesario. Tenga en cuenta que la configuración es la única tarea que todos los usuarios deben completar correctamente.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Aplique las directrices del asistente estándar para los programas de instalación basados en asistentes.** Use estas directrices para determinar un buen diseño de página, una navegación eficaz, etiquetas de control buenas, el uso de instrucciones principales y el uso de ayuda.
-   **Permitir que los usuarios reinicien el programa de instalación donde lo dejaron si requiere una gran cantidad de entrada del usuario o tarda mucho tiempo en completarse.** Si los usuarios reinician el programa después de cerrarlo antes de la finalización, restaure la entrada de usuario anterior y reinicie donde se detuvo la instalación.
-   **No muestre las ventanas de configuración maximizadas.** Al mostrar una ventana de configuración maximizada, se supone que los usuarios prestarán a la configuración su atención individida, lo que es poco probable. En su lugar, elija un tamaño adecuado para que el contenido mantenga una apariencia sencilla.

### <a name="windows-integration"></a>Windows integración

-   **Asigne al archivo de instalación el nombre "Setup.exe".** "Install.exe" es una alternativa aceptable. Esto permite que Windows (y los usuarios) reconozcan el archivo como un programa de instalación.
    -   **Excepción:** Para los programas descargados de Internet, ayude a los usuarios a administrar y organizar su carpeta Descargas incluyendo el nombre del programa en el nombre del archivo de instalación. Por ejemplo, SetupVisualStudioExpress2008.exe.
-   **Copie los archivos de programa en las ubicaciones del sistema de archivos adecuadas.** Esto permite a los usuarios y Windows buscar y organizar mejor los archivos. Para obtener más información, vea el Windows instrucciones de uso del espacio [de nombres del sistema de archivos](../fileio/naming-a-file.md#namespaces).

### <a name="user-account-control"></a>Control de cuentas de usuario

-   **Firme digitalmente el archivo ejecutable de instalación.** Los ejecutables firmados tienen muchas ventajas, incluido el uso de una interfaz de usuario de elevación de control de cuentas de usuario más específica. Para obtener información sobre cómo firmar archivos, vea [Introducción a la firma de código.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   **Si una configuración puede requerir elevación, eleve lo más tarde posible.** Muestre la interfaz de usuario de elevación solo después de que el usuario se haya confirmado en una opción que requiere elevación. Normalmente, la interfaz de usuario de elevación aparece durante la fase de instalación, no la fase de decisión. Sin embargo, si una configuración siempre requiere elevación, eleve en su punto de entrada.
-   **Requerir siempre elevación para la desinstalación.** Esto evita que el malware desinstale software crítico sin que los usuarios lo sepan.
-   **Una vez elevado, permanezca con privilegios elevados hasta que ya no sean necesarios.** Los usuarios no deben tener que elevar varias veces para completar la instalación de un programa.
-   **Si se requieren privilegios especiales para la instalación, compruebe las credenciales del usuario e informe de cualquier problema en la primera o segunda página.** No permita que los usuarios realicen mucho trabajo solo para averiguar que no tienen las credenciales adecuadas para completar la instalación.
-   **Requerir los privilegios mínimos posibles.** Por ejemplo, los administradores son reacios a instalar software que requiere credenciales de administrador de dominio.

Para obtener más instrucciones, consulte [Control de cuentas de usuario.](winenv-uac.md)

### <a name="restarting-windows"></a>Reiniciar Windows

-   **Evite reiniciar Windows.** La mayoría de los programas deben instalarse sin reiniciar Windows. La razón principal por la que las instalaciones o actualizaciones del programa requieren un reinicio del sistema es que algunos de los archivos implicados están siendo usados actualmente por un programa en ejecución. En este caso, una alternativa mejor es hacer que los usuarios conozcan la situación, permitir que los usuarios cierren estos programas y reintentar la acción. Para obtener más información sobre cómo evitar reinicios, vea [Restart Manager](../rstmgr/restart-manager-portal.md).
-   **Si el programa de instalación debe reiniciar Windows:**
    -   **Use un solo reinicio.** Retrase el reinicio requerido por los requisitos previos hasta que el programa y sus actualizaciones estén completamente instalados.
    -   **Permitir que los usuarios determinen cuándo ocurre.** No reinicie el Windows automáticamente, ya que los usuarios pueden perder el trabajo. Asegúrese de que los usuarios tengan claro que tienen una opción.

        **Incorrecto:**

        ![captura de pantalla del cuadro de diálogo con reinicio y cancelación ](images/exper-setup-image6.png)

        En este ejemplo, los usuarios no parecen tener la opción de cuándo reiniciar Windows.

    -   **Si el usuario decide no reiniciar Windows inmediatamente, presente los comentarios finales como correcto, no como un error.** Aunque técnicamente la instalación no se completa hasta el reinicio, se ha realizado correctamente desde el punto de vista del usuario.

### <a name="streamlining-setup"></a>Configuración de la secuenciación

-   **Siempre que sea práctico, inicie el proceso de instalación con un solo paso.** Por ejemplo, en lugar de agregar una página independiente en el programa de instalación para los términos de licencia, puede proporcionar un vínculo a ellos en su lugar. Si vincula a los términos:
    -   Frasee el botón de confirmación como "Aceptar e instalar" para requerir consentimiento explícito para aceptar los términos de licencia.
    -   Asegúrese de que el vínculo del contrato de licencia no se puede dividir vinculando a un archivo local a la instalación en lugar de a una página web.
    -   Proporcione la capacidad de imprimir el contrato de licencia desde su ventana de presentación.
-   **Elimine las opciones y preguntas innecesarias.**
    -   Posponer las opciones más adecuadas para el primer uso del programa o la característica.

        ![captura de pantalla del cuadro de diálogo con la opción de configuración personalizada ](images/exper-setup-image7.png)

        En este ejemplo, Reproductor de Windows Media opciones de privacidad por usuario en el primer uso del programa.

    -   No pregunte a los usuarios sobre el estado del sistema. Detecte esta información automáticamente en su lugar y pida a los usuarios que comprueben solo si hay una razón para cambiar.
    -   No haga preguntas sobre detalles no importantes. Por ejemplo, para los Windows típicos, es seguro suponer que debe copiar archivos de programa en la carpeta Archivos de programa.

        **Incorrecto:**

        ![captura de pantalla del cuadro de diálogo con ubicación de instalación ](images/exper-setup-image8.png)

        En este ejemplo, el programa de instalación debe simplificarse mediante la eliminación de la solicitud de entrada de ubicación de archivo. Dado el tamaño del programa, a la mayoría de los usuarios no les importa y simplemente haga clic en Siguiente.

    -   No pida permiso para hacer lo que no debería hacer de todos modos. Por ejemplo, la mayoría de los programas no deben incluir una opción para colocar el icono de programa en el escritorio.
    -   No confirme la cancelación del programa de instalación. Si los usuarios hacen clic en Cancelar durante la instalación, suponga que la cancelación fue intencionada y cierre el programa sin confirmación. Si lo hace, se corre el riesgo de perder mucho tiempo o esfuerzo, permita a los usuarios reiniciar el programa de instalación y retomar el lugar donde lo dejaron.

-   **Optimice para la instalación desatendida.**
    -   Presente todas las opciones y preguntas durante la fase de decisión.
    -   En las fases de descarga e instalación, retrase la intervención del usuario en los problemas detectados hasta el final de la fase. Al hacerlo, los usuarios pueden dejar la instalación desatendida hasta que vuelvan a su comodidad.
-   **Elimine las páginas innecesarias.** Si la mayoría de los usuarios siempre hace clic en Siguiente en una página, considere la posibilidad de deshacerse de la página. Para obtener instrucciones sobre cómo eliminar determinados tipos de páginas, vea [Tipos de página](#page-types).
-   **Elimine el texto innecesario.**
    -   Quite el texto redundante de las instrucciones y etiquetas.
    -   No explique los conceptos básicos Windows uso, como:
        -   Cómo interactuar con controles (ejemplos: Para empezar, haga clic en Siguiente; Para obtener más opciones, haga clic en Opciones; Para obtener más información, haga clic en Ayuda).
        -   Cómo funcionan los asistentes (por ejemplo: si desea revisar o cambiar cualquier configuración, haga clic en Atrás).
        -   Cómo funciona la instalación (ejemplo: este programa copiará los archivos de programa en el disco duro...).
-   **Elimine los esfuerzos innecesarios.**
    -   Proporcione buenos valores predeterminados:
        -   Por lo general, seleccione la respuesta más segura y privada para que sea la predeterminada.
        -   Si la seguridad y la privacidad no son factores, seleccione la respuesta más probable o adecuada.

            ![captura de pantalla del cuadro de diálogo con el nombre y la empresa mostrados ](images/exper-setup-image9.png)

            En este ejemplo, el nombre de usuario y la organización proporcionados de forma predeterminada se obtienen del Registro.

        -   Si se recomienda encarecidamente una opción, considere la posibilidad de seleccionarla de forma predeterminada o agregar "(recomendado)" a su etiqueta.

    -   Avanzar páginas automáticamente cuando una página no tiene ninguna entrada y la tarea se realiza correctamente, como con las páginas de descarga, instalación, progreso y actualizaciones. Una vez que se haya realizado el paso, permanezca en estas páginas solo para mostrar problemas.
    -   Cuando sea práctico, inicie el programa automáticamente cuando finalice la instalación, en lugar de mostrar una página Enhorabuena o Finalización. Cuando la instalación se ejecuta de forma interactiva, suponga que el usuario está instalando el programa para ejecutarlo inmediatamente, por lo que la ejecución del programa es el mejor comentario para mostrar que la instalación se ha completado. La ejecución automática del programa no es práctica cuando el programa de instalación instala más de un programa (por ejemplo, un conjunto de aplicaciones que consta de muchos programas), cuando el programa de instalación no se ejecuta de forma interactiva o cuando el proceso de instalación no se completa después de la instalación.

### <a name="page-types"></a>Tipos de página

**Páginas de bienvenida y Tareas iniciales de bienvenida**

-   **Elimine las páginas de bienvenida.** Aunque es excelente sentirse bienvenido, los usuarios normalmente simplemente hacen clic en Siguiente sin leer. Y dado que los usuarios normalmente omiten estas páginas sin leer, el texto hace poco más que lo obvio, por diseño.

    **Incorrecto:**

    ![captura de pantalla de la pantalla de bienvenida con next y cancel ](images/exper-setup-image10.png)

    En este ejemplo, no hay nada que hacer para el usuario, pero haga clic en Siguiente.

-   **Use una página Tareas iniciales solo si debe informar a los usuarios sobre los requisitos previos para la instalación.** Estos requisitos previos incluyen la instalación del software o el hardware necesarios, la realización de los cambios y actualizaciones de configuración del sistema necesarios, la realización de una copia de seguridad del sistema para protegerse frente a la pérdida de datos u la obtención de la información necesaria que es probable que el usuario ya no tenga.
-   **Siempre que sea práctico, proporcione la capacidad de cumplir los requisitos previos directamente desde el programa de instalación.** Los usuarios deben tener que realizar los pasos manualmente solo si no hay ninguna alternativa.
-   Si no se usa una página Tareas iniciales página principal o una página de inicio de sesión, incluya el nombre y la descripción del programa en la que sea la primera página **del programa de instalación.** Puede usar el lenguaje de bienvenida como texto introductorio, siempre y cuando el propósito de la página sea claro.

**Páginas de términos de licencia**

-   **Escriba los términos de licencia con texto claro y conciso.** Use lenguaje sin formato. Evite "legales".
-   **Presente mediante un formato fácil de leer y examinar.** No use fragmentos largos de texto en mayúsculas.

    **Incorrecto:**

    ![captura de pantalla de los términos de licencia en mayúsculas ](images/exper-setup-image11.png)

    En este ejemplo, el texto en mayúsculas y el tamaño de fuente grande dificultan la lectura de los términos, lo que obliga a los usuarios a desplazarse más de lo necesario.

-   **Requerir consentimiento explícito para aceptar los términos de licencia.** La aceptación de la licencia nunca debe seleccionarse de forma predeterminada. Si se usan botones de radio para indicar la aceptación, deje las opciones desactivadas de forma predeterminada y exija a los usuarios que acepten los términos antes de habilitar el botón Siguiente.

    ![captura de pantalla del cuadro de diálogo con el botón siguiente atenuado ](images/exper-setup-image12.png)

    En este ejemplo, el botón Siguiente está deshabilitado hasta que los usuarios han aceptado explícitamente los términos de licencia.

-   **No es necesario que los usuarios se desplacen a la parte inferior del texto de los términos de licencia antes de habilitar el botón Siguiente.** Esto impone una carga innecesaria a los usuarios para comprender por qué el botón Siguiente está deshabilitado.
-   **Proporcione un comando Imprimir,** ya sea con un botón de comando o un menú contextual. Presente los términos en un formato optimizado para la impresión.

**Páginas de registro de productos**

-   **Requerir que los usuarios se registren solo si deben para poder usar el programa.** Explique claramente por qué los usuarios deben registrarse.
-   **Proporcione un registro opcional solo si hay una ventaja clara para** el usuario, como notificar a los usuarios las actualizaciones de productos. Deje esta opción desactivada de forma predeterminada.
-   **Permitir que los usuarios se registren más adelante.** Proporcione un máximo de tres recordatorios y permita a los usuarios descartar los recordatorios con un solo clic.

**Páginas de ámbito (típicas, personalizadas o mínimas)**

-   **Prefiere eliminar esta página.** Suponga que la mayoría de los usuarios quieren la experiencia de configuración típica (y diseñe esa experiencia para que funcione bien para la mayoría de los usuarios).
-   Si debe incluir una página de ámbito:
    -   **Explicar las diferencias entre las opciones en términos de funcionalidad y espacio en disco.** Los usuarios confían en la claridad de la información de la página de ámbito para asegurarse de que hacen la elección correcta.
    -   **Asegúrese de que las opciones personalizadas solo son necesarias para un pequeño porcentaje de usuarios, mientras que la mayoría de los usuarios pueden omitirlas de forma segura.** Si no es así, las opciones deben estar en la ruta de configuración típica.
    -   **Si los usuarios eligen opciones personalizadas, seleccione las opciones de instalación típicas de forma predeterminada.** Los usuarios consideran la instalación típica como la línea de base y desean personalizar agregando o quitando opciones de esa línea base.
-   Si debe usar una opción de instalación personalizada, considere la posibilidad de usar el tamaño y la ubicación relativos de los botones para guiar a la mayoría de los usuarios **a la instalación típica.**

    ![captura de pantalla del cuadro de diálogo con el botón de instalación grande ](images/exper-setup-image13.png)

    En este ejemplo, el diseño de páginas refuerza visualmente el hecho de que la mayoría de los usuarios deben optar por la instalación típica.

**Páginas de entrada**

-   **Reduzca el número de opciones de configuración haciendo lo correcto de forma predeterminada.** Para obtener información sobre cómo eliminar opciones, consulte [Streamlining setup ( Configuración de streamlining).](#streamlining-setup)
-   **Proporcione valores predeterminados aceptables siempre que sea posible.** Elija valores predeterminados que sean seguros y privados, y que sean aceptables para la mayoría de los usuarios sin cambios.
-   **A menos que el programa tenga requisitos inusuales, esfuércse por tener una sola página de preguntas y opciones.** Pero si el programa requiere varias páginas de preguntas y opciones, debe mostrarlas en el flujo de páginas del asistente principal. No intente reducir técnicamente el número de páginas colocando opciones en cuadros de diálogo o usando pestañas.
-   ![captura de pantalla del cuadro de diálogo de configuración con cuatro opciones ](images/exper-setup-image14.png)
-   En este ejemplo, las opciones se limitan a una sola página.
-   **Valide la entrada lo antes posible:**
    -   Prohíba los caracteres no válidos en la entrada.
    -   Use [globos para](ctrl-balloons.md) notificar problemas con cuadros de texto no válidos.
    -   Valide los campos relacionados de una página cuando los usuarios hacen clic en Siguiente.
    -   Valide los campos relacionados entre las páginas de entrada en cuanto se puedan detectar problemas.
-   **Dé a todas las rutas de acceso de archivo editables un botón Examinar.** Permitir a los usuarios especificar rutas de acceso de red.
-   **Para la página de entrada final, etiquete el botón de confirmación Instalar, no Siguiente.** Cuando se inicia la instalación, los usuarios no deben desapreorse. Antes del punto de confirmación, asegúrese de que los usuarios pueden cambiar fácilmente cualquier configuración.

**Inicio de páginas de instalación**

-   **Elimine esta página si no tiene otro propósito que resumir las opciones anteriores y comenzar la instalación.** Si las páginas de entrada están claras y son pocas en número, no debería ser necesario resumirlas. En su lugar, la página de entrada final debe tener el botón Instalar, que conduce directamente a la página de progreso.
-   **Para instalaciones complejas dirigidas a profesionales de TI, proporcione una página Instalación con una lista completa de los cambios que realizará el programa de instalación.** Muchos profesionales de IT tienen un control estricto de la administración de cambios, por lo que necesitan saber el efecto que tendrá la instalación del programa en detalle.

**Páginas de progreso**

-   **Proporcione siempre una página de progreso,** incluso si el programa se instala rápidamente. Proporcione una página de progreso independiente [para la fase de descarga](#setup-phases) si la hay. Deshabilite los botones Atrás (o Anterior) y Siguiente mientras la configuración está en curso, pero deje el botón Cancelar habilitado y con capacidad de respuesta.

    ![captura de pantalla del cuadro de diálogo con la barra de progreso ](images/exper-setup-image15.png)

    Página de progreso típica.

-   **Use una sola barra de progreso determinada.** Siga las [instrucciones de la barra de progreso determinadas,](progress-bars.md)entre las que se incluyen:
    -   Indique claramente la finalización. No permita que una barra de progreso vaya al 100 % a menos que se haya completado la operación.
    -   No reinicie el progreso. Una barra de progreso pierde su valor si se reinicia (quizás porque se completa un paso de la operación) porque los usuarios no tienen forma de saber cuándo se completará la operación. En su lugar, haga que todos los pasos de la operación compartan una parte del progreso y que la barra de progreso finalice una vez.
-   **Proporcione una descripción concisa del paso actual encima de la barra de progreso.** Para instalaciones rápidas, este texto no es necesario; la barra de progreso por sí sola es suficiente. Para las instalaciones que requieren un minuto o más, el texto puede ser útil para los usuarios que asistan a la instalación.
    -   **Use fragmentos de oración, normalmente empezando por un verbo y terminando con puntos suspensivos.** Ejemplos: Copiar archivos..., Instalar los componentes necesarios...
    -   **Coloque el texto encima de la barra, no debajo.**

        **Incorrecto:**

        ![captura de pantalla del texto que se muestra en la barra de progreso ](images/exper-setup-image16.png)

        En este ejemplo, el texto explicativo debe aparecer encima de la barra de progreso.

    -   **Evite abarrote la página de progreso con detalles innecesarios.** Esta página no es para [soporte](#handle-technical-support-strategically)técnico, por lo que no es necesario mostrar GUID de registro ni archivos específicos copiados.

        **Incorrecto:**

        ![captura de pantalla del GUID que se muestra en la barra de progreso ](images/exper-setup-image17.png)

        En este ejemplo, los detalles técnicos, como los GUID, no tienen sentido para los usuarios.

**Páginas de error**

-   **Si se produce un error en el programa de instalación con un problema significativo, muestre una página de error que explique los problemas junto con los pasos prácticos para resolverlos.** Muestra la página con un icono de error. No use un cuadro de diálogo para este propósito.

    ![captura de pantalla de la página de error y el icono ](images/exper-setup-image18.png)

    En este ejemplo, el error de instalación se explica en una página de error, junto con algunos pasos para resolver el problema.

-   **Si la instalación se completa con un problema recuperable menor, presente el problema como una tarea adicional en lugar de un error.** Use un lenguaje positivo, orientado al éxito y alentador, no términos como error, error o problema. No use un icono de error.

**Páginas de finalización/enhorabuena**

-   **Al instalar un único programa de forma interactiva, inicie el programa (y cierre el Asistente para la instalación) para indicar que la instalación se ha realizado correctamente, en lugar de mostrar una página de finalización. Excepciones:**
    -   Las configuraciones que se ejecutan desde la línea de comandos no deben iniciar programas.
    -   Las actualizaciones automáticas (por ejemplo, Windows update) no deben iniciar programas.
    -   La instalación de directivas de grupo no debe iniciar programas.
    -   Cualquier escenario de configuración profesional de TI (porque no se instala para su propio uso).
-   **Si la instalación tiene pasos de seguimiento después de la instalación, enuméguelos en una página Finalización.** Pero para justificar una página Finalización, asegúrese de que es probable que los usuarios realicen los pasos y que los pasos realmente deben indicarse (es decir, no son obvios).

    **Incorrecto:**

    ![captura de pantalla de la página en la que se muestra que se ha completado la instalación ](images/exper-setup-image19.png)

    En este ejemplo, una página Finalización innecesaria indica lo obvio. Windows La actualización se ejecuta automáticamente, por lo que no hay ninguna razón para que los usuarios la ejecuten manualmente.

-   **Al instalar un conjunto de programas, muestre una página Finalización para indicar que se ha completado correctamente y los pasos de seguimiento que puedan ser necesarios.**

    ![captura de pantalla de la página final de configuración del conjunto de aplicaciones de office ](images/exper-setup-image20.png)

    En este ejemplo, el programa de instalación ha instalado varios programas, por lo que no tiene sentido iniciar un programa determinado automáticamente. Una página Finalización es más adecuada.

### <a name="leaving-users-in-control"></a>Dejar a los usuarios bajo control

-   **No recopila información personal, como la que se usa con fines de marketing.** El programa de instalación no es una oportunidad para insertar su propia agenda, realizar ventas cruzadas de otras ofertas de programas ni realizar investigaciones de mercado. puede dañar la relación de confianza con los usuarios de esta manera.
-   **No fuerce a los usuarios a no instalar características opcionales.** En su lugar, [permita que opten por](glossary.md) participar. Por ejemplo, los usuarios deben elegir explícitamente instalar un Windows Desktop Desktop Desktop.
-   **Permitir a los usuarios agregar o quitar características opcionales mediante el programa de instalación después de la instalación inicial.** Los usuarios pueden realizar esta tarea mediante el elemento **Desinstalar o cambiar un** panel de control de programa.
-   **En el caso de las iniciativas de mejora de la experiencia del cliente, explique qué datos se transmiten, cómo se usan y cuánto tiempo se mantienen.** Use un vínculo a un tema de Ayuda de declaración de privacidad para este propósito.
-   **Evite el uso de sonido,** ya que muchos escenarios de instalación son desatendidos y porque el sonido puede distraer innecesariamente incluso durante las instalaciones atendidas.

### <a name="security"></a>Seguridad

-   **Para la instalación basada en Internet, proporcione las actualizaciones de seguridad automáticamente durante la instalación inicial.** Los usuarios no deben tener que actualizarse como un paso independiente.
-   **Evite recomendar que los usuarios desactiven los firewalls como requisito previo para instalar el programa.**
-   Si se debe desactivar un firewall, haga lo siguiente:
    -   **Limite la duración de esta condición al menor tiempo posible.**
    -   **Señalar explícitamente cuándo los usuarios pueden volver a activar el firewall.**

### <a name="uninstall"></a>Desinstalación

-   **La desinstalación debe quitar todos los seguimientos de un programa, incluidos los siguientes:**
    -   Archivos de programa, incluido el programa de instalación.
    -   menú Inicio entradas.
    -   Iconos de escritorio inicio rápido iconos (si los hay).
    -   La configuración del Registro.
    -   Asociaciones de archivo.
-   **La desinstalación debe dejar lo siguiente:**
    -   Archivos creados por el usuario, como archivos de documento.
    -   Bibliotecas de vínculos dinámicos compartidas almacenadas en la carpeta System.

### <a name="help-and-support"></a>Ayuda y soporte técnico

-   **Diseñe el programa de instalación para que no necesite ayuda; para ello, haga preguntas claras y autoexplicativas.** Reserve ayuda para preguntas avanzadas que realmente se benefician de una explicación adicional.
-   **No use archivos Léame.** Estos archivos están obsoletos y los usuarios no los leen de todos modos. En su lugar, proporcione contenido en línea si es necesario.
-   **Vínculo a temas de Ayuda adecuados o solución de problemas de contenido de mensajes de error de instalación.** Asegúrese de que el contenido de la Ayuda proporciona una ruta de acceso clara para resolver el problema. Para obtener más información, vea [Mensajes de error.](mess-error.md)
-   **Cree archivos de registro para capturar información útil para el soporte técnico.** No abarrote la interfaz de usuario de instalación con detalles relacionados con el soporte técnico que no tienen sentido para la mayoría de los usuarios. Use los archivos de registro para este propósito en su lugar.

### <a name="text"></a>Texto

-   **Sea conciso.** Los asistentes para la instalación suelen sobreexplicar características y opciones, mediante bloques de texto que son difíciles de examinar rápidamente. **Excepciones:**
    -   Deletrear todos los acrónimos. La configuración suele ser la primera experiencia de los usuarios con el programa, por lo que no suponga que entienden la jerga, como los acrónimos.
    -   Explicar terminología y conceptos desconocidos, preferiblemente en su lugar, pero usando temas de Ayuda si es necesario.
-   **Prefiere un tono descriptivo y profesional; evite un tono muy técnico.**

**Incorrecto:**

Restrinja la instalación por usuario.

**Correcto:**

Instalar solo para mí.

-   No use ahora en etiquetas de botón de comando porque se puede conceder lamediacia del comando.
    -   **Excepción:** Cuando sea necesario, use ahora para diferenciar los comandos que inician una tarea de los comandos que realizan una tarea inmediatamente.

![captura de pantalla del botón de descarga ](images/exper-setup-image21.png)

En este ejemplo, al hacer clic en el botón de comando se va a una ventana o página que permite a los usuarios descargar.

![captura de pantalla del botón Descargar ahora ](images/exper-setup-image22.png)

En este ejemplo, al hacer clic en el botón de comando se realiza la descarga inmediatamente.

Solo un comando de un flujo de tareas debe etiquetarse con ahora. Por ejemplo, un comando **Descargar ahora** nunca debe ir seguido de otro **comando Descargar** ahora.

-   Use los términos de licencia, no el contrato de licencia, el contrato de licencia, el contrato de licencia del usuario final o el CLUF.

Para obtener más instrucciones, [vea Estilo y tono.](text-style-tone.md)

## <a name="documentation"></a>Documentación

-   Como verbo, configurar es dos palabras; como adjetivo o sustantivo, el programa de instalación es una palabra.
-   El programa de instalación está en mayúsculas y no tiene guiones.
-   Use instalar para hacer referencia a la adición de hardware o software a un sistema informático.
-   No use install como un sustantivo. Use la instalación en su lugar.
-   Use reiniciar, no reiniciar. Indique que es el equipo, no un programa, el que se está reiniciando.

 

 