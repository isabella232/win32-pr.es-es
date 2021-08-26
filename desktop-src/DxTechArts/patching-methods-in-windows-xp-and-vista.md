---
title: Aplicación de revisiones a Game Software Windows XP, Windows Vista y Windows 7
description: En este artículo se examinan algunos métodos de aplicación de revisiones que funcionarán bien en Windows Vista y Windows 7, así como Windows XP.
ms.assetid: 27be805a-bffd-a9f8-2207-2a9a4822ba48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91dae9b3bc91c96006f3b2117093962ee485db948fd983191f2db3c7f88fb33a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042505"
---
# <a name="patching-game-software-in-windows-xp-windows-vista-and-windows-7"></a>Aplicación de revisiones a Game Software Windows XP, Windows Vista y Windows 7

Windows Vista y Windows 7 tienen una serie de características para que el sistema operativo sea más seguro. La seguridad agregada significa que aplicar revisiones al software no es tan sencillo como en el pasado. En este artículo se examinan algunos métodos de aplicación de revisiones que funcionarán bien en Windows Vista y Windows 7, así como Windows XP.

Hay dos categorías principales de juegos que requieren revisiones:

-   Juegos que solo requieren revisiones ocasionales, como la mayoría de los juegos sin conexión.
-   Juegos que requieren revisiones frecuentes, como la mayoría de los juegos en línea.

En este artículo también se ofrece una breve introducción al Control de cuentas de usuario (UAC) para servir de fondo sobre los derechos que los desarrolladores pueden esperar que los usuarios tengan en Windows Vista y Windows 7.

