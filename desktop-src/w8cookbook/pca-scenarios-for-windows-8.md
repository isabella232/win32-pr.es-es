---
title: Escenarios del Asistente de compatibilidad de programas para Windows 8
description: Escenarios del Asistente de compatibilidad de programas para Windows 8
ms.assetid: C61BF746-63EE-4F4E-81D3-52947FD4954D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d63fbd912e14ac682ffe820ad140b2cad6a487dfbac833aa419c53389a9339ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852669"
---
# <a name="program-compatibility-assistant-scenarios-for-windows-8"></a>Escenarios del Asistente de compatibilidad de programas para Windows 8

## <a name="platforms"></a>Plataformas

**Clientes:** Windows XP \| Windows Vista \| Windows 7 \| Windows 8  

## <a name="description"></a>Descripción

El Asistente para compatibilidad de programas (PCA) es una característica de Windows 8 que ayuda a los usuarios finales a ejecutar aplicaciones de escritorio diseñadas para versiones Windows anteriores. Windows 8 tiene una excelente compatibilidad de aplicaciones integrada que permite que las aplicaciones diseñadas para Windows 7 o versiones anteriores de Windows funcionen muy bien en Windows 8 automáticamente. Sin embargo, hay un pequeño número de aplicaciones que pueden tener problemas para ejecutarse sin intervención.

Cuando un usuario ejecuta una aplicación, PCA realiza un seguimiento de la aplicación e identifica los síntomas de determinados problemas de compatibilidad conocidos en Windows 8. Cuando detecta algún síntoma de problema, proporciona al usuario la oportunidad de aplicar una corrección recomendada que le ayudará a ejecutar mejor la aplicación en Windows 8.

## <a name="scenarios"></a>Escenarios

PCA realiza un seguimiento de las aplicaciones para ver si hay un conjunto de problemas de compatibilidad conocidos en Windows 8. PCA realiza un seguimiento de los problemas, identifica las correcciones y proporciona un cuadro de diálogo al usuario con instrucciones para aplicar una corrección recomendada. El usuario puede decidir aplicar las correcciones recomendadas o elegir no hacer nada y cancelar la recomendación. Si el usuario se cancela, PCA ya no realizará el seguimiento de esa aplicación.

PcA suele aplicar uno de los tres modos de compatibilidad de Windows: Windows XP SP3, Windows Vista SP2 o Windows 7, dependiendo de cuándo se haya escrito el programa (o su configuración). PCA usa los atributos LINK DATE y SUBSYSTEM VERSION del programa y las secciones TRUSTINFO y COMPATIBILITY del manifiesto de archivo ejecutable para determinar cuál de los modos es pertinente y aplica \_ Windows XP SP3 (incluye privilegios administrativos), Windows Vista SP2 o Windows 7, respectivamente. Un glosario al final del documento enumera cada uno de los modos de compatibilidad que aplica PCA y su descripción.

En todos los escenarios que se enumeran a continuación, PCA realiza un seguimiento de las aplicaciones por segunda vez después de aplicar una corrección. Si la aplicación sigue fallando de la misma manera incluso después de aplicar una corrección de compatibilidad, PCA revierte la corrección. A continuación, PCA dejará de realizar el seguimiento permanente de la aplicación específica que ha fallado.

Aunque PCA realiza un seguimiento de muchos posibles problemas, no todos los problemas provocarán errores en la aplicación. PCA recomienda correcciones solo en situaciones en las que hay una alta probabilidad de que el error de la aplicación se deba a Windows de compatibilidad. Las secciones siguientes se expanden en cada uno de los escenarios de PCA desarrollados en Windows 8. En cada sección se describe el escenario del problema y las recomendaciones que pca proporciona para permitir que la aplicación siga funcionando correctamente en Windows 8.

Para obtener más información sobre los cambios de compatibilidad en Windows 8, consulte los otros temas de la guía *Windows 8 compatibilidad*.

Los escenarios a los que PCA realiza un seguimiento y recomienda correcciones son:

-   No se puede instalar o desinstalar la aplicación
-   No se puede ejecutar la aplicación con un mensaje de Windows de comprobación de versión
-   No se puede iniciar la aplicación debido a privilegios administrativos
-   Bloqueos de aplicaciones debido a problemas de memoria específicos
-   Se produce un error en la aplicación debido a archivos del sistema no coincidentes
-   Se produce un error en la aplicación debido a errores no controladas en aplicaciones de 64 Windows
-   Se produce un error en la aplicación al intentar eliminar archivos no Windows protegidos
-   Se produce un error en la aplicación al intentar modificar Windows archivos
-   Se produce un error en la aplicación debido al uso de modos de color de 8 o 16 bits
-   Se produce un error en la aplicación debido a problemas de visualización y gráficos
-   La aplicación no puede declarar el reconocimiento de PPP
-   Se produce un error en la aplicación debido a que faltan Windows características
-   Se produce un error en la aplicación debido a controladores sin signo en el equipo de 64 Windows 8
-   Seguimiento de aplicaciones instaladas a través de la configuración de compatibilidad
-   La aplicación no puede iniciar instaladores o actualizadores
-   Instaladores de aplicaciones que deben ejecutarse con privilegios administrativos
-   Applets Panel de control heredados que deben ejecutarse con privilegios administrativos

