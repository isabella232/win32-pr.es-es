---
title: Configurar
description: Los usuarios no disfrutan de la instalación de software, por lo que las experiencias de instalación modernas deben ser sencillas, eficientes y sin problemas.
ms.assetid: ed0265a6-4c39-4a1f-9493-e316a6519df7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 4e5de6f15dd797dd1d1362d1b515122b78c770f4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104563772"
---
# <a name="setup"></a>Configurar

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Los usuarios no disfrutan de la instalación de software, por lo que las experiencias de instalación modernas deben ser sencillas, eficientes y sin problemas.

Normalmente, el programa de instalación hace referencia a la experiencia de instalación y configuración inicial de un programa. Sin embargo, el programa de instalación también puede hacer referencia a todo el ciclo de vida de la instalación, incluida la instalación inicial, las actualizaciones de programas incrementales (como actualizaciones de versión o Service Pack), la reparación y la desinstalación.

La mayoría de los usuarios tienen en cuenta la configuración como un mal necesario, para que se realice lo más rápido posible. El punto de instalar el programa es usarlo, no tomar decisiones de incontables sobre la configuración y el uso, o, peor aún, para dedicar mucho tiempo a responder a preguntas personales que se usan con fines de registro o marketing.

![Captura de pantalla que muestra un cuadro de diálogo de instalación con cuatro opciones.](images/exper-setup-image1.png)

Una experiencia de instalación simplificada.

La experiencia de instalación combinada con el primer uso del programa se conoce como la primera experiencia. El programa debe proporcionar una primera experiencia simplificada para los usuarios. Cada pregunta o paso que no es necesario o que se puede posponer les retrasa el uso del programa. Los programas de instalación demasiado complejos se relicsn de una antigüedad diferente.

