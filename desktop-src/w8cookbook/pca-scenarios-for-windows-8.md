---
title: Escenarios del Asistente para la compatibilidad de programas para Windows 8
description: Escenarios del Asistente para la compatibilidad de programas para Windows 8
ms.assetid: C61BF746-63EE-4F4E-81D3-52947FD4954D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebada2ca5115d24f260808a1c9ae899963184a8
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104550802"
---
# <a name="program-compatibility-assistant-scenarios-for-windows-8"></a>Escenarios del Asistente para la compatibilidad de programas para Windows 8

## <a name="platforms"></a>Plataformas

**Clientes** : Windows XP Windows \| vista Windows 7 Windows \| \| 8  

## <a name="description"></a>Descripción

Asistente para la compatibilidad de programas (PCA) es una característica de Windows 8 que ayuda a los usuarios finales a ejecutar aplicaciones de escritorio diseñadas para versiones anteriores de Windows. Windows 8 tiene una gran compatibilidad de aplicaciones integrada que permite que las aplicaciones diseñadas para Windows 7 o versiones anteriores de Windows funcionen de forma automática en Windows 8. Sin embargo, hay un pequeño número de aplicaciones que pueden tener problemas para ejecutarse sin intervención.

Cuando un usuario ejecuta una aplicación, PCA realiza un seguimiento de la aplicación e identifica los síntomas de ciertos problemas de compatibilidad conocidos en Windows 8. Cuando detecta síntomas de problemas, proporciona al usuario una oportunidad para aplicar una corrección recomendada que le ayudará a ejecutar mejor la aplicación en Windows 8.

## <a name="scenarios"></a>Escenarios

PCA realiza un seguimiento de las aplicaciones para un conjunto de problemas de compatibilidad conocidos en Windows 8. PCA realiza un seguimiento de los problemas, identifica las correcciones y proporciona al usuario un cuadro de diálogo con instrucciones para aplicar una corrección recomendada. El usuario puede decidir si desea aplicar las correcciones recomendadas o no hacer nada y cancelar la recomendación. Si el usuario se cancela, PCA dejará de realizar un seguimiento de esa aplicación.

Normalmente, PCA aplica uno de los tres modos de compatibilidad de Windows: Windows XP SP3, Windows Vista SP2 o Windows 7, dependiendo de Cuándo se creó el programa (o su configuración). PCA usa los \_ atributos de fecha de vínculo y de versión del subsistema del programa y las secciones de compatibilidad y TRUSTINFO del manifiesto del archivo ejecutable para determinar cuál de los modos es relevante y se aplica a Windows XP SP3 (incluye privilegios administrativos), Windows Vista SP2 o Windows 7, respectivamente. Un glosario al final del documento muestra cada uno de los modos de compatibilidad que PCA aplica y su descripción.

En todos los escenarios que se enumeran a continuación, PCA realiza un seguimiento de las aplicaciones por segunda vez después de aplicar una corrección. Si la aplicación sigue produciendo un error de la misma manera incluso después de aplicar una corrección de compatibilidad, PCA revierte la corrección. A continuación, PCA dejará permanentemente el seguimiento de la aplicación específica que produjo un error.

Aunque PCA realiza un seguimiento de muchos problemas potenciales, no todos los problemas provocarán errores en la aplicación. PCA solo recomienda correcciones en situaciones en las que existe una alta probabilidad de que el error de aplicación se deba a motivos de compatibilidad de Windows. Las secciones siguientes se expanden en cada uno de los escenarios de PCA desarrollados en Windows 8. En cada sección se describe el escenario de problemas y las recomendaciones que PCA proporciona para permitir que la aplicación siga funcionando correctamente en Windows 8.

Para obtener más información sobre los cambios de compatibilidad en Windows 8, consulte los otros temas de la *Guía de compatibilidad de Windows 8*.

Los escenarios en los que PCA realiza un seguimiento y recomiendan correcciones son:

-   No se puede instalar o desinstalar la aplicación
-   La aplicación no se puede ejecutar con un mensaje de comprobación de la versión de Windows
-   No se puede iniciar la aplicación debido a un privilegio administrativo
-   La aplicación se bloquea debido a problemas de memoria específicos
-   Se produce un error en la aplicación debido a que los archivos del sistema no coinciden
-   Se produce un error en la aplicación debido a errores no controlados en Windows de 64 bits
-   Se produce un error en la aplicación al intentar eliminar archivos protegidos que no son de Windows
-   Se produce un error en la aplicación al intentar modificar archivos de Windows
-   Se produce un error en la aplicación debido a que usa modos de color de 8 o 16 bits
-   Se produce un error en la aplicación debido a gráficos y problemas de visualización
-   La aplicación no puede declarar el reconocimiento de PPP
-   Se produce un error en la aplicación debido a que faltan características de Windows
-   Se produce un error en la aplicación debido a controladores no firmados en Windows 8 de 64 bits
-   Seguimiento de aplicaciones instaladas mediante la configuración de compatibilidad
-   La aplicación no puede iniciar instaladores o actualizadores
-   Instaladores de aplicaciones que necesitan ejecutarse con privilegios administrativos
-   Applets heredados del panel de control que necesitan ejecutarse con privilegios administrativos

