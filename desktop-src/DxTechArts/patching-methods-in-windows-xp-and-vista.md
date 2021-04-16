---
title: Aplicar revisiones al software de juegos en Windows XP, Windows Vista y Windows 7
description: En este artículo se examinan algunos métodos de revisión que funcionarán bien en Windows Vista y Windows 7, así como en Windows XP.
ms.assetid: 27be805a-bffd-a9f8-2207-2a9a4822ba48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ae0b1455cae61b8372f81e6928977743084c9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685748"
---
# <a name="patching-game-software-in-windows-xp-windows-vista-and-windows-7"></a>Aplicar revisiones al software de juegos en Windows XP, Windows Vista y Windows 7

Windows Vista y Windows 7 tienen una serie de características para que el sistema operativo sea más seguro. La seguridad agregada significa que la aplicación de revisiones a software no es tan sencilla como lo hacía en el pasado. En este artículo se examinan algunos métodos de revisión que funcionarán bien en Windows Vista y Windows 7, así como en Windows XP.

Hay dos categorías principales de juegos que requieren revisiones:

-   Juegos que requieren solo revisiones ocasionales, como la mayoría de los juegos sin conexión.
-   Juegos que requieren revisiones frecuentes, como la mayoría de los juegos en línea.

En este artículo también se ofrece una breve introducción al control de cuentas de usuario (UAC) para servir de referencia en cuanto a los derechos que los desarrolladores pueden esperar tener en Windows Vista y Windows 7.