Cada uno de estos escenarios se expande a continuación:

**No se puede instalar o desinstalar la aplicación**

Uno de los tipos más comunes de errores de la aplicación se produce durante la instalación de la aplicación. Los programas de instalación más antiguos normalmente producirán un error de dos maneras:

-   El programa de instalación no conoce las características de Control de cuentas de usuario (UAC) de Windows 8, por lo que es posible que no se ejecute con los privilegios completos necesarios para realizar cambios en el sistema en las áreas protegidas de Windows 8
-   El programa de instalación comprueba la versión Windows y se bloquea para que no se ejecute si la versión es mayor de lo esperado.

Estas condiciones de error son dos de los tipos más comunes de errores de compatibilidad en la instalación. PCA, con la ayuda de otros componentes de Windows, como UAC, detecta los programas de instalación en el inicio y los realiza un seguimiento hasta el final de la instalación. Si el programa de instalación no puede agregar archivos o si agrega una entrada válida en la parte "Agregar quitar programas" del panel de control de Windows, PCA considera que se ha produce un error en la instalación.

En este caso, PCA recomienda un modo de compatibilidad adecuado para la aplicación. El modo de compatibilidad permite que el programa de instalación se ejecute en el modo Windows para el que se diseñó y también garantiza que la aplicación se ejecute con privilegios administrativos. PCA aplica el modo de compatibilidad RUNASADMIN junto con el modo de compatibilidad Windows XP, Windows Vista o Windows 7. El usuario, al final de la instalación con errores, verá un cuadro de diálogo con la recomendación de PCA:

![La aplicación no puede instalar o desinstalar el cuadro de diálogo](images/pcafigure1.png)

A continuación, el usuario puede elegir:

-   Ejecute el programa con la configuración de compatibilidad (opción recomendada), después de lo cual PCA aplicará la configuración recomendada (modo de compatibilidad), reinicie el programa de instalación y realice un seguimiento de él hasta que la instalación se complete correctamente.
-   Indique que el programa se instaló correctamente, en cuyo caso PCA no agregará ninguna configuración y dejará de realizar el seguimiento de la instalación.
-   Haga clic en Cerrar, en cuyo caso PCA no agregará ninguna configuración y dejará de realizar el seguimiento de esta configuración.

El mismo mecanismo se usa para ayudar a la desinstalación de la aplicación cuando un usuario intenta desinstalar la aplicación desde la sección "Agregar quitar programas" de Windows o desde el acceso directo del desinstalador de la aplicación.

**No se puede ejecutar la aplicación con un mensaje de Windows de comprobación de versión**

Uno de los errores de compatibilidad más comunes en el entorno de ejecución de la aplicación se debe a la Windows de la versión. Muchas aplicaciones, al iniciarse, comprueban Windows versión; Si no reconocen la versión, se bloquean a sí mismos aunque la aplicación se haya podido ejecutar sin problemas.

Por lo general, estas comprobaciones están asociadas a dos condiciones de las que realiza un seguimiento el PCA:

La aplicación muestra un cuadro de mensaje que advierte al usuario. A continuación se muestra un ejemplo:

![No se puede ejecutar la aplicación con un cuadro de diálogo de mensaje de comprobación de versión de Windows](images/pcafigure2.png)

-   La aplicación finaliza inmediatamente o se bloquea

Si PCA identifica ambas condiciones para una aplicación, proporcionará una recomendación al usuario. PCA permitirá al usuario volver a ejecutar la aplicación con la configuración de compatibilidad. PCA aplicará los requisitos Windows XP, Windows Vista o Windows de compatibilidad 7 según la aplicación. Como en cualquiera de los escenarios, el usuario puede decir a PCA que la aplicación se ejecutó correctamente o rechazar la configuración recomendada haciendo clic en el botón Cerrar. A continuación se proporciona un cuadro de diálogo de ejemplo:

![La aplicación no se puede ejecutar con un cuadro de diálogo de opción de mensaje de comprobación de versión de Windows](images/pcafigure3.png)

**No se puede iniciar o ejecutar la aplicación debido a privilegios administrativos**

Algunas aplicaciones necesitan privilegios administrativos para ejecutar y ejecutar su funcionalidad. Sin embargo, en Windows 8, de forma similar a Windows 7 y Windows Vista, las aplicaciones se ejecutan en niveles de privilegios inferiores de forma predeterminada debido a UAC. Las aplicaciones más recientes diseñadas para Windows Vista y versiones posteriores generalmente declararán el nivel de privilegios en el que deben ejecutarse mediante la sección TRUSTINFO del manifiesto exe. Sin embargo, las aplicaciones anteriores suelen producir un error de dos maneras:

-   La aplicación muestra un mensaje al usuario que indica que requiere privilegios administrativos, como se muestra a continuación:

![No se puede iniciar o ejecutar la aplicación debido al cuadro de diálogo de privilegios administrativos](images/pcafigure4a.png)

-   La aplicación finaliza inmediatamente o se bloquea

Si PCA identifica ambas condiciones para una aplicación, proporcionará una recomendación al usuario. PCA permitirá al usuario volver a ejecutar la aplicación con privilegios administrativos (PCA aplica el modo de compatibilidad RUNASHIGHEST). El usuario recibirá un mensaje de UAC cuando se vuelva a ejecuta la aplicación. Como en cualquiera de los escenarios, el usuario puede optar por volver a ejecutar con la configuración recomendada o rechazar la configuración recomendada haciendo clic en Cerrar. A continuación se proporciona un cuadro de diálogo de ejemplo:

![No se puede iniciar o ejecutar la aplicación debido al cuadro de diálogo de opción de privilegios administrativos](images/pcafigure5.png)

**Bloqueos de aplicaciones debido a problemas de memoria específicos**

Algunas aplicaciones se bloquean debido a un problema de memoria conocido. La aplicación des hace referencia a un archivo DLL de la memoria y, a continuación, llama a una función para ejecutar código en el mismo archivo DLL. Esto provoca un bloqueo inmediato de la aplicación. Aunque este problema no se debe a Windows 8 de compatibilidad, es un problema relativamente común que se observa en una amplia variedad de aplicaciones. PCA realiza un seguimiento de este problema para ofrecer a los usuarios la oportunidad de ejecutar su aplicación de forma más confiable.

Para estas aplicaciones, PCA aplica automáticamente el modo de compatibilidad PINDLL de forma silenciosa. El modo de compatibilidad invocado por PCA impide que la aplicación libera el archivo DLL de la memoria. Por lo tanto, la llamada de función a la DLL por parte de la aplicación funcionará, lo que impide que la aplicación se bloquea y permite que siga funcionando correctamente.

**Se produce un error en la aplicación debido a archivos del sistema no coincidentes**

Algunas aplicaciones diseñadas para Windows XP y anteriores incluyen copias Windows archivos DLL del sistema junto con sus instaladores. Cuando se instalan estas aplicaciones, la aplicación tiene una copia anterior del archivo DLL en su propia carpeta, así como la versión más reciente del archivo DLL que se encuentra en las Windows del sistema.

En Windows Vista y versiones posteriores, esta condición puede provocar un error en la aplicación cuando intenta cargar el archivo DLL local, ya que este archivo DLL no funcionará bien con el resto de los archivos DLL del sistema de Windows actuales. Puesto que la aplicación generalmente no conoce las versiones más recientes de este archivo DLL, no funciona correctamente.

Cuando PCA detecta que el archivo DLL no se pudo cargar correctamente, aplicará una configuración de compatibilidad que permite a Windows cargar la versión más reciente del archivo DLL desde la carpeta del sistema de Windows para que la aplicación se pueda ejecutar correctamente.

Al final de la primera ejecución con errores de la aplicación, los usuarios verán el cuadro de diálogo PCA que les notifica la configuración aplicada como se indica a continuación:

![Se produce un error en la aplicación debido a un cuadro de diálogo de archivos del sistema no coincidentes](images/pcafigure6.png)

**Se produce un error en la aplicación debido a errores no controladas en aplicaciones de 64 Windows**

En la versión de 64 bits de Windows 8, se ha habilitado una nueva excepción para el mecanismo de devolución de llamada del bucle de mensajes. Aunque esta excepción se introdujo por primera Windows 7, no era obligatorio controlar este error. En Windows 8, las aplicaciones que usan bucles de mensajes deben controlar esta nueva excepción. Si no lo hacen, se bloquearán. Es posible que las aplicaciones diseñadas Windows versiones anteriores no conozcan esta excepción y, por tanto, no puedan controlar este error (excepción) correctamente.

PCA detecta las aplicaciones que no se pueden aplicar debido a este error no controlada y aplica automáticamente el modo de compatibilidad DISABLEUSERCALLBACKEXCEPTION para la aplicación. Una vez aplicada la configuración al final de la ejecución, se notifica al usuario como se indica a continuación. La aplicación obtiene el modo en la siguiente ejecución y podrá evitar este error.

![Se produce un error en la aplicación debido a errores no controladas en el cuadro de diálogo de ventanas de 64 bits](images/pcafigure7.png)

**Se produce un error en la aplicación al intentar eliminar archivos no Windows protegidos**

Algunas aplicaciones diseñadas para Windows XP y anteriores suponen que normalmente se ejecutan con privilegios administrativos completos. Como curso del comportamiento normal de la aplicación, pueden intentar eliminar archivos no Windows protegidos (ya sea en archivos de programa o Windows carpetas). Cuando se produce un error en la operación de eliminación, muchas de estas aplicaciones se pueden bloquear.