Cada uno de estos escenarios se expande a continuación:

**No se puede instalar o desinstalar la aplicación**

Uno de los tipos más comunes de errores de aplicación se produce durante la instalación de la aplicación. Los programas de instalación más antiguos no se suelen realizar de dos maneras:

-   El programa de instalación no es consciente de las características del control de cuentas de usuario (UAC) de Windows 8, por lo que es posible que no se ejecute con los privilegios completos necesarios para realizar cambios del sistema en las áreas protegidas de Windows 8.
-   El programa de instalación comprueba la versión de Windows y se bloquea para que no se ejecute si la versión es mayor de lo que espera.

Estas condiciones de error son dos de los tipos más comunes de errores de compatibilidad en el programa de instalación. PCA, con la ayuda de otros componentes de Windows, como UAC, detecta programas de instalación en el inicio y realiza un seguimiento de ellos hasta el final de la instalación. Si el programa de instalación no puede Agregar archivos o si desea agregar una entrada válida en la parte "Agregar o quitar programas" del panel de control de Windows, PCA considerará que el programa de instalación ha producido un error.

En este caso, PCA recomienda un modo de compatibilidad adecuado para la aplicación. El modo de compatibilidad permite que el programa de instalación se ejecute en el modo de Windows para el que se diseñó y también garantiza que la aplicación se ejecute con privilegios de administrador. PCA aplica el modo de compatibilidad RUNASADMIN junto con el modo de compatibilidad de Windows XP, Windows Vista o Windows 7 adecuado. El usuario, al final de la instalación con errores, verá un cuadro de diálogo con la recomendación de PCA:

![cuadro de diálogo no se puede instalar o desinstalar la aplicación](images/pcafigure1.png)

El usuario puede elegir:

-   Ejecute el programa con la configuración de compatibilidad (opción recomendada), después de la cual PCA aplicará la configuración recomendada (modo de compatibilidad), reiniciará el programa de instalación y realizará un seguimiento hasta que la instalación se complete correctamente.
-   Indicar que el programa se instaló correctamente, en cuyo caso PCA no agregará ninguna configuración y dejará de realizar el seguimiento de la configuración.
-   Haga clic en cerrar, en cuyo caso PCA no agregará ninguna configuración y dejará de realizar el seguimiento de esta configuración.

El mismo mecanismo se usa para ayudar a la desinstalación de la aplicación cuando un usuario intenta desinstalar la aplicación desde la sección ' Agregar o quitar programas ' de Windows o desde el acceso directo de desinstalación de la aplicación.

**La aplicación no se puede ejecutar con un mensaje de comprobación de la versión de Windows**

Uno de los errores de compatibilidad más comunes en el tiempo de ejecución de la aplicación es debido a la comprobación de la versión de Windows. Muchas aplicaciones, en el momento del inicio, comprueban la versión de Windows. Si no reconocen la versión, se bloquean, incluso si la aplicación podría haberse ejecutado sin problemas.

Por lo general, estas comprobaciones se asocian con dos condiciones que el PCA sigue:

La aplicación muestra un cuadro de mensaje que advierte al usuario. A continuación se muestra un ejemplo:

![la aplicación no se puede ejecutar con un cuadro de diálogo de mensaje de comprobación de la versión de Windows](images/pcafigure2.png)

-   La aplicación finaliza inmediatamente o se bloquea

Si PCA identifica ambas condiciones para una aplicación, le proporcionará una recomendación al usuario. PCA permitirá al usuario volver a ejecutar la aplicación con la configuración de compatibilidad. PCA aplicará el modo de compatibilidad de Windows XP, Windows Vista o Windows 7 adecuado en función de la aplicación. Como en cualquiera de los escenarios, el usuario puede indicar al PCA que la aplicación se ejecutó correctamente o dejar de usar la configuración recomendada haciendo clic en el botón Cerrar. A continuación se proporciona un cuadro de diálogo de ejemplo:

![la aplicación no se puede ejecutar con un cuadro de diálogo de opción de mensaje de comprobación de versión de Windows](images/pcafigure3.png)

**La aplicación no se puede iniciar o ejecutar debido a un privilegio administrativo**

Algunas aplicaciones necesitan privilegios administrativos para ejecutar y ejecutar su funcionalidad. Sin embargo, en Windows 8, similar a Windows 7 y Windows Vista, las aplicaciones se ejecutan en niveles de privilegios inferiores de forma predeterminada debido a UAC. Las aplicaciones más recientes diseñadas para Windows Vista y versiones posteriores declararán, por lo general, el nivel de privilegio que necesitan para ejecutarse en mediante la sección TRUSTINFO del manifiesto de EXE. Sin embargo, las aplicaciones anteriores suelen producir errores de dos maneras:

-   La aplicación muestra un mensaje al usuario que requiere privilegios administrativos, como se muestra a continuación:

![la aplicación no se puede iniciar o ejecutar debido a un cuadro de diálogo de privilegios administrativos](images/pcafigure4a.png)