-   [Control de cuentas de usuario](#user-account-control)
-   [Juegos que solo requieren revisiones ocasionales](#games-that-require-only-occasional-patches)
    -   [Método 1: usar Windows Installer para revisiones ocasionales](#method-1-use-windows-installer-for-occasional-patches)
    -   [Método 2: requerir derechos de administrador para aplicar revisiones](#method-2-require-administrator-rights-to-apply-patches)
-   [Juegos que requieren revisiones frecuentes](#games-that-require-frequent-patches)
    -   [Método 3: instalación por usuario](#method-3-install-per-user)
    -   [Método 4: instalación en una ubicación de Per-Computer común](#method-4-install-to-a-common-per-computer-location)
    -   [Otras posibilidades](#other-possibilities)
-   [Resumen](#summary)

## <a name="user-account-control"></a>Control de cuentas de usuario

Windows Vista y Windows 7 tienen dos tipos principales de cuentas de usuario: usuario estándar y administrador. Una cuenta de usuario estándar tiene varias restricciones de acceso; por ejemplo, no puede escribir datos en el sistema de archivos en% SystemDrive% \\ archivos de programa o en el registro del \_ equipo local HKEY \_ . Esto tiene implicaciones para aplicar revisiones a un juego si se instala en una ubicación de solo lectura. A diferencia de Windows XP, la cuenta de usuario estándar es mucho más común en Windows Vista y Windows 7. También se requieren cuentas de usuario estándar para características importantes del sistema operativo, como el control parental. Los controles parentales requieren que la cuenta secundaria sea usuario estándar y la elevación de dicha cuenta al administrador para un solo juego impide que los controles parentales trabajen con todos los demás juegos. Por lo tanto, es importante que los juegos se diseñen para usuarios estándar.

Windows Vista y Windows 7 tienen un modelo más reciente para los derechos de usuario, con el fin de evitar que los usuarios ejecuten programas que intenten realizar operaciones que el usuario no desea o autoriza. Para ello, el control de cuentas de usuario (anteriormente conocido como cuenta de usuario con privilegios mínimos o LUA) permite a los usuarios operar el equipo con derechos de bajo nivel la mayor parte del tiempo, a la vez que puede ejecutar fácilmente aplicaciones que requieran derechos de nivel superior, cuando sea necesario. Esto significa que las cuentas de usuario y las cuentas de administrador estándar ejecutan aplicaciones con derechos de usuario estándar, pero solo las cuentas de administrador tienen la capacidad de conceder derechos elevados a las aplicaciones. El sistema operativo pide a los usuarios con cuentas de administrador un consentimiento explícito antes de ejecutar una aplicación con permisos elevados, y si un programa que requiere derechos de administrador se ejecuta en una cuenta de usuario estándar, el sistema solicita la aprobación del administrador.

## <a name="games-that-require-only-occasional-patches"></a>Juegos que solo requieren revisiones ocasionales

Algunos juegos solo requieren algunas revisiones a lo largo de su ciclo de vida. Dos métodos que puede emplear para esta frecuencia de revisión son distribuir revisiones como Windows Installer paquetes, lo que normalmente no requiere derechos de administrador o usar algún otro tipo de distribución que modifique directamente los archivos de juego.

> [!Note]  
> Independientemente de si un juego requiere la aplicación de revisiones frecuentes, las aplicaciones suelen requerir la instalación o eliminación de los derechos de administrador.

 

### <a name="method-1-use-windows-installer-for-occasional-patches"></a>Método 1: usar Windows Installer para revisiones ocasionales

En este método, se usa un Windows Installer para instalar un paquete (archivo. msi) y una revisión de Windows Installer (archivo. msp) para instalar las revisiones. El paquete debe tener una tabla MsiPatchCertificate y la revisión debe estar firmada digitalmente por un certificado de la tabla. Puede encontrar más información sobre la firma digital en [firma Authenticode para desarrolladores de juegos](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

Puede encontrar más detalles y requisitos para usar este método de revisión en la documentación Windows Installer:

-   [Revisiones y actualizaciones](/windows/desktop/Msi/patching-and-upgrades)
-   [Revisión de control de cuentas de usuario (UAC)](/windows/desktop/Msi/user-account-control--uac--patching)

El inconveniente de este método es que si el juego no se instaló desde un medio extraíble en Windows XP, la revisión requiere derechos de administrador. Sin embargo, esto no es probable que sea demasiado restrictivo, ya que la mayoría de los administradores de usuarios en Windows XP y la restricción del software instalado desde medios extraíbles no está presente en Windows Vista.

La principal ventaja de este método es que las revisiones se pueden aplicar mediante una cuenta de usuario estándar sin necesidad de un símbolo del sistema y la autenticación de derechos elevados. Esto proporciona una mejor experiencia de usuario, ya que para jugar un juego, un usuario con una cuenta de usuario estándar no necesita pedir a alguien con una cuenta de administrador que instale la revisión o que proporcione la cuenta de usuario estándar con derechos de administrador permanentes.

Es posible que este método funcione para juegos que requieran revisiones frecuentes, pero la sobrecarga que supone el uso de paquetes Windows Installer, en términos de integración de compilación y compatibilidad con un gran número de archivos, podría hacer que este método sea menos conveniente que otros.

### <a name="method-2-require-administrator-rights-to-apply-patches"></a>Método 2: requerir derechos de administrador para aplicar revisiones

En este método, el archivo ejecutable que aplica la revisión requiere derechos de administrador para ejecutarse. Con derechos de administrador, el ejecutable de aplicación de revisiones puede modificar directamente los archivos de juego ubicados en% SystemDrive% \\ archivos de programa.

La ventaja de este método es su simplicidad. Sin embargo, este método no es adecuado si el juego necesita revisiones frecuentes, ya que si un usuario con una cuenta de usuario estándar desea jugar a un juego que requiere revisiones frecuentes, como un juego en línea de varios jugadores masivo, ese usuario tiene dos opciones:

-   Pida a un administrador que inicie sesión y revise el juego, lo que podría ser inconveniente para ambas partes.
-   Su cuenta se ha elevado de forma permanente con derechos de administrador.

> [!Note]  
> Esta última solución no solo debilita la seguridad del sistema en su conjunto, sino que evita que funcionen características importantes, como los controles parentales.

 

Al implementar este método, el archivo ejecutable que aplica la revisión debe ser diferente del ejecutable del juego. El manifiesto del ejecutable de aplicación de revisiones debe especificar requireAdministrator para requestedExecutionLevel para denotarlo como una aplicación que requiere derechos de administrador. Puede encontrar más información sobre cómo hacerlo en [procedimientos recomendados para desarrolladores e instrucciones para aplicaciones en un entorno con menos privilegios](/previous-versions/dotnet/articles/aa480150(v=msdn.10)), en "esquema de manifiesto de aplicación".

Cuando se usa este método, incluso con la configuración del manifiesto, el archivo ejecutable podría iniciarse sin derechos de administrador en dos casos:

-   Si el sistema operativo es Windows XP y la cuenta del usuario es un usuario restringido.
-   Si el sistema operativo es Windows Vista o Windows 7, la cuenta de usuario es un usuario estándar y UAC está deshabilitado.

Ambos son escenarios de consumidor poco frecuentes. Sin embargo, el aplicador debe tener el manifiesto que requiere derechos de administrador y debe llamar a [**IsUserAnAdmin**](/windows/desktop/api/shlobj_core/nf-shlobj_core-isuseranadmin); Si esta función devuelve FALSE, se muestra el mensaje de error "se requieren derechos de administrador".

En general, el método 1 es preferible para juegos que necesitan solo algunas revisiones durante su duración.

## <a name="games-that-require-frequent-patches"></a>Juegos que requieren revisiones frecuentes

Muchos juegos basados en Internet se están mejorando continuamente y normalmente requieren revisiones normales. En estos juegos, las revisiones se pueden aplicar por usuario o por equipo, como se describe en los temas siguientes. Otras posibles soluciones incluyen la modificación de la ACL que protege los archivos de programa% SystemDrive% \\ o la creación de un servicio personalizado.

### <a name="method-3-install-per-user"></a>Método 3: instalar Per-User

Un enfoque sencillo y recomendado es instalar el juego completo en una subcarpeta por usuario de la carpeta de datos de la aplicación local, que puede encontrar mediante una llamada a [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con CSIDL \_ local \_ appdata. Una ruta de acceso de ejemplo es C: \\ Documents and Settings \\ nombre de usuario \\ configuración local \\ datos de aplicación \\ ExampleGame. Esta ubicación permite que una aplicación que se ejecuta con derechos de usuario estándar modifique directamente los archivos de juego.

Sin embargo, hay un inconveniente de este enfoque cuando un equipo tiene varios usuarios: cada usuario tiene una copia del juego instalado y los usuarios deben descargar y aplicar las revisiones. Esto no solo desperdicia espacio en disco y tiempo de los usuarios, sino que también aumenta el uso de ancho de banda de red para el servidor que proporciona revisiones. Además, dado que cualquier aplicación con derechos de usuario estándar puede modificar el juego, los archivos ejecutables de juegos están menos protegidos. depende del fabricante del juego decidir si esto es aceptable o no.

### <a name="method-4-install-to-a-common-per-computer-location"></a>Método 4: instalación en una ubicación de Per-Computer común

Otro método consiste en instalar los datos de juego no ejecutables en un subdirectorio de la ruta de acceso especificada por [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) CSIDL \_ Common \_ AppData; una ruta de acceso de ejemplo es C: \\ Documents and Settings \\ All Users \\ Application Data \\ ExampleGame. Se trata de una ubicación compartida para todos los usuarios y las aplicaciones que se ejecutan con derechos de usuario estándar pueden modificarla. Este método minimiza la necesidad de volver a aplicar revisiones grandes cuando el juego se reproduce desde más de una cuenta. Los archivos ejecutables del juego deben conservarse en% SystemDrive% \\ Programs files para minimizar el riesgo para otras cuentas del sistema. Los archivos ejecutables deben comprobar la integridad del nuevo contenido en el directorio compartido, ya que la ubicación puede ser modificada por un programa o una persona con derechos de usuario estándar. considere el uso de [**MapFileAndCheckSum**](/windows/desktop/api/imagehlp/nf-imagehlp-mapfileandchecksuma) para calcular una suma de comprobación de los archivos.

Este método tiene la ventaja de que funciona igual de bien en Windows XP y Windows Vista, y no requiere derechos de administrador.

### <a name="other-possibilities"></a>Otras posibilidades

Fuera de los métodos ya descritos, otra posibilidad es modificar la ACL de la carpeta de juegos% SystemDrive% \\ Program Files \\ \\ al instalar el juego para que una herramienta de revisión pueda escribir directamente en los archivos del juego incluso cuando se ejecuta con derechos de usuario estándar. Aunque esto no es difícil, omite la protección de seguridad que ofrece el sistema a los archivos del juego y proporciona una oportunidad para que los programas malintencionados modifiquen el contenido del directorio. Esto no es aconsejable y se recomienda encarecidamente que se utilice en su lugar una alternativa.

Una posibilidad final es escribir un servicio personalizado. En general, escribir un servicio personalizado para aplicar revisiones a los juegos no es una buena idea, ya que hacerlo es complicado y propenso a errores. Se recomienda que la revisión se realice mediante el uso de otros métodos descritos en este artículo. Sin embargo, es posible que sea necesario un servicio personalizado cuando se combina con soluciones antiengaño o antipiratería. Este servicio debe admitir un gran número de juegos y estar diseñado para que solo pueda descargar los archivos de revisión y escribir solo en el directorio de instalación del juego de destino. Es importante que el servicio sea pequeño, tenga un área expuesta mínima que sea vulnerable a los ataques y use el menor número posible de recursos del sistema cuando el juego no se esté ejecutando.

## <a name="summary"></a>Resumen

En última instancia, depende de usted decidir qué método implementar. Debe sopesar los factores que son importantes para usted. La seguridad, la frecuencia de aplicación de revisiones, la facilidad de uso por parte del cliente, la carga de trabajo necesaria para implementar, la complejidad de la solución y el cumplimiento de las características de la plataforma son los factores que cada desarrollador debe tener en cuenta antes de decidir un método determinado.

Puede encontrar más información sobre la protección de cuentas de usuario en [requisitos de desarrollo de aplicaciones de Windows Vista para el control de cuentas de usuario (UAC)](/previous-versions/aa905330(v=msdn.10)).

 

 