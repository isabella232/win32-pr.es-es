---
title: Registrando el servidor DLL para la activación de suplentes
description: Registrando el servidor DLL para la activación de suplentes
ms.assetid: 7133daa4-43b2-402e-a8ac-b357bea745d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca0af764bebf54590442f87f0b4ffdb1a681012
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794001"
---
# <a name="registering-the-dll-server-for-surrogate-activation"></a>Registrando el servidor DLL para la activación de suplentes

Un servidor DLL se cargará en un proceso suplente en las siguientes condiciones:

-   Debe haber un valor AppID especificado en la clave CLSID en el registro y una clave [AppID](appid-key.md) correspondiente.
-   En una llamada de activación, se establece el bit del [**\_ \_ servidor local CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) y la clave CLSID no especifica [LocalServer32](localserver32.md), [LocalServer](localserver.md)o [LocalService](localservice.md). Si se establecen otros bits **CLSCTX** , se sigue el [**algoritmo de procesamiento**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)para las marcas de ejecución in-Process, local o remota.
-   La clave CLSID contiene la subclave [InProcServer32](inprocserver32.md) .
-   La DLL de proxy/stub especificada en la clave **InProcServer32** existe.
-   El valor [DllSurrogate](dllsurrogate.md) existe en la clave **AppID** .

Si hay un servidor **LocalServer**, **LocalServer32** o **LocalService**, que indica la existencia de un archivo exe, siempre se iniciará el servidor o el servicio exe en su preferencia para cargar un servidor dll en un proceso suplente.

Se debe especificar el valor con nombre **DllSurrogate** para que se produzca la activación de suplentes. La activación hace referencia a las llamadas a cualquiera de las siguientes funciones de activación:

-   [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)
-   [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
-   [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)

Para iniciar una instancia del suplente proporcionado por el sistema, establezca el valor de **DllSurrogate** en una cadena vacía o en **null**. Para especificar el inicio de un suplente personalizado, establezca el valor en la ruta de acceso del suplente.

Si se especifica [RemoteServerName](remoteservername.md) y **DllSurrogate** para el mismo AppID, se omite el valor **remoteservername** y el valor **DllSurrogate** provoca una activación en el equipo local. Para la activación de suplentes remotos, especifique **RemoteServerName** pero no **DllSurrogate** en el cliente y especifique **DllSurrogate** en el servidor.

Un servidor DLL diseñado para ejecutarse siempre en su propio proceso suplente se configura mejor con un AppID igual a su CLSID. En **AppID**, solo hay que especificar un valor con nombre de **DllSurrogate** con un valor de cadena vacía.

Es mejor configurar un servidor DLL diseñado para ejecutarse por sí solo en su propio proceso suplente y para el servicio de varios clientes a través de una red con un valor [runas](runas.md) especificado en la clave del registro **AppID** . El hecho de que **runas** especifique "usuario interactivo" o una identidad de usuario específica depende de la interfaz de usuario, la seguridad y otros requisitos del servidor. Cuando se especifica un valor **runas** , solo se carga una instancia del servidor para atender a todos los clientes, independientemente de la identidad del cliente. Por otro lado, no configure el servidor con **runas** si la intención es tener una instancia del servidor dll que se ejecuta en suplente para atender cada identidad de cliente remoto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Requisitos del servidor DLL](dll-server-requirements.md)
</dt> <dt>

[Uso compartido de suplentes](surrogate-sharing.md)
</dt> </dl>

 

 