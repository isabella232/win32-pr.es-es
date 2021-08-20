---
title: Depuración de una Active Directory extensión
description: La hoja de propiedades Active Directory servicio de directorio de Microsoft, el menú contextual y las extensiones del Asistente para la creación de objetos documentadas en este tema se implementan como servidores com en proceso.
ms.assetid: 8c280084-fd2f-4d34-a119-d4e925a68a5c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aa5e6cc32a3ee2491cc18800bcf4aa2792452ac3fd5818940a682288932fb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020004"
---
# <a name="debugging-an-active-directory-extension"></a>Depuración de una Active Directory extensión

La hoja de propiedades Active Directory servicio de directorio de Microsoft, el menú contextual y las extensiones del Asistente para la creación de objetos documentadas en este tema se implementan como servidores com en proceso. Es decir, cada extensión es un archivo DLL que se ejecuta en el contexto del proceso de host. Para depurar la extensión, es necesario asociarla a una aplicación y ejecutarla en un depurador.

## <a name="debugging-active-directory-extensions-displayed-in-the-windows-shell"></a>Depurar extensiones Active Directory en el shell de Windows

Active Directory las extensiones que se muestran en Windows shell se cargan en el contexto del Explorer.exe proceso. Estas extensiones se pueden depurar como una extensión de shell estándar. Para obtener más información sobre la depuración de extensiones de shell, vea [Depuración con el shell](/previous-versions/windows/desktop/legacy/cc144064(v=vs.85)).

## <a name="debugging-active-directory-extensions-displayed-in-the-active-directory-mmc-snap-ins"></a>Depuración de Active Directory extensiones mostradas en el Active Directory MMC Snap-Ins

Active Directory que se muestran en Active Directory complementos MMC administrativos se cargan en el contexto del Microsoft Management Console. Para depurar una extensión, busque Mmc.exe en el sistema local y establezca el depurador para usarlo como aplicación para la depuración. En la mayoría de los sistemas, Mmc.exe se encuentra en el Windows del sistema, por ejemplo, C: \\ Winnt \\ System32. Dependiendo del depurador, es posible que tenga o no que establecer el archivo DLL de extensión para que también lo cargue el depurador. Muchos depuradores también permiten asociar el depurador a un proceso MMC en ejecución. Para obtener más información, consulte la Guía del usuario del depurador.

Puede ser conveniente que MMC cargue automáticamente un complemento específico. Para ello, establezca los argumentos de la aplicación en la ruta de acceso y el nombre de archivo de un archivo MSC. Puede ser un archivo MSC instalado por el sistema o uno que cree. Para crear un archivo MSC, siga estos pasos.

1.  Ejecute Mmc.exe.
2.  Cargue el complemento deseado seleccionando Agregar o quitar complemento   -  **de archivo... en el** menú MMC y seleccione el complemento deseado.
3.  Guarde el archivo MSC seleccionando **Archivo**  -  **Guardar como... en** el menú MMC.

Si no establece un archivo MSC de inicio, debe cargar manualmente el complemento deseado al ejecutar la aplicación en el depurador.

Cuando la aplicación host se ejecuta en el depurador, el depurador puede mostrar un mensaje de advertencia que indica que la aplicación que se ejecuta no contiene símbolos de depuración. Esto se espera y se puede omitir de forma segura porque realmente está depurando el archivo DLL, no la aplicación host.

En la mayoría de los casos, no se llamará a la extensión hasta que el usuario realice alguna acción que haga que la extensión se cargue e inicialice. Por ejemplo, si está depurando una extensión de menú contextual mostrada para objetos de usuario, la extensión no se cargará hasta la primera vez que se muestre el menú contextual de un objeto de usuario.

Ahora debería poder establecer puntos de interrupción y ver la salida de depuración. Si la extensión no parece cargarse, establezca un punto de interrupción en la [**función DllGetClassObject de la**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) extensión. Si **no se llama a DllGetClassObject,** es probable que la extensión no esté registrada correctamente.

Una vez completada la depuración, salga de MMC y el depurador se debe descargar con normalidad.

 

 