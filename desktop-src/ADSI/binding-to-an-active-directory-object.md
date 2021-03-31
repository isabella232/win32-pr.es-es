---
title: Enlazar a un objeto Active Directory
description: La forma más común de enlazar a un objeto Active Directory es usar la función GetObject entre un cliente ADSI y un proveedor ADSI.
ms.assetid: d278ea26-2fd5-4343-8d87-ff85515325fb
ms.tgt_platform: multiple
keywords:
- Enlazar a un objeto Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59992dbc88c00be6306dec24523ec4e030d4a516
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904817"
---
# <a name="binding-to-an-active-directory-object"></a>Enlazar a un objeto Active Directory

La forma más común de enlazar a un objeto Active Directory es usar la función **GetObject** entre un cliente ADSI y un proveedor ADSI. Esta es también la forma más fácil de mostrar cómo el componente de proveedor recibe las solicitudes de servicio y. Tanto la función [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) de la API ADSI como la función Visual Basic **GetObject** siguen los mismos pasos para el enlace.

En este ejemplo, suponga que el cliente ADSI es una aplicación de visor ADSI que ha recibido el ADsPath "Sample://Seattle/Redmond/Shelly" de la interfaz de usuario (1). En la siguiente ilustración se detalla la secuencia de eventos mediante la numeración de las flechas de flujo.

![vista detallada de los componentes ADSI](images/dscsex.png)

En la ilustración anterior, el cliente inicia la solicitud de un puntero de interfaz en el objeto Active Directory representado por el ADsPath "Sample://Seattle/Redmond/Shelly" de los servicios ADSI (2). Durante la inicialización, el software de servicios llenó una tabla de identificadores de programación (ProgID) del proveedor instalados desde el registro ("LDAP:", "Sample:", "WinNT:", etc.) y emparejarlos con los **CLSID** correspondientes que identifican el módulo de software adecuado.

El servidor ADSI comprueba que el ProgID, en este caso "Sample:", existe en ADsPath. A continuación, crea un contexto de enlace para optimizar más referencias a este objeto y llama a la función COM estándar [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) para crear un moniker com que se puede usar para buscar y enlazar al objeto que representa al usuario "Shelly".

En la sección siguiente, los nombres de archivo del código fuente del componente de proveedor de ejemplo se incluyen entre paréntesis cuando corresponda.

Como en otras implementaciones de servidor COM, [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) examina el identificador de programa (ProgID) y busca el **CLSID** adecuado en el registro (3) para buscar el código de generador de clases proporcionado por el proveedor correspondiente (Cprovcf. cpp) en la implementación de proveedor adecuada (4). Este código crea un objeto de nivel superior inicial que implementa el método [**IParseDisplayName::P arsedisplayname**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) (Cprov. cpp). La implementación del proveedor de **ParseDisplayName** resuelve la ruta de acceso en el espacio de nombres propio del proveedor. En este momento, se llama a ADsObject y se invoca el analizador proporcionado con el componente de proveedor (Parse. cpp) para comprobar que el ADsPath es sintácticamente correcto para este espacio de nombres.

**GetObject**, que se define en Getobj. cpp, determina si el objeto solicitado es un objeto de espacio de nombres, un objeto de esquema o algún otro tipo de objeto. Si uno de los dos primeros, se crea ese tipo de objeto de clase de esquema y se recupera el puntero de interfaz adecuado. De lo contrario, la ruta de acceso del directorio de ejemplo se crea a partir de la ADsPath (por ejemplo, " \\ Seattle \\ Redmond \\ Shelly", pero en un servicio de directorio diferente podría haber tenido que ser " \\ ou = Seattle \\ ou = Redmond \\ CN = Shelly") y el control pasa a SampleDSOpenObject, que abre el objeto en el almacenamiento de datos de ejemplo y también recupera su tipo de objeto

Con los datos recopilados, se crea un nuevo objeto (6) para representar el elemento descrito por ADsPath y se recupera un puntero a la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) en ese objeto. En este caso, se crea un objeto de Active Directory genérico que admite los métodos **IUnknown** y [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) (Cgenobj. cpp, Core. cpp). La rutina CSampleDSGenObject:: AllocateGenObject Lee los datos de la biblioteca de tipos para crear las entradas de envío adecuadas para estos objetos nuevos con el fin de admitir [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

Al ajustar este puntero de interfaz en un moniker, se completa la función ResolvePathName (Cprov. cpp) y se analiza el nombre para mostrar.

Todos los objetos COM creados durante este proceso se almacenan en caché por motivos de rendimiento y se administran a través del contexto de enlace. Esto mejora el rendimiento de otras operaciones en el mismo objeto que sigue inmediatamente al enlace de moniker.

Ahora se consulta el objeto Active Directory con formato correcto para el identificador de interfaz solicitado para la llamada inicial de [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) y se recupera un puntero a esa interfaz (7) y se devuelve a través del servidor ADSI al cliente (8&9). Desde entonces, el cliente trabaja directamente con el componente de proveedor a través de los métodos de interfaz hasta que se cumple la solicitud inicial (10).

Además, las solicitudes de datos de objetos del cliente normalmente adoptan la forma de solicitudes de las propiedades obtiene y put de la propiedad, que se optimizan mediante la implementación de proveedor de una caché de propiedades (Cprops. cpp). Empaquetar y desempaquetar datos de forma inteligente, que a menudo incluye la copia y liberación de estructuras y cadenas, entre los tipos de datos nativos del sistema operativo del componente de proveedor de ejemplo y el tipo de [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) de automatización que admite ADSI tiene lugar antes de que se carguen las propiedades en la memoria caché (Smpoper. cpp).

El componente de proveedor de ejemplo está diseñado para que las llamadas reales al sistema operativo estén aisladas lógicamente del componente de proveedor, lo que crea un software portable a más de un sistema operativo (RegDSAPI. cpp).

 

 