**Nota:** Las instrucciones relacionadas con la [primera experiencia](exper-first-exper.md) con un programa y los [asistentes](win-wizards.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Aunque todos los programas de Microsoft Windows necesitan algún tipo de programa de instalación, tiene la opción de elegir dónde colocar la configuración del programa:

-   Configurar
-   Primer uso del programa
-   Opciones de programa centralizadas
-   En el contexto del uso de la característica

**Configuración**

Presente la configuración del programa de instalación si:

-   Los valores correctos son necesarios para usar el programa y se aplican a todos los usuarios.
-   El uso de la configuración predeterminada no es aceptable, ya sea porque no hay ningún valor predeterminado seguro, es probable que los usuarios elijan valores que no sean los predeterminados o que la configuración predeterminada requiera el consentimiento del usuario.
-   Los usuarios deberían, pero no es probable, cambiar la configuración importante después del programa de instalación.

**Primer uso del programa**

Presente la configuración del primer uso del programa si:

-   Los valores correctos son necesarios para usar el programa y se aplican a usuarios individuales.
-   El uso de la configuración predeterminada no es aceptable, ya sea porque no hay ningún valor predeterminado seguro, es probable que los usuarios elijan valores que no sean los predeterminados o que la configuración predeterminada requiera el consentimiento del usuario.
-   Los usuarios deben, pero no obstante, cambiar la configuración importante con las opciones del programa.
-   La configuración personaliza una experiencia principal o una que es fundamental para la identificación personal de un usuario con el programa.

Para este tipo de configuración, es probable que los usuarios realicen mejores elecciones en el contexto del programa que en la instalación.

**Opciones de programa centralizadas**

Presente la configuración del cuadro de [diálogo Opciones](win-property-win.md) del programa si se cumplen todas las condiciones siguientes:

-   Hay configuraciones predeterminadas que funcionan bien para la mayoría de los usuarios.
-   Hay muchas opciones de configuración y se aplican a través de las características y las tareas.
-   Es más probable que los usuarios esperen encontrar la configuración en una ubicación centralizada.

**En el contexto del uso de la característica**

Presente la configuración en el contexto correspondiente si se cumplen todas las condiciones siguientes:

-   Hay configuraciones predeterminadas que funcionan bien para la mayoría de los usuarios.
-   Hay un pequeño número de valores independientes para una característica específica.
-   Es más probable que los usuarios esperen encontrar la configuración con la característica asociada que una ubicación centralizada.
-   Hay un lugar obvio en la interfaz de usuario (UI) para tener acceso a la configuración.

Con especial atención a la selección de ubicación de los valores de configuración, puede reducir la carga de los usuarios durante su primera experiencia con el programa.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="design-a-lightweight-setup"></a>Diseñar una instalación ligera

Bienvenido, siguiente, siguiente, siguiente, siguiente, siguiente, instalar, finalizar, enhorabuena. ¿Está familiarizado con este programa de instalación? Históricamente, los programas de instalación han adoptado este tipo de diseño ineficaz: una larga secuencia de pantallas que invitan a los usuarios a una secuencia de clics sin tener en cuenta.

Si los usuarios describen la configuración del programa con palabras como rápidas y sencillas, seguramente elogiar la experiencia. En su lugar, sería mucho más usar el programa que configurarlo.

**Revise el diseño del programa de instalación en busca de preguntas, opciones, páginas y rutas de acceso no esenciales y Ruthless sobre cómo eliminarlas.** Realice una investigación de usuario para averiguar qué opciones realmente necesitan los usuarios y asegúrese de que no se mindlessly haciendo clic en el botón siguiente a través de todas las páginas. Postergue cualquier opción o pregunta que se resuelva mejor en el contexto del programa en ejecución.

Muchos programas de instalación ofrecen páginas estándar, no porque son necesarias o son útiles, pero porque son estándares. Por ejemplo, las páginas de bienvenida, las páginas de Resumen y las páginas de enhorabuena suelen agregar clics. En su lugar, el programa de instalación solo debe agregar páginas si son necesarias para completar la tarea de instalación. Para obtener instrucciones sobre los tipos de páginas de instalación y cómo evaluarlas, consulte [tipos de página](#page-types) más adelante en este artículo.

![captura de pantalla de la primera página de configuración de ProClarity ](images/exper-setup-image2.png)

En este ejemplo, el programa de instalación elimina la página de bienvenida tradicional y se hace avanzar a la empresa.

Aunque es posible que sea necesario ofrecer distintas ramas del programa de instalación (una experiencia rápida, típica y una experiencia más controlable y personalizada), asegúrese de que tiene suficientes opciones personalizadas para garantizar la complejidad adicional. No agregue ramas a menos que sea necesario. Algunas opciones poco importantes en una bifurcación personalizada sugieren la necesidad de reorganizar el diseño del programa de instalación.

Otro motivo para simplificar la configuración es que a veces los usuarios inestables sobreanalicen las opciones, Temendo que una elección equivocada podría ser irreversible o destructiva. Forzar a los usuarios a tomar decisiones acerca de las cosas que no entienden o que le interesan pueden hacer que se sientan ansiosos, incompetentes e incluso frustrantes. No es una buena impresión en primer lugar. Es mejor hacerlo rápidamente, sentirse cómodo y seguro a medida que exploran las características del programa y toman mejores decisiones sobre las opciones de características en ese momento. Para obtener más instrucciones, consulte [optimizar la configuración](#streamlining-setup) más adelante en este artículo.

Procure que la experiencia de instalación sea lo [más sencilla posible, pero no más sencilla](/previous-versions//dn742474(v=vs.85)). Los programas destinados a usuarios muy técnicos pueden necesitar una configuración compleja. Por ejemplo, el equipo de Microsoft SQL Server detectó que los administradores de bases de datos prefieren mantener el control sobre muchas opciones de configuración, como las ubicaciones de archivos. Además, SQL Server es una aplicación empresarial de gran tamaño, con una serie de componentes que difieren ampliamente en el propósito y la funcionalidad. Así que, aunque queremos simplificar las cosas, el programa de instalación debe reflejar la complejidad del producto y las expectativas y necesidades de sus usuarios.

Además, estos programas de instalación complejos deben ser la excepción, no la regla. La mayoría de los programas de Windows deben procurar iniciar el proceso de instalación con un solo paso sencillo.

### <a name="setup-phases"></a>Fases de configuración

Los programas de instalación bien diseñados permiten a los usuarios realizar otras actividades durante la tarea que consume mucho tiempo en descargar y copiar archivos. Para ejecutarse en modo desatendido, los programas de instalación están diseñados para tener cuatro fases independientes:

-   **La fase de decisión.** Los usuarios indican cómo quieren que el programa esté instalado y configurado.
-   **La fase de descarga.** Para programas descargados de Internet. Si el programa tiene varias aplicaciones o versiones, los usuarios indican lo que se debe descargar durante la fase de decisión.
-   **Fase de instalación.** El programa de instalación copia los archivos y realiza los cambios de configuración adecuados.
-   **La fase de finalización.** Se abordan los detalles, pasos o problemas restantes.

Dado que la fase de instalación puede tardar mucho tiempo, esta fase debe diseñarse para ejecutarse hasta su finalización sin intervención del usuario. Esto significa que todas las preguntas deben realizarse durante la fase de decisión y los problemas que surjan deben ponerse en cola y abordarse en la fase de finalización. **Si la fase de instalación tarda más de un minuto en completarse, supongamos que los usuarios realizarán otra acción durante las fases de descarga e instalación.**

**Incorrecto:**

![captura de pantalla de los informes automáticos de instalación diálogo ](images/exper-setup-image3.png)

En este ejemplo, el programa de instalación interrumpe el progreso para formular una pregunta que se debería haber solicitado durante la fase de decisión.

### <a name="present-helpful-progress"></a>Presente progreso útil

Si los usuarios esperan a través de la fase de instalación de la experiencia de instalación, es posible que vea una barra de progreso en cuanto a su finalización aparente, solo para ver el restablecimiento de la barra de progreso y volver a empezar, hay un sentido real en la bandeja. El progreso indicado era engañoso y, en última instancia, no tiene sentido.

Una variación de este escenario doloroso es la instalación "brinksmanship": los usuarios ven el progreso, por ejemplo, 99 por ciento completado, pero están obligados a esperar durante un período de tiempo desproporcionado antes de terminar hasta el 100 por ciento. Por lo tanto, en lo que respecta a lo que es más importante para el usuario, una promesa implícita sobre la cantidad de tiempo de espera, la demanda del 99% completado es engañosa.

Durante las fases de descarga e instalación, los usuarios suelen tener dos cosas que quieren saber: deben esperar o hacer otra cosa, y es la configuración que se va a realizar pronto. Aunque hay suficientes variables en el proceso de instalación para evitar que proporcione información de progreso perfectamente precisa, los comentarios de progreso deben ser suficientemente precisos para responder a estas dos preguntas y establecer las expectativas adecuadas. Además de una barra de progreso, puede incluir una breve instrucción sobre el tiempo total esperado para el proceso.

![captura de pantalla del cuadro de diálogo que muestra el progreso de la instalación ](images/exper-setup-image4.png)

En este ejemplo, la página de progreso incluye una breve instrucción general sobre la cantidad de tiempo que puede tardar la instalación.

Los programas de instalación correctos usan barras de progreso de manera eficaz para proporcionar a los usuarios información útil sobre el progreso del programa de instalación. Para obtener más instrucciones, vea [barras de progreso](progress-bars.md).

### <a name="design-for-all-setup-scenarios"></a>Diseño para todos los escenarios de instalación

Los programas de instalación modernos deben estar diseñados para controlar diversos escenarios de instalación:

-   El usuario del programa lo está instalando desde un disco o recurso compartido de archivos de red.
-   El usuario del programa lo descarga de la Web.
-   Un fabricante de equipos originales (OEM) incluye el programa en el equipo en el generador.
-   Un profesional de TI está instalando el programa en muchos equipos de una organización.
-   Alguien que no sea el usuario que está instalando el programa (por ejemplo, un elemento primario en nombre de un elemento secundario o un compañero de trabajo que está usando el mismo equipo que otro compañero de trabajo).

En estos casos, no debe preocuparse de que los usuarios siempre estén instalando el programa para ellos mismos (con las opciones de preferencias personales inadecuadas), con lo que se supervisará el proceso de forma minuciosa (es importante realizar una configuración desatendida) o incluso una interfaz gráfica de usuario para la tarea.

### <a name="dont-forget-the-uninstall-experience"></a>No olvide la experiencia de desinstalación.

Para completar el ciclo de vida de instalación del software, los usuarios deben poder quitar el software que no quieran o que ya no necesiten. Esto es especialmente importante si no instalaron el propio programa (por ejemplo, si estaba previamente cargado en el equipo).

### <a name="handle-technical-support-strategically"></a>Controle el soporte técnico estratégicamente

La instalación del programa es una tarea que todos los usuarios deben completar correctamente. Si los usuarios no pueden instalar el programa, debe proporcionarles un soporte técnico caro o que ya no sean los usuarios.

Diseñe el programa de instalación para proporcionar al equipo de soporte técnico las características y la información que necesitan para ayudar a los usuarios a instalar correctamente. Estos detalles no deberían estar expuestos normalmente a los usuarios, pero deben ser accesibles fácilmente cuando sea necesario.

**Incorrecto:**

![captura de pantalla de la etiqueta que muestra el nombre del servidor com ](images/exper-setup-image5.png)

En este ejemplo, la barra de progreso muestra detalles que solo son significativos para el soporte técnico.

Simplificar la experiencia de usuario normal: no se amontona con información que solo tiene valor para soporte técnico. En su lugar, registre la información de soporte técnico en un archivo de registro de instalación. Y lo que es más importante, ayudan a los usuarios a evitar la necesidad de soporte técnico con mensajes de error claros y concisos que expliquen los problemas bien y proporcionen soluciones prácticas. Proporcione vínculos a los artículos de ayuda cuando sea necesario. Considere la posibilidad de proporcionar una opción de reparación al programa de instalación para reparar la configuración o los archivos dañados o que faltan.

**Si solo hace tres cosas...**

1.  1. Haga que el programa de instalación sea lo más sencillo y ligero posible. Recuerde que los usuarios no disfrutan del programa de instalación, sino que lo hacen. Fíjese detenidamente en cada pregunta, opción, página y ruta de acceso, y recorte todo lo que no es esencial para completar la instalación.
2.  2. Diseño para todos los escenarios de instalación, incluidas las instalaciones desatendidas, las instalaciones con scripts y la desinstalación. En el caso de instalaciones desatendidas eficientes, asegúrese de que hay una separación limpia entre las fases de configuración.
3.  3. Diseñe el programa de instalación de modo que los usuarios puedan resolver los problemas de instalación por sí solos, pero también registren la información necesaria para el soporte técnico en caso de que sea necesario. Tenga en cuenta que el programa de instalación es la tarea que todos los usuarios deben completar correctamente.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Aplique las directrices del asistente estándar para los programas de instalación basados en asistente.** Siga estas instrucciones para determinar el diseño correcto de la página, la navegación eficaz, las etiquetas de control correctas, el uso de las instrucciones principales y el uso de la ayuda.
-   **Permita que los usuarios reinicien el programa de instalación en el que se dejaron si requieren mucha información del usuario o tardan mucho tiempo en completarse.** Si los usuarios reinician el programa después de cerrarlo antes de la finalización, restaure la entrada del usuario anterior y reinicie el lugar donde se detuvo la instalación.
-   **No mostrar las ventanas de configuración maximizadas.** Si se muestra una ventana de configuración maximizada, se supone que los usuarios darán su atención a la instalación, lo que es improbable. En su lugar, elija un tamaño adecuado para que el contenido tenga un aspecto sencillo.

### <a name="windows-integration"></a>Integración de Windows

-   **Asigne al archivo de instalación el nombre "Setup.exe".** "Install.exe" es una alternativa aceptable. Esto permite a Windows (y a los usuarios) reconocer el archivo como programa de instalación.
    -   **Excepción:** En el caso de los programas descargados de Internet, ayude a los usuarios a administrar y organizar su carpeta de descargas incluyendo el nombre del programa en el nombre del archivo de instalación. Por ejemplo, SetupVisualStudioExpress2008.exe.
-   **Copie los archivos de programa en las ubicaciones adecuadas del sistema de archivos.** Esto permite a los usuarios y a Windows buscar y organizar mejor los archivos. Para obtener más información, vea las [instrucciones de uso del espacio de nombres del sistema de archivos de Windows](../fileio/naming-a-file.md#namespaces).

### <a name="user-account-control"></a>Control de cuentas de usuario

-   **Firmar digitalmente el archivo ejecutable de instalación.** Los ejecutables firmados tienen muchas ventajas, como el uso de una interfaz de usuario de elevación de control de cuentas de usuario más específica. Para obtener información sobre la firma de archivos, vea [Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).
-   **Si una instalación puede requerir elevación, eleve lo más tarde posible.** Mostrar la interfaz de usuario de elevación solo después de que el usuario se haya confirmado en una opción que requiere elevación. Normalmente, la interfaz de usuario de elevación aparece durante la fase de instalación, no en la fase de decisión. Sin embargo, si una instalación requiere siempre elevación, eleve en su punto de entrada.
-   **Siempre se requiere la elevación para la desinstalación.** Al hacerlo, se impide que el malware desinstale software crítico sin que los usuarios lo sepan.
-   **Una vez elevado, Manténgase elevado hasta que ya no se necesiten privilegios elevados.** Los usuarios no deben tener que elevar varias veces para realizar la instalación de un programa.
-   **Si se requieren privilegios especiales para la instalación, compruebe las credenciales del usuario y notifique los problemas en la primera o en la segunda página.** No permita que los usuarios realicen mucho trabajo solo para encontrar que no tienen las credenciales correctas para completar la instalación.
-   **Requerir los privilegios mínimos posibles.** Por ejemplo, los administradores se ven resistentes para instalar software que requiere credenciales de administrador de dominio.

Para obtener más instrucciones, consulte [control de cuentas de usuario](winenv-uac.md).

### <a name="restarting-windows"></a>Reiniciar Windows

-   **Evite reiniciar Windows.** La mayoría de los programas deben instalarse sin reiniciar Windows. La razón principal por la que las instalaciones o actualizaciones de programas requieren un reinicio del sistema es que algunos de los archivos implicados están siendo utilizados actualmente por un programa en ejecución. En este caso, una alternativa mejor es que los usuarios conozcan la situación, permitan a los usuarios cerrar estos programas y vuelvan a intentar la acción. Para obtener más información acerca de cómo evitar los reinicios, vea [restart Manager](../rstmgr/restart-manager-portal.md).
-   **Si el programa de instalación debe reiniciar Windows:**
    -   **Use un único reinicio.** Retrasar el reinicio necesario para los requisitos previos hasta que el programa y sus actualizaciones se instalen por completo.
    -   **Permita que los usuarios determinen Cuándo se produce.** No reinicie Windows automáticamente, ya que los usuarios pueden perder el trabajo. Asegúrese de que está claro a los usuarios que tienen una opción.

        **Incorrecto:**

        ![captura de pantalla del cuadro de diálogo con reiniciar y cancelar ](images/exper-setup-image6.png)

        En este ejemplo, no parece que los usuarios tengan la opción de reiniciar Windows.

    -   **Si el usuario decide no reiniciar Windows inmediatamente, presente los comentarios finales como un éxito, no un error.** Aunque técnicamente la instalación no se completa hasta el reinicio, se realizó correctamente desde el punto de vista del usuario.

### <a name="streamlining-setup"></a>Optimizar la configuración

-   **Siempre que sea práctico, inicie el proceso de instalación con un solo paso.** Por ejemplo, en lugar de agregar una página independiente en el programa de instalación de los términos de licencia, puede proporcionar un vínculo a ellas en su lugar. Si vincula a los términos:
    -   Frase el botón confirmar como "aceptar e instalar" para requerir el consentimiento explícito para aceptar los términos de licencia.
    -   Asegúrese de que el vínculo del contrato de licencia no se puede romper vinculando a un archivo local del programa de instalación en lugar de a una página web.
    -   Proporcionar la capacidad de imprimir el contrato de licencia desde la ventana de visualización.
-   **Elimine las opciones y preguntas innecesarias.**
    -   Posponer opciones más adecuadas para el primer uso del programa o la característica.

        ![captura de pantalla del cuadro de diálogo con la opción de configuración personalizada ](images/exper-setup-image7.png)

        En este ejemplo, Windows Media Player presenta las opciones de privacidad por usuario en el primer uso del programa.

    -   No formule preguntas a los usuarios sobre el estado del sistema. En su lugar, detecte esta información automáticamente y solicite a los usuarios que solo la verifiquen si hay un motivo para cambiar.
    -   No formule preguntas sobre detalles no importantes. Por ejemplo, para los programas típicos de Windows es seguro suponer que debe copiar los archivos de programa en la carpeta archivos de programa.

        **Incorrecto:**

        ![captura de pantalla del cuadro de diálogo con ubicación de instalación ](images/exper-setup-image8.png)

        En este ejemplo, el programa de instalación se debe simplificar eliminando la solicitud de entrada de ubicación del archivo. Dado el tamaño del programa, la mayoría de los usuarios no tienen cuidado y simplemente haga clic en siguiente.

    -   No pida permiso para hacer lo que no debe hacer de todos modos. Por ejemplo, la mayoría de los programas no deben incluir una opción para colocar el icono de programa en el escritorio.
    -   No confirme la cancelación del programa de instalación. Si los usuarios hacen clic en Cancelar durante la instalación, asuma que la cancelación era intencional y cierre el programa sin confirmación. Si esto se debe a la pérdida de un gran tiempo o esfuerzo, permita a los usuarios reiniciar el programa de instalación y seleccionar dónde se dejaron.

-   **Optimizar para la instalación desatendida.**
    -   Presente todas las opciones y preguntas durante la fase de decisión.
    -   En el caso de las fases de descarga e instalación, retrasar la intervención del usuario en los problemas detectados hasta el final de la fase. Al hacerlo, los usuarios pueden dejar la instalación desatendida hasta que vuelvan a su comodidad.
-   **Elimine las páginas innecesarias.** Si la mayoría de los usuarios solo hacen clic en siguiente en una página, considere la posibilidad de deshacerse de la página. Para obtener instrucciones sobre cómo eliminar determinados tipos de páginas, consulte [tipos de página](#page-types).
-   **Elimine el texto innecesario.**
    -   Quitar el texto redundante de las instrucciones y las etiquetas.
    -   No explique los conceptos básicos de uso de Windows, como:
        -   Cómo interactuar con controles (ejemplos: para comenzar, haga clic en siguiente; Para obtener más opciones, haga clic en opciones; Para obtener más información, haga clic en ayuda).
        -   Cómo funcionan los asistentes (por ejemplo, si desea revisar o cambiar algún valor de configuración, haga clic en atrás).
        -   Cómo funciona el programa de instalación (por ejemplo, este programa copiará los archivos de programa en el disco duro...).
-   **Elimine el esfuerzo innecesario.**
    -   Proporcione valores predeterminados buenos:
        -   Por lo general, seleccione la respuesta más segura y privada para que sea la predeterminada.
        -   Si la seguridad y la privacidad no son factores, seleccione la respuesta más probable o cómoda.

            ![captura de pantalla del cuadro de diálogo con el nombre y la compañía mostrados ](images/exper-setup-image9.png)

            En este ejemplo, el nombre de usuario y la organización proporcionados de forma predeterminada se obtienen del registro.

        -   Si se recomienda encarecidamente, considere la posibilidad de seleccionarla de forma predeterminada o de agregar "(recomendado)" a su etiqueta.

    -   Avanzar páginas automáticamente cuando una página no tiene ninguna entrada y la tarea se realiza correctamente, como con las páginas descargar, instalar, progreso y actualizaciones. Una vez realizado el paso, Manténgase solo en estas páginas para mostrar problemas.
    -   Cuando sea práctico, inicie el programa automáticamente cuando finalice la instalación, en lugar de mostrar una página de enhorabuena o de finalización. Cuando el programa de instalación se ejecuta de forma interactiva, supongamos que el usuario está instalando el programa para ejecutarlo de inmediato, por lo que la ejecución del programa es la mejor opción para mostrar que se ha completado la instalación. Ejecutar el programa automáticamente no es práctico cuando el programa de instalación instala más de un programa (por ejemplo, un conjunto que consta de muchos programas), cuando el programa de instalación no se ejecuta de forma interactiva o cuando el proceso de instalación no se completa después de la instalación.

### <a name="page-types"></a>Tipos de páginas

**Páginas de bienvenida y Introducción**

-   **Elimine las páginas de bienvenida.** Aunque es excelente sentir la bienvenida, los usuarios normalmente solo tienen que hacer clic en siguiente sin leer. Y dado que los usuarios normalmente omiten estas páginas sin leer, el texto hace poco más que el estado obvio, por diseño.

    **Incorrecto:**

    ![captura de pantalla de la pantalla de bienvenida con siguiente y cancelar ](images/exper-setup-image10.png)

    En este ejemplo, no hay nada para que el usuario haga clic en siguiente.

-   **Use una página de Introducción solo si debe informar a los usuarios sobre los requisitos previos para la instalación de.** Estos requisitos previos incluyen la instalación de software o hardware necesario, la realización de cambios y actualizaciones de configuración del sistema necesarios, la realización de una copia de seguridad del sistema para proteger contra la pérdida de datos o la obtención de la información necesaria que el usuario aún no tiene.
-   **Siempre que sea práctico, proporcione la capacidad de realizar los requisitos previos directamente desde el programa de instalación.** Los usuarios deben tener que realizar los pasos manualmente solo si no hay ninguna alternativa.
-   Si no se usa una página principal o una página de Introducción, **incluya el nombre del programa y la descripción en la primera página del programa de instalación.** Puede usar el lenguaje de bienvenida como texto de introducción siempre que el propósito de la página sea claro.

**Páginas de términos de licencia**

-   **Escriba los términos de la licencia mediante texto claro y conciso.** Use el lenguaje sin formato. Evite "legalese".
-   **Presente con un formato que sea fácil de leer y examinar.** No utilice los pasajes largos de texto en mayúsculas.

    **Incorrecto:**

    ![captura de pantalla de los términos de licencia en mayúsculas ](images/exper-setup-image11.png)

    En este ejemplo, el texto en mayúsculas y el tamaño de fuente grande hacen que los términos sean difíciles de leer, lo que obliga a los usuarios a desplazarse más de lo necesario.

-   **Requerir consentimiento explícito para aceptar los términos de licencia.** La aceptación de la licencia nunca debe estar seleccionada de forma predeterminada. Si los botones de radio se usan para indicar la aceptación, deje las opciones desactivadas de forma predeterminada y solicite a los usuarios que acepten los términos antes de habilitar el botón siguiente.

    ![captura de pantalla del cuadro de diálogo con el botón siguiente atenuado ](images/exper-setup-image12.png)

    En este ejemplo, el botón siguiente está deshabilitado hasta que los usuarios hayan aceptado explícitamente los términos de licencia.

-   **No es necesario que los usuarios se desplacen a la parte inferior del texto de los términos de licencia antes de que se habilite el botón siguiente.** Esto impone una carga innecesaria a los usuarios para comprender por qué está deshabilitado el botón siguiente.
-   **Proporcione un comando imprimir,** ya sea con un botón de comando o un menú contextual. Presente los términos en un formato optimizado para la impresión.

**Páginas de registro del producto**

-   **Solicite a los usuarios que se registren solo si deben usar el programa.** Explique claramente por qué los usuarios deben registrarse.
-   **Proporcione un registro opcional solo si hay una ventaja clara en el usuario,** por ejemplo, para notificar a los usuarios de las actualizaciones del producto. Deje esta opción desactivada de forma predeterminada.
-   **Permitir a los usuarios registrarse más tarde.** Proporcione un máximo de tres recordatorios y permita a los usuarios descartar los recordatorios con un solo clic.

**Páginas de ámbito (típica, personalizada o mínima)**

-   **Prefiere eliminar esta página.** Supongamos que la mayoría de los usuarios quieren tener la experiencia de instalación típica (y diseñar esa experiencia para que funcione bien para la mayoría de los usuarios).
-   Si debe incluir una página de ámbito:
    -   **Explique las diferencias entre las opciones en cuanto a funcionalidad y espacio en disco.** Los usuarios confían en la claridad de la información de la página ámbito para asegurarse de que hacen la elección correcta.
    -   **Asegúrese de que las opciones personalizadas son necesarias solo para un pequeño porcentaje de usuarios, mientras que la mayoría de los usuarios pueden omitirlas sin ningún riesgo.** De lo contrario, las opciones deben estar en la ruta de acceso de instalación típica.
    -   **Si los usuarios eligen opciones personalizadas, tiene las opciones de instalación típicas seleccionadas de forma predeterminada.** Los usuarios tienen en cuenta la instalación típica como línea de base y desean personalizarla agregando o quitando opciones de esa línea de base.
-   Si debe usar una opción de instalación personalizada, **considere la posibilidad de usar la ubicación y el tamaño de los botones relativos para guiar la mayoría de los usuarios a la instalación típica.**

    ![captura de pantalla del cuadro de diálogo con el botón de instalación grande ](images/exper-setup-image13.png)

    En este ejemplo, el diseño de página refuerza visualmente el hecho de que la mayoría de los usuarios deberían optar por la instalación típica.

**Páginas de entrada**

-   **Para reducir el número de opciones de instalación, haga lo correcto de forma predeterminada.** Para ver las formas de eliminar opciones, consulte [optimizar la configuración](#streamlining-setup).
-   **Proporcione valores predeterminados aceptables siempre que sea posible.** Elija los valores predeterminados que son seguros y privados y que son aceptables para la mayoría de los usuarios sin cambios.
-   **A menos que el programa tenga requisitos inusuales, procure tener una sola página de preguntas y opciones.** Pero si el programa requiere varias páginas de preguntas y opciones, se muestran en el flujo principal de la página del asistente. No intente reducir el número de páginas técnicamente mediante la colocación de opciones en los cuadros de diálogo o el uso de pestañas.
-   ![captura de pantalla del cuadro de diálogo de instalación con cuatro opciones ](images/exper-setup-image14.png)
-   En este ejemplo, las opciones se limitan a una sola página.
-   **Valide la entrada lo antes posible:**
    -   Prohibir caracteres no válidos en la entrada.
    -   Use los [globos](ctrl-balloons.md) para notificar problemas con cuadros de texto no válidos.
    -   Validar los campos relacionados en una página cuando los usuarios hacen clic en siguiente.
    -   Valide los campos relacionados en las páginas de entrada en cuanto se puedan detectar problemas.
-   **Conceda a todas las rutas de acceso de archivo editables un botón examinar.** Permitir a los usuarios especificar rutas de acceso de red.
-   **En la página de entrada final, etiquete el botón de confirmación instalar, no siguiente.** Los usuarios no deben sorprender cuando se inicia la instalación. Antes del punto de confirmación, asegúrese de que los usuarios puedan cambiar fácilmente la configuración.

**Páginas de inicio de la instalación**

-   **Elimine esta página si no tiene ningún propósito distinto de resumir las opciones anteriores y comenzar la instalación.** Si las páginas de entrada son claras y pocas en número, no debería ser necesario resumirlos. En su lugar, la página de entrada final debe tener el botón instalar, que conduce directamente a la página de progreso.
-   **Para instalaciones complejas destinadas a profesionales de ti, proporcione una página de instalación con una lista completa de los cambios que realizará el programa de instalación.** Muchos profesionales de TI tienen un control estricto de administración de cambios, por lo que necesitarán conocer el efecto que tendrá en cuenta la instalación del programa.

**Páginas de progreso**

-   **Proporcione siempre una página de progreso,** incluso si el programa se instala rápidamente. Proporcione una página de progreso independiente para [la fase de descarga](#setup-phases) , si hay alguna. Deshabilite los botones atrás (o anterior) y siguiente mientras el programa de instalación está en curso, pero deje el botón Cancelar habilitado y con capacidad de respuesta.

    ![captura de pantalla del cuadro de diálogo con barra de progreso ](images/exper-setup-image15.png)

    Página de progreso típica.

-   **Use una sola barra de progreso determinante.** Siga las [instrucciones de la barra de progreso de finalización](progress-bars.md), que incluye:
    -   Indique claramente la finalización. No permita que una barra de progreso vaya al 100 por ciento, a menos que la operación se haya completado.
    -   No reinicie el progreso. Una barra de progreso pierde su valor si se reinicia (quizás porque se completa un paso de la operación) porque los usuarios no tienen forma de saber cuándo se completará la operación. En su lugar, haga que todos los pasos de la operación compartan una parte del progreso y que la barra de progreso vaya a finalización una vez.
-   **Proporcione una descripción concisa del paso actual situado encima de la barra de progreso.** En el caso de las instalaciones rápidas, este tipo de texto es innecesario; la barra de progreso solo es suficiente. En el caso de las instalaciones que requieren un minuto o más, el texto puede ser útil para los usuarios que asisten a la instalación.
    -   **Utilice fragmentos de oraciones, que normalmente empiezan por un verbo, y que terminan con puntos suspensivos.** Ejemplos: Copiando archivos..., instalando los componentes necesarios....
    -   **Coloque el texto encima de la barra, no a continuación.**

        **Incorrecto:**

        ![captura de pantalla del texto que se muestra en la barra de progreso ](images/exper-setup-image16.png)

        En este ejemplo, el texto explicativo debe aparecer encima de la barra de progreso.

    -   **Abstenerse de abarrotar la página de progreso con detalles innecesarios.** Esta página no es para [soporte técnico](#handle-technical-support-strategically), por lo que no es necesario mostrar los GUID de registro o los archivos específicos que se han copiado.

        **Incorrecto:**

        ![captura de pantalla del GUID mostrado en la barra de progreso ](images/exper-setup-image17.png)

        En este ejemplo, los detalles técnicos, como los GUID, no tienen sentido para los usuarios.

**Páginas de error**

-   **Si el programa de instalación produce un problema importante, muestre una página de error que explique los problemas junto con los pasos prácticos para resolverlos.** Muestra la página con un icono de error. No use un cuadro de diálogo para este fin.

    ![captura de pantalla de la página de errores y el icono ](images/exper-setup-image18.png)

    En este ejemplo, el error de instalación se explica en una página de error, junto con algunos pasos para resolver el problema.

-   **Si el programa de instalación se completa con un problema recuperable menor, presente el problema como una tarea adicional en lugar de un error.** Use el lenguaje de promoción correcto, orientado a errores, que le anima, no los términos como error, error o problema. No use un icono de error.

**Páginas de enhorabuena/finalización**

-   **Al instalar un único programa de forma interactiva, inicie el programa (y cierre el Asistente para la instalación) para indicar que la instalación se realizó correctamente, en lugar de mostrar una página de finalización. Excepciones**
    -   Las configuraciones que se ejecutan desde la línea de comandos no deben iniciar programas.
    -   Las actualizaciones automáticas (por ejemplo, Windows Update) no deberían iniciar programas.
    -   La instalación de la Directiva de grupo no debe iniciar programas.
    -   Cualquier escenario de instalación profesional de ti (porque no se instala para su propio uso).
-   **Si el programa de instalación tiene pasos de seguimiento después de la instalación, debe enumerarlos en una página de finalización.** No obstante, para justificar una página de finalización, asegúrese de que es probable que los usuarios realicen los pasos y que se indiquen los pasos de forma original (es decir, que no sean obvios).

    **Incorrecto:**

    ![captura de pantalla de la página que muestra el programa de instalación finalizada ](images/exper-setup-image19.png)

    En este ejemplo, una página de finalización innecesaria indica el obvio. Windows Update se ejecuta automáticamente, por lo que no hay ningún motivo por el que los usuarios la ejecuten manualmente.

-   **Al instalar un conjunto de programas, muestra una página de finalización para indicar que la operación se ha realizado correctamente y que pueden ser necesarios pasos de seguimiento.**

    ![captura de pantalla de la página final de la instalación del conjunto de Office ](images/exper-setup-image20.png)

    En este ejemplo, el programa de instalación ha instalado varios programas, por lo que no tiene sentido iniciar un programa determinado automáticamente. Una página de finalización es más adecuada.

### <a name="leaving-users-in-control"></a>Mantener a los usuarios en control

-   **No recopile información personal, como la que se usa para fines de marketing.** El programa de instalación no es una oportunidad para imponer su propia agenda, vender otras ofertas de programas o realizar investigaciones de mercado. puede dañar la relación de confianza con los usuarios de este modo.
-   **No obligue a los usuarios a no participar en la instalación de características opcionales.** Permita que [participen](glossary.md) en su lugar. Por ejemplo, los usuarios deben elegir explícitamente instalar un gadget de escritorio de Windows.
-   **Permitir a los usuarios agregar o quitar características opcionales mediante el programa de instalación después de la configuración inicial.** Los usuarios pueden realizar esta tarea mediante el elemento **desinstalar o cambiar un programa** del panel de control.
-   **En el caso de iniciativas para la mejora de la experiencia del usuario, explique qué datos se transmiten, cómo se utiliza y cuánto tiempo se mantiene.** Use un vínculo a un tema de ayuda de declaración de privacidad para este fin.
-   **Evite el uso de sonido,** ya que muchos escenarios de instalación son desatendidos, y dado que el sonido puede destraerse innecesariamente incluso durante las instalaciones atendidas.

### <a name="security"></a>Seguridad

-   **En el caso de la instalación basada en Internet, proporcione las actualizaciones de seguridad automáticamente durante la configuración inicial.** Los usuarios no deben actualizarse como un paso independiente.
-   **No se recomienda que los usuarios desactiven los firewalls como requisito previo para instalar el programa.**
-   Si un firewall debe estar desactivado, haga lo siguiente:
    -   **Limite la duración de esta condición a lo más breve posible.**
    -   **Señale explícitamente cuando los usuarios puedan volver a activar el firewall.**

### <a name="uninstall"></a>Desinstalación

-   **La desinstalación debe quitar todos los seguimientos de un programa, incluidos los siguientes:**
    -   Archivos de programa, incluido el programa de instalación de.
    -   Entradas del menú Inicio.
    -   Iconos de escritorio e iconos de inicio rápido (si existen).
    -   Configuración del registro.
    -   Asociaciones de archivo.
-   **La desinstalación debe dejarse detrás de lo siguiente:**
    -   Archivos creados por el usuario, como archivos de documento.
    -   Bibliotecas de vínculos dinámicos compartidas almacenadas en la carpeta del sistema.

### <a name="help-and-support"></a>Ayuda y soporte técnico

-   **Diseñe el programa de instalación para que no necesite ayuda formulando preguntas claras y explicativas.** Reserve ayuda para preguntas avanzadas que realmente se beneficien de una explicación más detallada.
-   **No use archivos Léame.** Estos archivos ahora están obsoletos y los usuarios no los leen de todos modos. En su lugar, proporcione contenido en línea si es necesario.
-   **Vínculo a los temas de ayuda adecuados o a la solución de problemas de contenido de los mensajes de error del programa de instalación.** Asegúrese de que el contenido de la ayuda proporciona una ruta de acceso clara para resolver el problema. Para obtener más información, consulte [mensajes de error](mess-error.md).
-   **Cree archivos de registro para capturar información útil para el soporte técnico.** No cargue la interfaz de usuario del programa de instalación con detalles relacionados con el soporte técnico que no tienen sentido para la mayoría de los usuarios. En su lugar, use los archivos de registro para este fin.

### <a name="text"></a>Texto

-   **Sea conciso.** Los asistentes de instalación suelen explicar las características y las opciones, mediante bloques de texto difíciles de analizar rápidamente. **Excepciones:**
    -   Deletrea todos los acrónimos. La configuración suele ser la primera vez que los usuarios tienen el programa, por lo que no se da por hecho que comprenden jerga como acrónimos.
    -   Explique terminología y conceptos desconocidos, preferiblemente en su lugar, pero con los temas de ayuda si es necesario.
-   **Prefiera un tono profesional y práctico. Evite un tono demasiado técnico.**

**Incorrecto:**

Restrinja la instalación por usuario.

**Correcto:**

Instalar solo para mí.

-   No use ahora las etiquetas del botón de comando porque se puede realizar la inmediatez del comando para concedido.
    -   **Excepción:** Cuando sea necesario, use ahora para diferenciar los comandos que inician una tarea de comandos que realizan una tarea inmediatamente.

![captura de pantalla del botón Descargar ](images/exper-setup-image21.png)

En este ejemplo, al hacer clic en el botón de comando se dirige a una ventana o página que permite a los usuarios descargar.

![captura de pantalla del botón Descargar ahora ](images/exper-setup-image22.png)

En este ejemplo, al hacer clic en el botón de comando se realiza la descarga inmediatamente.

Solo un comando de un flujo de tareas debe etiquetarse con Now. Por lo tanto, por ejemplo, un comando **Descargar ahora** nunca debe ir seguido de otro comando **Descargar ahora** .

-   Usar términos de licencia, no contrato de licencia, contrato de licencia, contrato de licencia para el usuario final o CLUF.

Para obtener más instrucciones, consulte [estilo y tono](text-style-tone.md).

## <a name="documentation"></a>Documentación

-   Como verbo, la configuración es de dos palabras: como adjetivo o sustantivo, el programa de instalación es una palabra.
-   El programa de instalación se pone en mayúsculas y no se divide en guiones.
-   Use instalar para hacer referencia a la adición de hardware o software a un sistema informático.
-   No utilice install como sustantivo. En su lugar, use la instalación de.
-   Use reiniciar, no reiniciar. Indique que es el equipo, no un programa, que se está reiniciando.

 

 