-   [Control de cuentas de usuario](#user-account-control)
-   [Juegos que requieren solo revisiones ocasionales](#games-that-require-only-occasional-patches)
    -   [Método 1: Usar el Windows para revisiones ocasionales](#method-1-use-windows-installer-for-occasional-patches)
    -   [Método 2: Requerir derechos de administrador para aplicar revisiones](#method-2-require-administrator-rights-to-apply-patches)
-   [Juegos que requieren revisiones frecuentes](#games-that-require-frequent-patches)
    -   [Método 3: Instalación por usuario](#method-3-install-per-user)
    -   [Método 4: Instalar en una ubicación de Per-Computer común](#method-4-install-to-a-common-per-computer-location)
    -   [Otras posibilidades](#other-possibilities)
-   [Resumen](#summary)

## <a name="user-account-control"></a>Control de cuentas de usuario

Windows Vista y Windows 7 tienen dos tipos principales de cuentas de usuario: Usuario estándar y Administrador. Una cuenta de usuario estándar tiene varias restricciones de acceso; por ejemplo, no puede escribir datos en el sistema de archivos en %SystemDrive% Archivos de programa o en el Registro en \\ la máquina local de HKEY. \_ \_ Esto tiene implicaciones para aplicar revisiones a un juego si se instala en una ubicación de solo lectura. A diferencia de Windows XP, la cuenta de usuario estándar es mucho más común en Windows Vista y Windows 7. Las cuentas de usuario estándar también son necesarias para características importantes del sistema operativo, como los controles parentales. Los controles parentales requieren que la cuenta secundaria sea Usuario estándar y elevar dicha cuenta al Administrador para incluso un juego impide que los controles parentales funcionen con todos los demás juegos. Por lo tanto, es importante que los juegos se diseñe para el usuario estándar.

Windows Vista y Windows 7 tienen un modelo más reciente para los derechos de usuario, para ayudar a evitar que los usuarios ejecuten programas que intenten realizar operaciones que el usuario no pretende ni autoriza. Con ese fin, el control de cuentas de usuario (anteriormente denominado Cuenta de usuario con privilegios mínimos o LUA) permite a los usuarios operar el equipo con derechos de bajo nivel la mayoría de las veces, a la vez que pueden ejecutar fácilmente aplicaciones que requieren derechos de nivel superior, cuando sea necesario. Esto significa que las cuentas de usuario estándar y las cuentas de administrador ejecutan aplicaciones con derechos de usuario estándar, pero solo las cuentas de administrador tienen la capacidad de conceder derechos elevados a las aplicaciones. El sistema operativo solicita a los usuarios el consentimiento explícito de las cuentas de administrador antes de ejecutar una aplicación con derechos elevados y, si un programa que requiere derechos de administrador se ejecuta en una cuenta de usuario estándar, el sistema solicita la aprobación del administrador.

## <a name="games-that-require-only-occasional-patches"></a>Juegos que requieren solo revisiones ocasionales

Algunos juegos solo requieren algunas revisiones a lo largo de su ciclo de vida. Dos métodos que puede emplear para esta frecuencia de aplicación de revisiones son distribuir revisiones como paquetes del instalador de Windows, que generalmente no requieren derechos de administrador, o usar algún otro tipo de distribución que modifique directamente los archivos de juego.

> [!Note]  
> Independientemente de si un juego requiere revisiones frecuentes, las aplicaciones normalmente requieren derechos de administrador para instalarse o quitarse.

 

### <a name="method-1-use-windows-installer-for-occasional-patches"></a>Método 1: Usar el Windows para revisiones ocasionales

En este método, se usa Windows Installer para instalar un paquete (archivo .msi) y se distribuye una revisión del instalador de Windows (archivo .msp) para instalar revisiones. El paquete debe tener una tabla MsiPatchCertificate y la revisión debe estar firmada digitalmente por un certificado de la tabla. Puede encontrar más información sobre la firma digital en [Authenticode Signing for Game Developers (Firma de Authenticode para desarrolladores de juegos).](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

Puede encontrar más detalles y requisitos para usar este método de aplicación de revisiones en la documentación Windows Installer:

-   [Aplicación de revisiones y actualizaciones](/windows/desktop/Msi/patching-and-upgrades)
-   [Revisión de Control de cuentas de usuario (UAC)](/windows/desktop/Msi/user-account-control--uac--patching)

La desventaja de este método es que si el juego no se instaló desde medios extraíbles en Windows XP, la aplicación de revisiones requiere derechos de administrador. Sin embargo, esto no probablemente sea demasiado restrictivo, ya que la mayoría de los usuarios administradores de Windows XP y la restricción al software instalado desde medios extraíbles no están presentes en Windows Vista.

La principal ventaja de este método es que las revisiones se pueden aplicar mediante una cuenta de usuario estándar sin necesidad de solicitar ni autenticación para derechos elevados. Esto proporciona una mejor experiencia de usuario, ya que para jugar a un juego, un usuario con una cuenta de usuario estándar no necesita pedir a alguien con una cuenta de administrador que instale la revisión o que proporcione derechos de administrador permanentes a la cuenta de usuario estándar.

Es posible que este método funcione para juegos que requieren revisiones frecuentes, pero la sobrecarga de usar paquetes del instalador de Windows, en términos de integración de compilación y compatibilidad con un gran número de archivos, puede hacer que este método sea menos deseable que otros.

### <a name="method-2-require-administrator-rights-to-apply-patches"></a>Método 2: Requerir derechos de administrador para aplicar revisiones

En este método, el archivo ejecutable que aplica la revisión requiere derechos de administrador para ejecutarse. Con los derechos de administrador, el ejecutable de aplicación de revisiones puede modificar directamente los archivos de juego ubicados en %SystemDrive% \\ Archivos de programa.

La ventaja de este método es su simplicidad. Sin embargo, este método no es adecuado si el juego necesita revisiones frecuentes, porque si un usuario con una cuenta de usuario estándar quiere jugar a un juego que requiere revisiones frecuentes, como un juego en línea multi player masivo, ese usuario tiene dos opciones:

-   Obtenga un administrador para iniciar sesión y aplicar revisiones al juego, lo que podría ser inconveniente para ambas partes.
-   Tener su cuenta permanentemente elevada con derechos de administrador.

> [!Note]  
> Esta última solución no solo debilite la seguridad del sistema en su conjunto, sino que impide que funcionen características importantes, como los controles parentales.

 

Al implementar este método, el archivo ejecutable que aplica la revisión debe ser diferente del ejecutable del juego. El manifiesto del ejecutable de aplicación de revisiones debe especificar requireAdministrator para requestedExecutionLevel para denotarlo como una aplicación que requiere derechos de administrador. Puede encontrar más información sobre cómo [](/previous-versions/dotnet/articles/aa480150(v=msdn.10))hacerlo en Procedimientos recomendados y directrices para desarrolladores para aplicaciones en un entorno con privilegios mínimos, en "Esquema de manifiesto de aplicación".

Cuando se usa este método, incluso con la configuración del manifiesto, es posible que el archivo ejecutable se pueda iniciar sin derechos de administrador en dos casos:

-   Si el sistema operativo está Windows XP y la cuenta del usuario es un usuario restringido.
-   Si el sistema operativo está Windows Vista o Windows 7, la cuenta del usuario es un usuario estándar y UAC está deshabilitado.

Ambos son escenarios de consumidor poco frecuentes. Sin embargo, el patcher debe hacer que el manifiesto requiera derechos de administrador y debe llamar a [**IsUserAnAdmin**](/windows/desktop/api/shlobj_core/nf-shlobj_core-isuseranadmin); Si esta función devuelve FALSE, se muestra el mensaje de error "Se requieren derechos de administrador".

En general, el método 1 es preferible para los juegos que necesitan solo algunas revisiones a lo largo de su duración.

## <a name="games-that-require-frequent-patches"></a>Juegos que requieren revisiones frecuentes

Muchos juegos basados en Internet se mejoran continuamente y normalmente requieren revisiones periódicas. Para estos juegos, se podrían aplicar revisiones por usuario o por equipo, como se describe en los temas siguientes. Otras posibles soluciones incluyen la modificación de la ACL que protege %SystemDrive% archivos de \\ programa o la creación de un servicio personalizado.

### <a name="method-3-install-per-user"></a>Método 3: Instalación Per-User

Un enfoque recomendado y sencillo es instalar todo el juego en una subcarpeta por usuario de la carpeta de datos de la aplicación local, que puede encontrar mediante una llamada a [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con CSIDL \_ LOCAL \_ APPDATA. Una ruta de acceso de ejemplo es C: Documents y Configuración nombre de usuario \\ Local Configuración Application Data \\ \\ \\ \\ ExampleGame. Esta ubicación permite que una aplicación que se ejecuta con derechos de usuario estándar modifique directamente los archivos de juego.

Sin embargo, este enfoque tiene una desventaja cuando un equipo tiene varios usuarios: cada usuario tiene instalada una copia del juego y cada usuario debe descargar y aplicar las revisiones. Esto no solo pierde el tiempo y el espacio en disco de los usuarios, sino que también aumenta el uso del ancho de banda de red en el servidor que proporciona revisiones. Además, dado que cualquier aplicación con derechos de usuario estándar puede modificar el juego, los ejecutables del juego están menos protegidos; Es decisión del fabricante del juego decidir si esto es aceptable o no.

### <a name="method-4-install-to-a-common-per-computer-location"></a>Método 4: Instalar en una ubicación de Per-Computer común

Otro método consiste en instalar los datos de juego no ejecutables en un subdirectorio de la ruta de acceso especificada por [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) CSIDL COMMON APPDATA; una ruta de acceso de ejemplo es \_ \_ C: \\ Documents y Configuración All Users Application Data \\ \\ \\ ExampleGame. Se trata de una ubicación compartida para todos los usuarios y se puede modificar mediante aplicaciones que se ejecutan con derechos de usuario estándar. Este método minimiza la necesidad de volver a aplicar revisiones grandes cuando se reproduce el juego desde más de una cuenta. Los archivos ejecutables para el juego deben mantenerse en %SystemDrive% Archivos de programas para minimizar el riesgo para otras \\ cuentas del sistema. Los archivos ejecutables deben comprobar la integridad del nuevo contenido en el directorio compartido, ya que esa ubicación la puede modificar un programa o una persona con derechos de usuario estándar. considere la posibilidad [**de usar MapFileAndCheckSum para**](/windows/desktop/api/imagehlp/nf-imagehlp-mapfileandchecksuma) calcular una suma de comprobación de los archivos.

Este método tiene la ventaja de funcionar igualmente bien en Windows XP y Windows Vista, y no requiere derechos de administrador.

### <a name="other-possibilities"></a>Otras posibilidades

Fuera de los métodos ya analizados, otra posibilidad es modificar la ACL de %SystemDrive% Program Files Game Folder al instalar el juego para que una herramienta de revisión pueda escribir directamente en los archivos del juego incluso cuando se ejecute con derechos de usuario \\ \\ \\ estándar. Aunque esto no es difícil, omite la protección de seguridad que ofrece el sistema a los archivos del juego y proporciona una oportunidad para que los programas malintencionados modifiquen el contenido del directorio. Esto no es aconsejable y se recomienda encarecidamente que se utilice una alternativa en su lugar.

Una posibilidad final es escribir un servicio personalizado. En general, escribir un servicio personalizado para aplicar revisiones a los juegos no es una buena idea, ya que hacerlo es complicado y propenso a errores. Se recomienda que la aplicación de revisiones se haga mediante otros métodos que se deban tratar en este artículo. Sin embargo, es posible que sea necesario un servicio personalizado cuando se combina con soluciones antisegráfilo o contra la piratería. Este servicio debe admitir un gran número de juegos y diseñarse para que solo pueda descargar los archivos de revisión y escribir solo en el directorio de instalación del juego de destino. Es importante que el servicio sea pequeño, que tenga un área expuesta mínima que sea vulnerable a ataques y que use el menor número posible de recursos del sistema cuando el juego no se esté ejecutando.

## <a name="summary"></a>Resumen

En última instancia, es usted quien decide qué método implementar. Debe sopesar los factores que son importantes para usted. La seguridad, la frecuencia de aplicación de revisiones, la facilidad de uso por parte del cliente, la carga de trabajo necesaria para implementar, la complejidad de la solución y el cumplimiento de las características de la plataforma son los factores que cada desarrollador debe tener en cuenta antes de decidir un método determinado.

Puede encontrar más información sobre la protección de cuentas de usuario en Windows Requisitos de desarrollo de aplicaciones de Vista para el control de cuentas de usuario [(UAC).](/previous-versions/aa905330(v=msdn.10))

 

 