PCA detecta estas aplicaciones que no pueden eliminar archivos protegidos y se bloquean, y proporciona una recomendación al usuario. PCA permitirá al usuario volver a ejecutar la aplicación con la configuración de compatibilidad. Como en cualquiera de los escenarios, el usuario puede decir a PCA que la aplicación se ejecutó correctamente o rechazar la configuración recomendada haciendo clic en el botón Cerrar. En este caso, PCA aplica el modo de compatibilidad VIRTUALIZEDELETE. A continuación se proporciona un cuadro de diálogo de ejemplo:

![Se produce un error en la aplicación al intentar eliminar el cuadro de diálogo de archivos protegidos que no son de Windows](images/pcafigure8.png)

**Se produce un error en la aplicación al intentar modificar Windows archivos o claves del Registro**

Algunas aplicaciones diseñadas para Windows XP y anteriores suponen que normalmente se ejecutan con privilegios administrativos completos. Como curso del comportamiento normal de la aplicación, pueden intentar modificar, eliminar o escribir archivos protegidos Windows (ya sea en archivos de programa o carpetas Windows) o claves del Registro propiedad de Windows. Cuando se produce un error en cualquiera de las operaciones de escritura, eliminación o modificación de un archivo o una clave del Registro, muchas de estas aplicaciones se pueden bloquear o producir un error grave.

PCA detecta estas aplicaciones que no pueden escribir en archivos Windows claves del Registro y proporciona una recomendación al usuario cuando se cierra la aplicación. PCA permitirá al usuario volver a ejecutar la aplicación con la configuración de compatibilidad. Como en cualquiera de los escenarios, el usuario puede decir a PCA que la aplicación se ejecutó correctamente o rechazar la configuración recomendada haciendo clic en el botón Cerrar. En este caso, PCA aplica el modo de compatibilidad WRPMITIGATION. A continuación se proporciona un cuadro de diálogo de ejemplo:

![Se produce un error en la aplicación al intentar modificar archivos de Windows o el cuadro de diálogo de claves del Registro](images/pcafigure9.png)

**Se produce un error en la aplicación debido al uso de modos de color de 8 o 16 bits**

Como parte de la nueva Windows 8 para aplicaciones de la Tienda Windows, uno de los cambios clave es que el Administrador de ventanas de escritorio (DWM) ahora solo admitirá colores de 32 bits en Windows 8. Ahora se simulan los modos de color inferior.

Muchas aplicaciones y juegos más antiguos diseñados para Windows XP o antes usan modos de color de 8 o 16 bits. Sin mitigación, estas aplicaciones podrían no ejecutarse en Windows 8. Sin embargo, cuando estas aplicaciones enumeran o intentan usar cualquiera de los modos de color de 8 o 16 bits para la presentación, PCA identifica inmediatamente el problema y, con la ayuda de DWM, garantiza que la aplicación funcionará correctamente con el modo de color simulado.

Tenga en cuenta que esto sucede en cuanto la aplicación solicita los modos de color bajo y es transparente para el usuario. El usuario no tiene que reiniciar la aplicación para obtener esta mitigación, ya que esta corrección siempre es necesaria para asegurarse de que la aplicación funciona correctamente.

**Se produce un error en la aplicación debido a problemas de visualización y gráficos**

Dado que Administrador de ventanas de escritorio (DWM) siempre está en Windows 8, algunas aplicaciones de la era xp anteriores de Windows pueden producir un error si la aplicación usa API de gráficos en modo mixto, como en el uso de las API GDI y DirectX para dibujar en la pantalla (principalmente juegos antiguos) e intenta usar el modo de pantalla completa:

-   DWM impedirá pintar directamente en el escritorio y el juego o la aplicación producirá un error o dibujará una pantalla negra en el escritorio y ninguno de los gráficos estará visible.
-   En tales casos, cuando la aplicación se cierra, Windows detecta que la aplicación o el juego tiene un problema con el modo de pantalla completa y aplica el modo de compatibilidad DXMAXIMIZEDWINDOWEDMODE que permite que la aplicación o el juego se ejecuten en un modo de ventana maximizado en lugar de en un modo de pantalla completa.
-   Una vez aplicada la configuración al final de la ejecución, pca notifica al usuario como se muestra a continuación. la aplicación tendrá el modo de compatibilidad en la siguiente ejecución y podrá ejecutarse correctamente.

![Se produce un error en la aplicación debido a gráficos y al cuadro de diálogo de problemas de visualización](images/pcafigure10.png)

**La aplicación no puede declarar el reconocimiento de PPP**

