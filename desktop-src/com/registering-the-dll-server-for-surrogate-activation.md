---
title: Registro del servidor DLL para la activación suplente
description: Registro del servidor DLL para la activación suplente
ms.assetid: 7133daa4-43b2-402e-a8ac-b357bea745d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca0af764bebf54590442f87f0b4ffdb1a681012
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973593"
---
# <a name="registering-the-dll-server-for-surrogate-activation"></a>Registro del servidor DLL para la activación suplente

Un servidor DLL se cargará en un proceso suplente en las siguientes condiciones:

-   Debe haber un valor AppID especificado en la clave CLSID en el Registro y una clave [AppID](appid-key.md) correspondiente.
-   En una llamada de activación, se establece el bit [**CLSCTX \_ LOCAL \_ SERVER**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) y la clave CLSID no especifica [LocalServer32,](localserver32.md) [LocalServer](localserver.md)o [LocalService](localservice.md). Si se establecen otros bits **CLSCTX,** se sigue el algoritmo de procesamiento para las marcas de ejecución en proceso, local o remota. [](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
-   La clave CLSID contiene la [subclave InprocServer32.](inprocserver32.md)
-   Existe el archivo DLL de proxy/stub especificado en la **clave InprocServer32.**
-   El [valor DllSurrogate](dllsurrogate.md) existe en la **clave AppID.**

Si hay un **servidor LocalServer**, **LocalServer32** o **LocalService**, que indica la existencia de un exe, el servidor o servicio EXE siempre se inicia en lugar de cargar un servidor DLL en un proceso suplente.

Se debe especificar el valor con nombre de **DllSurrogate** para que se produzca la activación suplente. La activación hace referencia a las llamadas a cualquiera de las siguientes funciones de activación:

-   [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)
-   [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
-   [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)

Para iniciar una instancia del suplente proporcionado por el sistema, establezca el valor de **DllSurrogate** en una cadena vacía o en **NULL.** Para especificar el inicio de un suplente personalizado, establezca el valor en la ruta de acceso del suplente.

Si se [especifican RemoteServerName](remoteservername.md) y **DllSurrogate** para el mismo AppID, se omite el valor **RemoteServerName** y el valor **DllSurrogate** provoca una activación en el equipo local. Para la activación suplente remota, especifique **RemoteServerName** pero no **DllSurrogate** en el cliente y especifique **DllSurrogate** en el servidor.

Un servidor DLL diseñado para ejecutarse siempre solo en su propio proceso suplente se configura mejor con un AppID igual a su CLSID. En **AppID**, simplemente especifique un valor con nombre **DllSurrogate** con un valor de cadena vacío.

Es mejor configurar un servidor DLL diseñado para ejecutarse solo en su propio proceso suplente y para dar servicio a varios clientes a través de una red con un valor [RunAs](runas.md) especificado en la clave del Registro **AppID.** Si **runAs especifica** "Usuario interactivo" o una identidad de usuario específica depende de la interfaz de usuario, la seguridad y otros requisitos del servidor. Cuando se especifica un valor **RunAs,** solo se carga una instancia del servidor para dar servicio a todos los clientes, independientemente de la identidad del cliente. Por otro lado, no configure el servidor con **RunAs** si la intención es que una instancia del servidor DLL se ejecute en suplente para dar servicio a cada identidad de cliente remota.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Requisitos del servidor DLL](dll-server-requirements.md)
</dt> <dt>

[Uso compartido suplente](surrogate-sharing.md)
</dt> </dl>

 

 