---
title: Depurar una extensión de Active Directory
description: La hoja de propiedades del servicio de directorio de Microsoft Active Directory, el menú contextual y las extensiones del Asistente para creación de objetos que se documentan en este tema se implementan como servidores COM en proceso.
ms.assetid: 8c280084-fd2f-4d34-a119-d4e925a68a5c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8d9646f4ccc2e8c740a81ddb48422881744f5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077538"
---
# <a name="debugging-an-active-directory-extension"></a>Depurar una extensión de Active Directory

La hoja de propiedades del servicio de directorio de Microsoft Active Directory, el menú contextual y las extensiones del Asistente para creación de objetos que se documentan en este tema se implementan como servidores COM en proceso. Es decir, cada extensión es un archivo DLL que se ejecuta en el contexto del proceso de host. Para depurar la extensión, es necesario asociar la extensión a una aplicación y ejecutar la aplicación en un depurador.

## <a name="debugging-active-directory-extensions-displayed-in-the-windows-shell"></a>Depurar extensiones de Active Directory mostradas en el shell de Windows

Active Directory extensiones mostradas en el shell de Windows se cargan en el contexto del proceso de Explorer.exe. Estas extensiones se pueden depurar como una extensión de Shell estándar. Para obtener más información sobre cómo depurar extensiones de Shell, consulte [depuración con el shell](/previous-versions/windows/desktop/legacy/cc144064(v=vs.85)).

## <a name="debugging-active-directory-extensions-displayed-in-the-active-directory-mmc-snap-ins"></a>Depurar extensiones de Active Directory mostradas en el Active Directory MMC Snap-Ins

Active Directory extensiones mostradas en el Active Directory complementos de MMC administrativos se cargan en el contexto de Microsoft Management Console. Para depurar una extensión, busque Mmc.exe en el sistema local y establezca el depurador para utilizarlo como la aplicación para la depuración. En la mayoría de los sistemas, Mmc.exe se encuentra en el directorio del sistema de Windows, por ejemplo, C: \\ WinNT \\ system32. Dependiendo del depurador, puede o no tener que establecer el archivo DLL de extensión para que lo cargue también el depurador. Muchos depuradores también permiten adjuntar el depurador a un proceso de MMC en ejecución. Para obtener más información, vea el manual del usuario del depurador.

Puede ser conveniente que MMC cargue automáticamente un complemento específico. Para ello, establezca los argumentos de la aplicación en la ruta de acceso y el nombre de archivo de un archivo MSC. Puede ser un archivo MSC instalado por el sistema o uno que cree. Se puede crear un archivo MSC siguiendo estos pasos.

1.  Ejecute Mmc.exe.
2.  Cargue el complemento deseado seleccionando **archivo**  -  **Agregar o quitar complemento...** en el menú MMC y seleccione el complemento que desee.
3.  Guarde el archivo MSC seleccionando **archivo**  -  **Guardar como...** en el menú MMC.

Si no establece un archivo MSC de inicio, debe cargar manualmente el complemento deseado cuando ejecute la aplicación en el depurador.

Cuando la aplicación host se ejecuta en el depurador, el depurador puede mostrar un mensaje de advertencia que indica que la aplicación que se está ejecutando no contiene símbolos de depuración. Esto es normal y se puede omitir sin ningún riesgo porque realmente está depurando el archivo DLL, no la aplicación host.

En la mayoría de los casos, no se llamará a la extensión hasta que el usuario realice alguna acción que provoque la carga y la inicialización de la extensión. Por ejemplo, si está depurando una extensión de menú contextual que se muestra para los objetos de usuario, la extensión no se cargará hasta que se muestre el menú contextual de un objeto de usuario por primera vez.

Ahora debería poder establecer puntos de interrupción y ver los resultados de la depuración. Si no parece que la extensión se cargue, establezca un punto de interrupción en la función [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) de la extensión. Si no se llama a **DllGetClassObject** , es probable que la extensión no esté registrada correctamente.

Una vez finalizada la depuración, salga de MMC y el depurador debe descargarse con normalidad.

 

 