-   La aplicación finaliza inmediatamente o se bloquea

Si PCA identifica ambas condiciones para una aplicación, le proporcionará una recomendación al usuario. PCA permitirá al usuario volver a ejecutar la aplicación con privilegios administrativos (PCA aplica el modo de compatibilidad RUNASHIGHEST). El usuario obtendrá un aviso de UAC cuando se vuelva a ejecutar la aplicación. Como en cualquiera de los escenarios, el usuario puede elegir volver a ejecutar con la configuración recomendada o dejar de usar la configuración recomendada haciendo clic en cerrar. A continuación se proporciona un cuadro de diálogo de ejemplo:

![la aplicación no se puede iniciar o ejecutar debido a un cuadro de diálogo de opciones de privilegio administrativo](images/pcafigure5.png)

**La aplicación se bloquea debido a problemas de memoria específicos**

Algunas aplicaciones se bloquean debido a un problema conocido en la memoria. La aplicación desreferencia una DLL de la memoria y, a continuación, llama a una función para ejecutar el código en el mismo archivo DLL. Esto provoca un bloqueo inmediato de la aplicación. Aunque este problema no se debe a los cambios de compatibilidad de Windows 8, se trata de un problema relativamente común en una amplia variedad de aplicaciones. PCA realiza un seguimiento de este problema para proporcionar a los usuarios la oportunidad de ejecutar su aplicación de forma más confiable.

Para estas aplicaciones, PCA aplica automáticamente el modo de compatibilidad de PINDLL de forma silenciosa. El modo de compatibilidad invocado por PCA evita que la aplicación libere el archivo DLL de la memoria. Por lo tanto, la llamada de función en el archivo DLL de la aplicación funcionará, lo que evitará que la aplicación se bloquee y permita que siga funcionando correctamente.

**Se produce un error en la aplicación debido a que los archivos del sistema no coinciden**

Algunas aplicaciones diseñadas para Windows XP y versiones anteriores incluyen copias de archivos DLL del sistema de Windows junto con sus instaladores. Cuando se instalan estas aplicaciones, la aplicación tiene una copia anterior de la DLL en su propia carpeta, así como la versión más reciente del archivo DLL que se encuentra en las carpetas del sistema de Windows.

En Windows Vista y versiones posteriores, esta condición puede hacer que la aplicación genere un error al intentar cargar el archivo DLL local, ya que este archivo DLL no funcionará bien con el resto de los archivos dll actuales del sistema de Windows. Dado que la aplicación generalmente no es consciente de las versiones más recientes de este archivo DLL, no funciona correctamente.

Cuando PCA detecta que el archivo DLL no se cargó correctamente, se aplicará una configuración de compatibilidad que permite a Windows cargar la versión más reciente de la DLL desde la carpeta del sistema de Windows para que la aplicación se ejecute correctamente.

Al final de la primera ejecución con errores de la aplicación, los usuarios verán el cuadro de diálogo PCA que les notifica la configuración aplicada como se indica a continuación:

![error de la aplicación debido a un cuadro de diálogo de archivos de sistema no coincidentes](images/pcafigure6.png)

**Se produce un error en la aplicación debido a errores no controlados en Windows de 64 bits**

En la versión de 64 bits de Windows 8, se ha habilitado una nueva excepción para el mecanismo de devolución de llamada del bucle de mensajes. Aunque esta excepción se presentó por primera vez en Windows 7, no era obligatorio controlar este error. En Windows 8, las aplicaciones que usan bucles de mensajes deben controlar esta nueva excepción. Si no es así, se bloquearán. Las aplicaciones diseñadas para versiones anteriores de Windows pueden no ser conscientes de esta excepción y, por lo tanto, no pueden controlar este error (excepción) correctamente.

PCA detecta las aplicaciones que no se superan debido a este error no controlado y aplica automáticamente el modo de compatibilidad de DISABLEUSERCALLBACKEXCEPTION para la aplicación. Después de aplicar la configuración al final de la ejecución, se notifica al usuario como se indica a continuación. La aplicación obtendrá el modo en la siguiente ejecución y podrá evitar este error.

![se produce un error en la aplicación debido a errores no controlados en el cuadro de diálogo de Windows de 64 bits](images/pcafigure7.png)

**Se produce un error en la aplicación al intentar eliminar archivos protegidos que no son de Windows**

Algunas aplicaciones diseñadas para Windows XP y anteriores suponen que normalmente se ejecutan con privilegios administrativos completos. Como un comportamiento normal de la aplicación, pueden intentar eliminar archivos protegidos que no son de Windows (ya sea en archivos de programa o carpetas de Windows). Cuando se produce un error en la operación de eliminación, muchas de estas aplicaciones pueden bloquearse.

PCA detecta estas aplicaciones que no pueden eliminar los archivos protegidos y se bloquean, y proporciona una recomendación al usuario. PCA permitirá al usuario volver a ejecutar la aplicación con la configuración de compatibilidad. Como en cualquiera de los escenarios, el usuario puede indicar al PCA que la aplicación se ejecutó correctamente o dejar de usar la configuración recomendada haciendo clic en el botón Cerrar. En este caso, PCA aplica el modo de compatibilidad VIRTUALIZEDELETE. A continuación se proporciona un cuadro de diálogo de ejemplo:

![se produce un error en la aplicación al intentar eliminar el cuadro de diálogo archivos protegidos que no son de Windows](images/pcafigure8.png)

**Se produce un error en la aplicación al intentar modificar archivos o claves del registro de Windows**

Algunas aplicaciones diseñadas para Windows XP y anteriores suponen que normalmente se ejecutan con privilegios administrativos completos. Como un comportamiento normal de la aplicación, pueden intentar modificar, eliminar o escribir archivos protegidos de Windows (tanto en archivos de programa o carpetas de Windows) como en claves del registro que pertenecen a Windows. Cuando se produce un error en cualquiera de las operaciones de escritura, eliminación o modificación de un archivo o una clave del registro, muchas de estas aplicaciones pueden bloquearse o producir un error incorrecto.

PCA detecta estas aplicaciones que no pueden escribir en archivos o claves del registro protegidos de Windows y proporciona una recomendación al usuario cuando se cierra la aplicación. PCA permitirá al usuario volver a ejecutar la aplicación con la configuración de compatibilidad. Como en cualquiera de los escenarios, el usuario puede indicar al PCA que la aplicación se ejecutó correctamente o dejar de usar la configuración recomendada haciendo clic en el botón Cerrar. En este caso, PCA aplica el modo de compatibilidad WRPMITIGATION. A continuación se proporciona un cuadro de diálogo de ejemplo:

![se produce un error en la aplicación al intentar modificar el cuadro de diálogo archivos de Windows o claves del registro](images/pcafigure9.png)

**Se produce un error en la aplicación debido a que usa modos de color de 8 o 16 bits**

Como parte de la reversión de Windows 8 para aplicaciones de la tienda Windows, uno de los cambios clave es que el Administrador de ventanas de escritorio (DWM) ahora solo admitirá colores de 32 bits en Windows 8. Ahora se simulan los modos de color inferior.

Muchas aplicaciones y juegos anteriores diseñados para Windows XP o antes de usar los modos de color de 8 o 16 bits. Sin mitigación, estas aplicaciones podrían no ejecutarse en Windows 8. Sin embargo, cuando estas aplicaciones enumeran o intentan usar cualquiera de los modos de color de 8 o 16 bits para la visualización, PCA identifica inmediatamente el problema y con la ayuda de DWM, garantiza que la aplicación funcionará correctamente con el modo de color simulado.

Tenga en cuenta que esto sucede en cuanto la aplicación solicita los modos de color bajo y es transparente para el usuario. El usuario no tiene que reiniciar la aplicación para obtener esta mitigación, ya que esta corrección siempre es necesaria para garantizar que la aplicación funcione correctamente.

**Se produce un error en la aplicación debido a gráficos y problemas de visualización**

Puesto que Administrador de ventanas de escritorio (DWM) siempre está activado en Windows 8, algunas aplicaciones anteriores de Windows XP era pueden producir un error si la aplicación usa API de gráficos de modo mixto, como en el uso de las API de GDI y de DirectX para dibujar en la pantalla (principalmente juegos más antiguos) e intenta usar el modo de pantalla completa:

-   DWM evitará el dibujo directo en el escritorio y se producirá un error en el juego o la aplicación, o bien se dibujará una pantalla negra en el escritorio y no se verá ninguno de los gráficos.
-   En tales casos, cuando se cierra la aplicación, Windows detecta que la aplicación o el juego tienen un problema con el modo de pantalla completa y aplica el modo de compatibilidad DXMAXIMIZEDWINDOWEDMODE que permite que la aplicación o el juego se ejecuten en un modo de ventana maximizado en lugar de un modo de pantalla completa.
-   Una vez que se aplica la configuración al final de la ejecución, el usuario recibe una notificación por PCA, tal como se muestra a continuación: la aplicación obtendrá el modo de compatibilidad en la siguiente ejecución y se podrá ejecutar correctamente.

![error de la aplicación debido a gráficos y mostrar el cuadro de diálogo problemas](images/pcafigure10.png)

**La aplicación no puede declarar el reconocimiento de PPP**