Otro problema típico de visualización con muchas aplicaciones anteriores se produce cuando Windows y la aplicación se ejecutan en modo de valores altos de PPP, pero la aplicación no declara su reconocimiento de valores altos de PPP a través de su manifiesto EXE. Entre los problemas comunes que pueden producirse debido a este error de coincidencia en la configuración se encuentran los elementos de interfaz de usuario recortados o el texto y un tamaño de fuente incorrecto. Para más información sobre los problemas, consulte este [vínculo aquí.](/previous-versions//dd464660(v=vs.85))

En tales casos, Windows detecta que la aplicación es compatible con valores altos de PPP y aplica el modo de compatibilidad HIGHDPIAWARE a la aplicación al final de la primera ejecución. A continuación, PCA informará al usuario sobre esto como se muestra a continuación:

![La aplicación no puede declarar el cuadro de diálogo de reconocimiento de ppp](images/pcafigure11.png)

**Se produce un error en la aplicación debido a que faltan Windows características**

Algunas aplicaciones dependen de Windows características que se han quitado desde Windows Vista. Cuando estas aplicaciones intentan cargar los archivos DLL o componentes COM que faltan, no funcionan.

PCA detecta las aplicaciones cuando intentan cargar las características de Windows que faltan y proporciona una recomendación para descargar estos componentes e instalarlos una vez que finalice la aplicación. El usuario puede hacer clic en "obtener ayuda en línea" para encontrar una alternativa o descargar la característica e instalarla. Si es necesario, el usuario puede elegir no hacer nada haciendo clic en Cerrar.

![Se produce un error en la aplicación debido a que falta el cuadro de diálogo de características de Windows](images/pcafigure12.png)

**Se produce un error en la aplicación debido a controladores sin signo en el equipo de 64 Windows 8**

Los controladores de 64 Windows requieren controladores firmados digitalmente (archivos SYS) desde Windows Vista. Sin embargo, las aplicaciones anteriores diseñadas antes del lanzamiento de Windows Vista suministraban controladores que no estaban firmados digitalmente. Si se instala este tipo de controlador sin signo, Windows cargará. En raras ocasiones, es posible que Windows se inicie si estos controladores se marcan como controladores de tiempo de arranque.

Algunas aplicaciones anteriores instalan controladores que no están firmados en aplicaciones de 64 bits Windows. Cualquier dispositivo o aplicación que intente usar este controlador puede producir un error o provocar un bloqueo del sistema. Para evitar este escenario, PCA detecta aplicaciones cuando instalan controladores sin signo y deshabilita el controlador que está marcado como controlador en tiempo de arranque.

También indica al usuario que adquiera un controlador firmado digitalmente para que la aplicación funcione correctamente. El mensaje se muestra como resultado de la instalación del controlador y como resultado de la instalación de la aplicación. Si otra aplicación instala el mismo controlador, esa aplicación también recibirá el mismo mensaje.

![Se produce un error en la aplicación debido a controladores sin signo en el cuadro de diálogo de Windows 8 de 64 bits](images/pcafigure13.png)

**Seguimiento de aplicaciones instaladas a través de la configuración de compatibilidad**

Cuando se produce un error en un instalador, PCA ayuda al instalador con varios modos de compatibilidad en función del tipo de error. Una vez que el instalador se realiza correctamente con la configuración de compatibilidad, PCA realizará un seguimiento de los accesos directos que agregó el instalador. Esto se hace para realizar un seguimiento de si las aplicaciones que se instalaron también pueden necesitar que se aplique la configuración de compatibilidad a su instalador.

Cuando un usuario inicia este tipo de aplicación, PCA solicita al usuario que pregunte si la aplicación ha funcionado correctamente. Si el usuario responde, "Sí", el PCA deja de realizar el seguimiento de la aplicación. Si el usuario responde "No", aplica el mismo modo de compatibilidad que se aplicó al instalador de la aplicación y vuelve a ejecuta la aplicación con el modo de compatibilidad aplicado.

**La aplicación no puede iniciar instaladores o actualizadores**

A veces, las aplicaciones inician programas secundarios que deben ejecutarse como administradores. Esto suele ocurrir cuando una aplicación intenta iniciar su software de actualizador para comprobar e instalar nuevas actualizaciones en la aplicación. Cuando las aplicaciones ejecutan directamente estos programas secundarios, el programa secundario puede no iniciarse porque la propia aplicación no tenía privilegios administrativos o porque el programa secundario no se ha marcado correctamente para la elevación con el manifiesto de UAC.

PCA realiza un seguimiento de estos errores y, cuando se cierra la aplicación principal, aplica automáticamente el modo de compatibilidad ELEVATECREATEPROCESS que ayudará a que los programas secundarios se ejecuten correctamente. Cuando la aplicación inicia la aplicación secundaria en ejecuciones posteriores, el usuario verá un cuadro de diálogo UAC para el programa secundario.

A continuación se muestra un ejemplo del cuadro de diálogo PCA:

![No se puede iniciar el cuadro de diálogo instaladores o actualizadores de la aplicación](images/pcafigure14.png)

**Instaladores de aplicaciones que deben ejecutarse con privilegios administrativos**

Los instaladores Windows aplicaciones de escritorio requieren privilegios administrativos, ya que escriben archivos, carpetas y entradas del Registro en áreas del sistema protegidas. Windows (UAC) tiene lógica de detección para identificar cuándo se ejecuta un instalador y solicita inmediatamente al usuario que proporcione privilegios administrativos a través del cuadro de diálogo UAC. Sin embargo, en algunos casos, esta lógica no podrá determinar que una aplicación era realmente un instalador y es posible que no obtenga privilegios administrativos. Por lo general, se trata de instaladores personalizados que no usan tecnologías de instalación conocidas, como Windows Installer o Install Shield.

En tales casos, PCA detecta que el instalador no pudo escribir sus archivos. Al final, si no se pudo instalar, PCA proporcionará una recomendación para aplicar la configuración de compatibilidad. Si el usuario elige hacer clic en "Ejecutar programa", pca aplicará el modo de compatibilidad RUNASADMIN y volverá a ejecutar el instalador. Si el usuario decide cerrar, no se aplicará ninguna configuración. A continuación se muestra un cuadro de diálogo PCA de ejemplo:

![Captura de pantalla que muestra un ejemplo de un cuadro de diálogo para un instalador de aplicación que debe ejecutarse con privilegios administrativos.](images/pcafigure15.png)

Los applets Panel de control que deben ejecutarse con privilegios administrativos Los applets del Panel de control suelen cambiar la configuración del sistema y necesitan la capacidad de ejecutar el administrador de anuncios. Sin embargo, los escritos antes Windows Vista no tienen un manifiesto EXE o no tienen la sección TRUSTINFO que declara el nivel de privilegio que requieren. Cuando se ejecutan estos applets, PCA los detecta y, al final de la primera ejecución, proporciona una recomendación para ejecutarse con la configuración administrativa. Si el usuario elige hacer clic en "Ejecutar programa", PCA aplica el modo de compatibilidad RUNASADMIN y vuelve a ejecutar el instalador. Si el usuario decide cerrar, no se aplicará ninguna configuración. A continuación se muestra un cuadro de diálogo PCA de ejemplo:

![instaladores de aplicaciones que deben ejecutarse con privilegios administrativos](images/pcafigure16.png)

**Comprobación de la configuración recomendada a través de comentarios del usuario**

Al final de cada uno de los escenarios (después de ejecutar la aplicación con la configuración de compatibilidad recomendada), PCA hará una pregunta sencilla al usuario:

![comprobar la configuración recomendada a través del cuadro de diálogo de comentarios del usuario](images/pcafigure17.png)

El usuario puede proporcionar comentarios si la aplicación funcionó o no con la configuración de compatibilidad. Estos datos se enviarán de forma anónima a Microsoft. Esto ayuda a garantizar que estas correcciones se puedan crear en Windows 8 Windows través de un proceso de actualización, de modo que los usuarios futuros de Windows 8 ya no encuentren el error de la aplicación y pca ya no necesite realizar el seguimiento del error en la aplicación.

**Seguimiento de problemas que no tienen recomendaciones**

Las aplicaciones pueden producir errores de muchas maneras diferentes por motivos de compatibilidad. PCA realiza un seguimiento de muchos más problemas de compatibilidad de los que se enumeran en los escenarios anteriores. En estos casos, muchas veces, la incidencia depende de la aplicación. Esto significa que algunas aplicaciones controlan estos problemas correctamente y se recuperan de él, mientras que otras no. Por lo tanto, para estos problemas, aunque PCA sigue el seguimiento de la aplicación, no proporciona una recomendación directa para una corrección.

Los problemas que pca realiza un seguimiento que no tienen una configuración recomendada o un cuadro de diálogo incluyen aplicaciones que:

-   Tener un tiempo de ejecución muy corto: las aplicaciones se ejecutan durante no más de tres segundos
-   Creación de objetos de memoria global sin privilegios administrativos
-   Error (excepción win32) al iniciarse
-   Comprobación de privilegios administrativos (pero no puede producirse un error)
-   Uso de códecs Indeo (en desuso de Windows Vista)
-   Intente escribir o eliminar claves de ubicaciones del Registro protegidas, como HKLM.
-   Bloqueo al iniciar

**Aplicación de correcciones mediante la pestaña compatibilidad y el solucionador de problemas de compatibilidad**

Como se mencionó anteriormente, las aplicaciones pueden producir un error por diversos motivos de compatibilidad. No todas tienen una recomendación clara de PCA, ya que la configuración depende de la aplicación. Sin embargo, los usuarios pueden ir al Solucionador de problemas de compatibilidad o a la pestaña Compatibilidad para aplicar ciertas correcciones comunes para intentar que su aplicación con errores funcione correctamente en Windows 8. En tales casos, PCA seguirá el seguimiento de la aplicación en busca de problemas de compatibilidad, antes y después de aplicar la corrección. Después de ejecutar la aplicación con la corrección aplicada, PCA le preguntará al usuario si la corrección ha funcionado. Una vez que el usuario responde a la pregunta, los datos se envían de forma anónima a través de telemetría a Microsoft. Estos datos se recopilan de muchos usuarios y se analizan, y las correcciones de calificación se distribuyen ampliamente a todos los Windows 8 a través de Windows actualización.

**Uso del solucionador de problemas de compatibilidad**

El solucionador de problemas de compatibilidad es un mecanismo de Windows que permite diagnosticar problemas con las aplicaciones y aplicar las correcciones recomendadas para que funcionen correctamente. Esto solo es necesario cuando PCA no proporciona ninguna recomendación para la aplicación.

El solucionador de problemas permite a los usuarios recorrer y responder a un conjunto de preguntas y, en función de las respuestas, aplicará un conjunto de correcciones y permitirá a los usuarios probar sus aplicaciones y comprobar las correcciones. Una vez comprobadas, las correcciones se aplicarán permanentemente a las aplicaciones para que funcionen mejor en Windows 8.

La interfaz de usuario del solucionador de problemas se muestra a continuación como referencia:

![uso del cuadro de diálogo solucionador de problemas de compatibilidad](images/pcafigure18.png)

Puede iniciar el Solucionador de problemas de compatibilidad de dos maneras:

**En la pantalla de inicio:**

1.  Tipo: solucionador de problemas de compatibilidad
2.  En la sección configuración, haga clic en el icono "Ejecutar programas realizados para la versión anterior de Windows".

  
**En el icono de la aplicación:**

1.  En el panel pantalla Inicio, haga clic con el botón derecho en el icono de la aplicación.
2.  Haga clic en "Abrir ubicación de archivo" (solo aplicaciones de escritorio)
3.  En la cinta explorador, haga clic en la pestaña "Aplicación".
4.  Elija "Solucionar problemas de compatibilidad".

  


**Uso de la pestaña Compatibilidad**

Tenga en cuenta que esto solo se recomienda para los usuarios que son expertos en probar diferentes configuraciones de compatibilidad. Este método no proporciona ninguna recomendación del tipo de corrección que se va a aplicar a las aplicaciones. En este caso, se espera que el usuario sepa qué correcciones se pueden aplicar para que la aplicación funcione. Si no está seguro de las correcciones, use el Solucionador de problemas de compatibilidad para encontrar una corrección para la aplicación.

Para acceder a la pestaña Compatibilidad:

 **En la pantalla de inicio:**

1.  Haga clic con el botón derecho en el icono de la aplicación.
2.  Abrir ubicación de archivo (solo aplicaciones de escritorio)

  
**En la cinta explorador:**

1.  Haga clic en Propiedades.
2.  Vaya a la pestaña Compatibilidad.
3.  Selección de las correcciones de compatibilidad
4.  Volver a ejecutar la aplicación
    > [!Note]  
    > Puede volver al mismo lugar de nuevo para cambiar o quitar también las correcciones. También puede aplicar las correcciones a todos los usuarios de la máquina mediante el botón que se proporciona en la pestaña.

     

  


![uso de la pestaña de compatibilidad](images/pcafigure19.png)

**Aplicaciones con problemas de compatibilidad conocidos**

Además de los escenarios de detección de problemas en tiempo de ejecución enumerados anteriormente, PCA también informa a los usuarios en el inicio de la aplicación si la aplicación tiene problemas de compatibilidad conocidos. La lista se almacena en la base de datos de compatibilidad de aplicaciones del sistema. Hay dos tipos de estos mensajes:

-   **Mensajes de** bloqueo duro: si se sabe que la aplicación es incompatible y si se permite que la aplicación se ejecute, tendrá un impacto grave en el sistema (por ejemplo, un bloqueo de Windows o no se puede arrancar después de la instalación), se mostrará un mensaje de bloqueo como se muestra a continuación.

![aplicaciones con problemas de compatibilidad conocidos: cuadro de diálogo de bloqueo de mensajes](images/pcafigure20.png)

-   **Mensajes de bloqueo flexible:** si la aplicación tiene un problema de compatibilidad conocido y puede que no funcione correctamente, se muestra este mensaje:

![aplicaciones con problemas de compatibilidad conocidos: cuadro de diálogo de mensajes de bloqueo flexible](images/pcafigure21.png)

En ambos casos, la opción "Obtener ayuda en línea" envía un informe de errores de Windows para obtener una respuesta en línea de Microsoft y mostrarla al usuario. Normalmente, las respuestas apuntarán al usuario a uno de los tres tipos de recursos:

-   Una actualización del proveedor de la aplicación
-   Sitio web de un proveedor de aplicaciones para obtener más información
-   Un artículo de Microsoft Knowledge Base para obtener más información

**Telemetría para PCA**

Después de que PCA soluciona los problemas de la aplicación en un equipo Windows 8 y obtiene todos los comentarios de los usuarios, recopila datos anónimos sobre la aplicación, el instalador, los problemas detectados y la configuración de compatibilidad aplicada a la aplicación y los envía de vuelta a Microsoft. Estos datos se recopilan de cualquier usuario que esté dispuesto a proporcionar dichos datos anónimos (a través del Programa para la mejora de la experiencia del usuario - CEIP). Una vez recopilados estos datos, se analizan los errores y correcciones de la aplicación y, a continuación, las correcciones se distribuyen a todo el ecosistema de Windows a través del mecanismo de actualización de Windows para que cualquier usuario de la aplicación en el futuro se beneficia automáticamente de la corrección.

**Controles administrativos y administración de la configuración de PCA**

Los administradores de TI pueden controlar el comportamiento de PCA de dos maneras:

-   **Desactivar PCA:** esta configuración permite a los administradores de TI desactivar los cuadros de diálogo que PCA muestra a los usuarios; PCA seguirá controle y detectará problemas y enviará telemetría de vuelta.
-   **Desactivar telemetría de aplicaciones:** esta configuración desactivará cualquier recopilación y envío de datos de telemetría por PCA
    > [!Note]  
    > Si ceip está desactivado, esta configuración no tiene ningún impacto.

     

**Diseño de aplicaciones para trabajar con PCA**

Los desarrolladores deben asegurarse de que sus aplicaciones funcionarán bien en todos los escenarios de compatibilidad descritos anteriormente. Los desarrolladores deben probar y validar sus aplicaciones para cada uno de los escenarios anteriores y asegurarse de que no haya ningún problema de compatibilidad. Si se identifican problemas de compatibilidad, los desarrolladores deben realizar las correcciones necesarias en sus aplicaciones para asegurarse de que se resuelve el problema de compatibilidad. Algunas de las correcciones comunes que los desarrolladores deben realizar incluyen:

-   Eliminación Windows de versiones del sistema operativo durante la instalación y el tiempo de ejecución
-   Eliminación de la comprobación de privilegios (comprobación del acceso de administrador); usar el manifiesto EXE para declarar el nivel correcto de privilegios necesarios
-   Asegúrese de que Windows archivos binarios no se envían en el instalador de la aplicación
-   Eliminación de la escritura en áreas protegidas (registro, carpetas) o escritura en archivos protegidos
-   Firmar digitalmente todos los archivos binarios (archivos EXE, DLL, SYS)
-   En el caso de los instaladores, asegúrese de que se agrega la entrada "Agregar o quitar programas"; como mínimo, esta entrada de metadatos de aplicación debe incluir el nombre de la aplicación, el publicador, la cadena de versión y el idioma admitido. Esto indicará al PCA que el instalador se completó correctamente y también proporcionará una manera cómoda para que los usuarios desinstale la aplicación.

Asegurarse de que la sección TRUSTINFO y COMPATIBILITY del manifiesto de la aplicación (ejecutable) se actualiza como se muestra en la guía de compatibilidad de Windows 8 le permitirá al PCA saber que la aplicación se diseñó para Windows 8 y también garantizará que la aplicación siempre se ejecute de forma nativa sin ningún modo de compatibilidad aplicado a ella.

Para asegurarse de que PCA considera que la aplicación está diseñada para Windows 8:

-   Todas las ESE (instalador o tiempo de ejecución) deben manifiestose para las secciones TRUSTINFO y COMPATIBILITY para Windows 8
-   El instalador debe agregar una entrada "Agregar o quitar programas".

**Glosario**

Los modos de compatibilidad utilizados por PCA se enumeran a continuación con una breve descripción de lo que habilita el modo.



| Mode                         | Descripción                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows7RTM                  | Este modo emula el comportamiento Windows 7, incluido el número de versión 6.1 del sistema operativo.                                                                   |
| WindowsVistaSP2              | Este modo emula el comportamiento Windows 7, incluido el número de versión 6.1 del sistema operativo.                                                                   |
| WindowsXPSp3                 | Este modo emula el comportamiento Windows XP SP3, incluido el número de versión 5.1 del sistema operativo. Esto también incluye el modo RUNASHIGHEST                    |
| RUNASHIGHEST                 | Este modo solicita al usuario que ejecute la aplicación con el privilegio más alto disponible. Los usuarios con privilegios administrativos verán una solicitud de elevación de UAC para la aplicación. |
| RUNASADMIN                   | Este modo siempre solicita al usuario que ejecute la aplicación con privilegios administrativos. las aplicaciones con este modo siempre recibirán el símbolo del sistema de elevación de UAC                    |
| ELEVATECREATEPROCESS         | Este modo hace que los procesos secundarios de la aplicación principal se ejecuten con privilegios administrativos; los procesos secundarios obtienen un cuadro de diálogo de elevación de UAC                          |
| PINDLL                       | Este modo obliga a que un archivo DLL esté en memoria para una aplicación incluso si la aplicación descarga el archivo DLL.                                                                                |
| DISABLEUSERCALLBACKEXCEPTION | Este modo intercepta las excepciones de llamada de usuario y permite que la aplicación continúe sin tener que controlar la excepción.                                          |
| VIRTUALIZEDELETE             | Este modo intercepta las operaciones de eliminación en archivos protegidos e impide que las aplicaciones generen errores debido a excepciones no controladas de la operación de eliminación.                   |
| WRPMITIGATION                | Este modo devuelve un resultado correcto cuando una aplicación intenta escribir, modificar o eliminar Windows archivos protegidos o entradas del Registro (sin completar realmente la operación).  |
| DXMAXIMIZEDWINDOWEDMODE      | Este modo identifica las aplicaciones que van al modo de pantalla completa y las redirige a un modo de ventana maximizado.                                                          |
| HIGHDPIAWARE                 | Este modo permite al resto de Windows saber que la aplicación es compatible con valores altos de PPP y ayuda a representar correctamente los elementos de la interfaz de usuario, el texto, la fuente, etc.                              |



 

 

 