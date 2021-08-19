---
title: Enlace a un objeto Active Directory
description: La manera más común de enlazar a un objeto Active Directory es usar la función GetObject entre un cliente ADSI y un proveedor ADSI.
ms.assetid: d278ea26-2fd5-4343-8d87-ff85515325fb
ms.tgt_platform: multiple
keywords:
- Enlace a un Active Directory ADSI de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc788ed9eb124e1da6c21848f02393d46608f00dd3a9e779788fa54429922400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429143"
---
# <a name="binding-to-an-active-directory-object"></a>Enlace a un objeto Active Directory

La manera más común de enlazar a un objeto Active Directory es usar la función **GetObject** entre un cliente ADSI y un proveedor ADSI. Esta es también la manera más fácil de mostrar cómo el componente de proveedor recibe las solicitudes de servicios y . Tanto la función de API ADSI [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) como la Visual Basic **getObject** siguen los mismos pasos para el enlace.

En este ejemplo, suponga que el cliente ADSI es una aplicación de visor ADSI que ha recibido la "Sample://Seattle/Redmond/Shelly" de ADsPath de su interfaz de usuario (1). En la ilustración siguiente se detalla la secuencia de eventos mediante la numeración de las flechas de flujo.

![vista detallada de los componentes adsi](images/dscsex.png)

En la ilustración anterior, el cliente inicia la solicitud de un puntero de interfaz en el objeto Active Directory representado por ADsPath "Sample://Seattle/Redmond/Shelly" de los servicios ADSI (2). Durante la inicialización, el software de servicios ha rellenado una tabla de identificadores de programación de proveedores instalados (ProgID) desde el registro ("LDAP:","Sample:", "WinNT:", y así sucesivamente) y los empareja con los **CLSID** correspondientes que identifican el módulo de software adecuado.

El servidor ADSI comprueba que el ProgID, en este caso "Sample:", existe en ADsPath. A continuación, crea un contexto de enlace para optimizar más referencias a este objeto y llama a la función COM [**estándar MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) para crear un moniker COM que se puede usar para buscar y enlazar al objeto que representa al usuario "Shelly".

En la sección siguiente, los nombres de archivo del código fuente del componente de proveedor de ejemplo se incluyen entre paréntesis cuando corresponda.

Al igual que en otras implementaciones de servidor COM, [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) examina el ProgID y busca el **CLSID** adecuado en el Registro (3) para buscar el código de generador de clases proporcionado por el proveedor correspondiente (Cprovcf.cpp) en la implementación del proveedor adecuada (4). Este código crea un objeto inicial de nivel superior que implementa el método [**IParseDisplayName::P arseDisplayName**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) (Cprov.cpp). La implementación del proveedor de **ParseDisplayName** resuelve la ruta de acceso en el propio espacio de nombres del proveedor. Esto finalmente llama a ADsObject e invoca el analizador proporcionado con el componente de proveedor (Parse.cpp) para comprobar que ADsPath es sintácticamente correcto para este espacio de nombres.

**GetObject**, que se define en Getobj.cpp y, a continuación, determina si el objeto solicitado es un objeto de espacio de nombres, un objeto de esquema o algún otro tipo de objeto. Si alguno de los dos primeros, se crea ese tipo de objeto de clase de esquema y se recupera el puntero de interfaz adecuado. De lo contrario, la ruta de acceso del directorio de ejemplo se crea a partir de ADsPath (por ejemplo, "Seattle Redmond Shelly", pero en un servicio de directorio diferente podría haber tenido que ser \\ \\ \\ \\ "OU=Seattle OU=Redmond CN=Shelly") y el control pasa a SampleDSOpenObject, que abre el objeto en el almacenamiento de datos de ejemplo y también recupera su tipo de objeto (en este \\ \\ caso, "User") (5).

Con los datos recopilados, se crea un nuevo objeto (6) para representar el elemento descrito por ADsPath y se recupera un puntero a la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) en ese objeto. En este caso, se crea un objeto Active Directory genérico que admite los métodos **IUnknown** e [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) (Cgenobj.cpp, Core.cpp). La rutina CSampleDSGenObject::AllocateGenObject lee los datos de la biblioteca de tipos para crear las entradas de distribución adecuadas para estos nuevos objetos con el fin de admitir [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

Al encapsular este puntero de interfaz en un moniker, se completa la función ResolvePathName (Cprov.cpp) y se analiza el nombre para mostrar.

Todos los objetos COM creados durante este proceso se almacenan en caché por motivos de rendimiento y se administran a través del contexto de enlace. Esto mejora el rendimiento de otras operaciones en el mismo objeto que sigue inmediatamente al enlace del moniker.

Este objeto Active Directory bien formado ahora se consulta para el identificador de interfaz solicitado para la llamada [**inicial ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) y se recupera un puntero a esa interfaz (7) y se pasa a través del servidor ADSI al cliente (8&9). A partir de ese momento, el cliente trabaja directamente con el componente de proveedor a través de los métodos de interfaz hasta que se satisface la solicitud inicial (10).

Además, las solicitudes de datos de objeto del cliente suelen tener la forma de solicitudes para la propiedad gets y puts, todas las cuales se optimizan a través de la implementación del proveedor de una caché de propiedades (Cprops.cpp). Empaquetar y desempaquetar datos de forma inteligente, lo que a menudo incluye copiar y liberar estructuras y cadenas, entre los tipos de datos nativos del sistema operativo del componente de proveedor de ejemplo y el tipo [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) de Automation compatible con ADSI tiene lugar antes de que las propiedades se carguen en la caché (Smpoper.cpp).

El componente de proveedor de ejemplo está diseñado para que las llamadas reales al sistema operativo estén aisladas lógicamente del componente de proveedor, creando software portátil a más de un sistema operativo (RegDSAPI.cpp).

 

 