Otro problema típico de visualización con muchas aplicaciones más antiguas se produce cuando Windows y la aplicación se ejecutan en modo de PPP alto, pero la aplicación no declara su reconocimiento de PPP altos a través de su manifiesto de EXE. Entre los problemas comunes que pueden producirse debido a esta falta de coincidencia en la configuración se recortan los elementos de la interfaz de usuario o el texto y el tamaño de fuente incorrecto. Para obtener más información sobre los problemas, consulte este vínculo [aquí](/previous-versions//dd464660(v=vs.85)).

En tales casos, Windows detecta que la aplicación tiene un reconocimiento de PPP alto y aplica el modo de compatibilidad de HIGHDPIAWARE a la aplicación al final de la primera ejecución. A continuación, PCA informará al usuario sobre este, tal y como se muestra a continuación:

![la aplicación no puede declarar el cuadro de diálogo reconocimiento de PPP](images/pcafigure11.png)

**Se produce un error en la aplicación debido a que faltan características de Windows**

Algunas aplicaciones dependen de las características de Windows que se han quitado desde Windows Vista. Cuando estas aplicaciones intentan cargar los archivos dll o los componentes COM que faltan, no funcionan.

PCA detecta las aplicaciones cuando intentan cargar las características de Windows que faltan y proporciona una recomendación para descargar estos componentes e instalarlos una vez finalizada la aplicación. El usuario puede hacer clic en "obtener ayuda en línea" para encontrar una alternativa o para descargar la característica e instalarla. Si es necesario, el usuario puede elegir no hacer nada haciendo clic en cerrar.

![error de aplicación debido a que falta el cuadro de diálogo características de Windows](images/pcafigure12.png)

**Se produce un error en la aplicación debido a controladores no firmados en Windows 8 de 64 bits**

Windows de 64 bits ha requerido controladores firmados digitalmente (archivos SYS) desde Windows Vista. Sin embargo, las aplicaciones anteriores diseñadas antes del lanzamiento de Windows Vista incluían controladores que no estaban firmados digitalmente. Si se instala un controlador sin firmar, Windows no los cargará. En raras ocasiones, es posible que Windows no se inicie si estos controladores están marcados como controladores en tiempo de arranque.

Algunas aplicaciones anteriores instalan controladores que no están firmados en Windows de 64 bits. Cualquier dispositivo o aplicación que intente usar este controlador puede producir un error o provocar un bloqueo del sistema. Para evitar este tipo de escenario, PCA detecta las aplicaciones cuando instalan controladores sin firmar y deshabilita el controlador que se marca como controlador en tiempo de arranque.

También indica al usuario que adquiera un controlador firmado digitalmente para que la aplicación funcione correctamente. El mensaje se muestra como resultado de la instalación del controlador y como resultado de la instalación de la aplicación. Si otra aplicación instala el mismo controlador, esa aplicación también obtendrá el mismo mensaje.

![se produce un error en la aplicación debido a controladores no firmados en el cuadro de diálogo Windows 8 de 64 bits](images/pcafigure13.png)

**Seguimiento de aplicaciones instaladas mediante la configuración de compatibilidad**

Cuando se produce un error en un instalador, PCA ayuda al instalador con varios modos de compatibilidad según el tipo de error. Una vez que el instalador se ejecuta correctamente con la configuración de compatibilidad, PCA realiza un seguimiento de los accesos directos que agregó el instalador. Esto se hace para realizar el seguimiento si las aplicaciones instaladas también pueden necesitar la configuración de compatibilidad aplicada a su instalador.

Cuando un usuario inicia una aplicación de este tipo, PCA solicita al usuario que le pregunte si la aplicación funcionó correctamente. Si el usuario responde, "sí", el PCA deja de realizar el seguimiento de la aplicación. Si el usuario responde "no", se aplica el mismo modo de compatibilidad que se aplicó al instalador de la aplicación y vuelve a ejecutar la aplicación con el modo de compatibilidad aplicado.

**La aplicación no puede iniciar instaladores o actualizadores**

A veces, las aplicaciones inician programas secundarios que deben ejecutarse como administradores. Este suele ser el caso cuando una aplicación intenta iniciar su software actualizador para comprobar e instalar nuevas actualizaciones en la aplicación. Cuando las aplicaciones ejecutan directamente estos programas secundarios, el programa secundario puede no iniciarse porque la propia aplicación no tenía privilegios administrativos o porque el programa secundario no se marcó correctamente para la elevación con el manifiesto de UAC.

PCA realiza un seguimiento de estos errores y, cuando se cierra la aplicación principal, aplica automáticamente el modo de compatibilidad ELEVATECREATEPROCESS que ayudará a que los programas secundarios se ejecuten correctamente. Cuando la aplicación inicia la aplicación secundaria en las ejecuciones posteriores, el usuario verá un cuadro de diálogo de UAC para el programa secundario.

A continuación se muestra un ejemplo del cuadro de diálogo PCA:

![no se puede iniciar el cuadro de diálogo instaladores o actualizadores en la aplicación](images/pcafigure14.png)

**Instaladores de aplicaciones que necesitan ejecutarse con privilegios administrativos**

Los instaladores de aplicaciones de escritorio de Windows requieren privilegios administrativos ya que escriben archivos, carpetas y entradas del registro en áreas del sistema protegidas. Windows (UAC) tiene lógica de detección para identificar el momento en que se ejecuta un instalador e indica inmediatamente al usuario que proporcione privilegios administrativos a través del cuadro de diálogo de UAC. Sin embargo, en algunos casos, esta lógica no podrá determinar si una aplicación era realmente un instalador y es posible que no obtenga privilegios administrativos. Suelen ser instaladores personalizados que no usan tecnologías de instalación conocidas como Windows Installer o instalar Shield.

En tales casos, PCA detecta que el instalador no pudo escribir sus archivos. Al final, si la instalación no se realizó correctamente, PCA le proporcionará una recomendación para aplicar la configuración de compatibilidad. Si el usuario elige hacer clic en "ejecutar programa", PCA aplicará el modo de compatibilidad RUNASADMIN y volverá a ejecutar el instalador. Si el usuario elige cerrar, no se aplicará ninguna configuración. A continuación se muestra un cuadro de diálogo PCA de ejemplo:

![Captura de pantalla que muestra un ejemplo de un cuadro de diálogo de un instalador de la aplicación que necesita ejecutarse con privilegios administrativos.](images/pcafigure15.png)

Los subprogramas heredados del panel de control que necesitan ejecutarse con el panel de control privilegios administrativos, generalmente cambian la configuración del sistema y necesitan la capacidad de ejecutar el administrador de ad. Sin embargo, los escritos antes de Windows Vista no tienen un manifiesto EXE o no tienen la sección TRUSTINFO que declara el nivel de privilegios que requieren. Cuando se ejecutan tales applets, PCA los detecta y, al final de la primera ejecución, proporciona una recomendación para ejecutar con la configuración administrativa. Si el usuario elige hacer clic en "ejecutar programa", PCA aplica el modo de compatibilidad de RUNASADMIN y vuelve a ejecutar el instalador. Si el usuario elige cerrar, no se aplicará ninguna configuración. A continuación se muestra un cuadro de diálogo PCA de ejemplo:

![instaladores de aplicaciones que necesitan ejecutarse con el cuadro de diálogo privilegios administrativos](images/pcafigure16.png)

**Comprobar la configuración recomendada a través de los comentarios del usuario**

Al final de cada uno de los escenarios (después de que la aplicación se ejecute con la configuración de compatibilidad recomendada), PCA le pedirá al usuario una pregunta sencilla:

![comprobación de la configuración recomendada mediante el cuadro de diálogo comentarios del usuario](images/pcafigure17.png)

El usuario puede proporcionar comentarios si la aplicación funcionó o no con la configuración de compatibilidad. Estos datos se enviarán de forma anónima a Microsoft. Esto ayuda a garantizar que estas correcciones se puedan integrar en Windows 8 a través del proceso de Windows Update, de modo que los futuros usuarios de Windows 8 ya no se encuentren en el error de aplicación y PCA ya no necesitará realizar un seguimiento de la aplicación para el error.

**Seguimiento de problemas que no tienen ninguna recomendación**

Las aplicaciones pueden producir errores de muchas formas diferentes por motivos de compatibilidad. PCA realiza un seguimiento de muchos más problemas de compatibilidad que los que se enumeran en los escenarios anteriores. En estos casos, muchas veces, la manifestación del problema depende de la aplicación. Esto significa que algunas aplicaciones controlan estos problemas correctamente y se recuperan de él, mientras que otros no. Por lo tanto, para estos problemas, mientras PCA sigue realizando un seguimiento de la aplicación, no proporciona una recomendación directa para una corrección.

Los problemas con los que PCA realiza un seguimiento y que no tienen una configuración recomendada o un cuadro de diálogo incluyen aplicaciones que:

-   Tener un tiempo de ejecución muy breve: las aplicaciones se ejecutan durante más de tres segundos
-   Crear objetos de memoria global sin privilegios administrativos
-   Error (excepción Win32) al iniciar
-   Comprobar los privilegios administrativos (pero puede que no se produzcan errores)
-   Usar códecs Indeo (desusados de Windows Vista)
-   Intente escribir o eliminar claves en ubicaciones del registro protegidas como HKLM
-   Bloqueo al iniciar

**Aplicar correcciones a través de la pestaña Compatibilidad y el solucionador de problemas de compatibilidad**

Como se mencionó anteriormente, se puede producir un error en las aplicaciones por diversos motivos de compatibilidad. No todas ellas tienen claras recomendaciones de PCA, ya que la configuración depende de la aplicación. Sin embargo, los usuarios pueden ir al solucionador de problemas de compatibilidad o la pestaña Compatibilidad para aplicar determinadas correcciones comunes para intentar que la aplicación con errores funcione correctamente en Windows 8. En tales casos, PCA seguirá realizando un seguimiento de la aplicación en busca de problemas de compatibilidad, antes y después de aplicar la corrección. Una vez que la aplicación se ejecuta con la corrección aplicada, PCA le pedirá al usuario si la corrección funcionó. Una vez que el usuario responde a la pregunta, los datos se envían de forma anónima a Microsoft a través de la telemetría. Estos datos se recopilan de muchos usuarios y se analizan, y las correcciones calificadas se distribuyen en general a todos los usuarios de Windows 8 a través de Windows Update.

**Usar el solucionador de problemas de compatibilidad**

El solucionador de problemas de compatibilidad es un mecanismo de Windows que le permite diagnosticar problemas con aplicaciones y aplicar correcciones recomendadas para que funcionen correctamente. Esto solo es necesario cuando PCA no proporciona ninguna recomendación para la aplicación.

El solucionador de problemas permite a los usuarios recorrer y responder a un conjunto de preguntas y, en función de las respuestas, aplicarán un conjunto de correcciones y permitirán a los usuarios probar sus aplicaciones y comprobar las correcciones. Una vez comprobado, las correcciones se aplicarán de forma permanente a las aplicaciones para que funcionen mejor en Windows 8.

A continuación se muestra la interfaz de usuario del solucionador de problemas como referencia:

![usar el cuadro de diálogo de solucionador de problemas de compatibilidad](images/pcafigure18.png)

Puede iniciar el solucionador de problemas de compatibilidad de dos maneras:

**Desde la pantalla Inicio:**

1.  Tipo: solucionador de problemas de compatibilidad
2.  En la sección configuración, haga clic en el icono ' ejecutar programas realizados para la versión anterior de Windows '

  
**En el icono de la aplicación:**

1.  En la pantalla Inicio, haga clic con el botón derecho en el icono de la aplicación.
2.  Haga clic en ' abrir Ubicación del archivo ' (solo aplicaciones de escritorio)
3.  En la cinta de opciones del explorador, haga clic en la pestaña "aplicación".
4.  Elija "solucionar problemas de compatibilidad".

  


**Uso de la pestaña Compatibilidad**

Tenga en cuenta que esto solo se recomienda para los usuarios que son expertos en probar la configuración de compatibilidad diferente. Este método no proporciona ninguna recomendación del tipo de corrección que se aplica a las aplicaciones. Aquí se espera que el usuario sepa qué correcciones se pueden aplicar para que la aplicación funcione. Si no está seguro de las correcciones, use el solucionador de problemas de compatibilidad para encontrar una corrección de la aplicación.

Para tener acceso a la pestaña Compatibilidad:

 **Desde la pantalla Inicio:**

1.  Haga clic con el botón derecho en el icono de la aplicación
2.  Abrir ubicación de archivo (solo aplicaciones de escritorio)

  
**Desde la cinta de opciones del explorador:**

1.  Haga clic en propiedades
2.  Vaya a la pestaña Compatibilidad
3.  Selección de las correcciones de compatibilidad
4.  Volver a ejecutar la aplicación
    > [!Note]  
    > Puede volver al mismo lugar para cambiar o quitar también las correcciones. También puede aplicar las correcciones a todos los usuarios del equipo mediante el botón proporcionado en la pestaña.

     

  


![uso de la pestaña Compatibilidad](images/pcafigure19.png)

**Aplicaciones con problemas de compatibilidad conocidos**

Además de los escenarios de detección de problemas en tiempo de ejecución enumerados anteriormente, PCA también informa a los usuarios del inicio de la aplicación si la aplicación tiene problemas de compatibilidad conocidos. La lista se almacena en la base de datos de compatibilidad de aplicaciones del sistema. Hay dos tipos de mensajes:

-   **Mensajes de bloque duro**: si se sabe que la aplicación no es compatible y, si se permite la ejecución de la aplicación, se producirá un impacto grave en el sistema (por ejemplo, un bloqueo de Windows o no se puede arrancar después de la instalación), se mostrará un mensaje de bloqueo como el que se muestra a continuación

![aplicaciones con problemas de compatibilidad conocidos: cuadro de diálogo mensajes de bloque duro](images/pcafigure20.png)

-   **Mensajes de bloque flexible**: Si la aplicación tiene un problema de compatibilidad conocido y es posible que no funcione correctamente, se muestra este mensaje:

![aplicaciones con problemas de compatibilidad conocidos: cuadro de diálogo mensajes de bloqueo de software](images/pcafigure21.png)

En ambos casos, la opción "obtener ayuda en línea" envía un informe de errores de Windows para obtener una respuesta en línea de Microsoft y mostrarla al usuario. Normalmente, las respuestas apuntarán al usuario a uno de los tres tipos de recursos:

-   Una actualización del proveedor de la aplicación
-   Sitio web de un proveedor de la aplicación para obtener más información
-   Un artículo de Microsoft Knowledge base para obtener más información

**Telemetría del PCA**

Una vez que PCA soluciona cualquier problema de la aplicación en un equipo con Windows 8 y obtiene todos los comentarios de los usuarios, recopila datos anónimos sobre la aplicación, el instalador, los problemas detectados y la configuración de compatibilidad aplicada a la aplicación y los envía de vuelta a Microsoft. Estos datos se recopilan de cualquier usuario que esté dispuesto a proporcionar estos datos anónimos (a través del Programa para la mejora de la experiencia del usuario-CEIP). Una vez que se recopilan estos datos, se analizan los errores y las correcciones de la aplicación, y las correcciones se distribuyen a todo el ecosistema de Windows a través del mecanismo de Windows Update para que cualquier usuario de la aplicación en el futuro se beneficie de la corrección automáticamente.

**Controles administrativos y administración de la configuración de PCA**

Los administradores de TI pueden controlar el comportamiento del PCA de dos maneras:

-   **Desactivar PCA** : esta opción permite a los administradores de ti desactivar los cuadros de diálogo que PCA muestra a los usuarios. PCA seguirá realizando un seguimiento de los problemas y los detectará y enviará datos de telemetría.
-   **Desactivar la telemetría** de la aplicación: esta opción desactiva cualquier recopilación y envío de datos de telemetría por PCA.
    > [!Note]  
    > Si el CEIP está desactivado, este valor no tiene ningún impacto.

     

**Diseño de aplicaciones para trabajar con PCA**

Los desarrolladores deben asegurarse de que sus aplicaciones funcionarán bien en todos los escenarios de compatibilidad descritos anteriormente. Los desarrolladores deben probar y validar sus aplicaciones para cada uno de los escenarios anteriores y asegurarse de que no hay problemas de compatibilidad. Si se identifican problemas de compatibilidad, los desarrolladores deben realizar las correcciones de las aplicaciones necesarias para asegurarse de que se resuelve el problema de compatibilidad. Algunas de las correcciones comunes que los desarrolladores deben hacer son:

-   Eliminar comprobaciones de versión del sistema operativo Windows en instalación y tiempo de ejecución
-   Eliminar comprobación de privilegios (comprobar el acceso de administrador); Use el manifiesto de EXE para declarar el nivel correcto de privilegio necesario
-   Asegurarse de que los archivos binarios de Windows no se incluyen en el instalador de la aplicación
-   Eliminar la escritura en áreas protegidas (registro, carpetas) o escritura sobre archivos protegidos
-   Firmar digitalmente todos los archivos binarios (EXE, DLL, SYS)
-   En el caso de los instaladores, asegúrese de que se agrega la entrada "Agregar o quitar programas" adecuada. como mínimo, esta entrada de metadatos de la aplicación debe incluir el nombre de la aplicación, el publicador, la cadena de versión y el idioma admitido. Esto indicará al PCA que el instalador se completó correctamente y también proporcionará a los usuarios una forma cómoda de desinstalar la aplicación.

Asegúrese de que la sección TRUSTINFO y compatibilidad del manifiesto de la aplicación (ejecutable) se actualiza como se muestra en la guía de compatibilidad de Windows 8 indicará al PCA que la aplicación está diseñada para Windows 8 y también garantizará que la aplicación se ejecute siempre de forma nativa sin ningún modo de compatibilidad aplicado.

Para asegurarse de que PCA considera que la aplicación está diseñada para Windows 8:

-   Todos los archivos. exe (instalador o tiempo de ejecución) se deben manifestar en TRUSTINFO y en las secciones de compatibilidad de Windows 8
-   El instalador debe agregar una entrada ' Agregar o quitar programas '

**Glosario**

Los modos de compatibilidad usados por PCA se enumeran a continuación con una breve descripción de lo que habilita el modo.



| Mode                         | Descripción                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows7RTM                  | Este modo emula el comportamiento común de Windows 7, incluido el número de versión del sistema operativo 6,1                                                                   |
| WindowsVistaSP2              | Este modo emula el comportamiento común de Windows 7, incluido el número de versión del sistema operativo 6,1                                                                   |
| WindowsXPSp3                 | Este modo emula el comportamiento común de Windows XP SP3, incluido el número de versión del sistema operativo 5,1. También incluye el modo RUNASHIGHEST                    |
| RUNASHIGHEST                 | Este modo solicita al usuario que ejecute la aplicación con el privilegio más alto disponible. Los usuarios con privilegios administrativos verán una petición de elevación de UAC para la aplicación |
| RUNASADMIN                   | Este modo siempre solicita al usuario que ejecute la aplicación con privilegios administrativos; las aplicaciones con este modo siempre obtendrán la solicitud de elevación de UAC.                    |
| ELEVATECREATEPROCESS         | Este modo hace que los procesos secundarios de la aplicación principal se ejecuten con privilegios administrativos; los procesos secundarios obtendrán un cuadro de diálogo de elevación de UAC                          |
| PINDLL                       | Este modo fuerza que un archivo DLL esté en memoria para una aplicación aunque la aplicación Descargue el archivo DLL                                                                                |
| DISABLEUSERCALLBACKEXCEPTION | Este modo intercepta las excepciones de devolución de llamada del usuario y permite que la aplicación continúe sin tener que controlar la excepción.                                          |
| VIRTUALIZEDELETE             | Este modo intercepta las operaciones de eliminación en archivos protegidos y evita que las aplicaciones generen errores debido a las excepciones no controladas de la operación de eliminación.                   |
| WRPMITIGATION                | Este modo devuelve SUCCESS cuando una aplicación intenta escribir, modificar o eliminar entradas del registro o archivos protegidos de Windows (sin completar realmente la operación)  |
| DXMAXIMIZEDWINDOWEDMODE      | Este modo identifica las aplicaciones que entran en modo de pantalla completa y las redirige a un modo de ventana maximizada.                                                          |
| HIGHDPIAWARE                 | Este modo permite que el resto de Windows sepa que la aplicación tiene un reconocimiento de PPP elevado y ayuda a representar correctamente los elementos de la interfaz de usuario, el texto, la fuente, etc.                              |



 

 

 