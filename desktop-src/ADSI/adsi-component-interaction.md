---
title: Interacción de componentes ADSI
description: El Active Directory de enrutador rellena una tabla de proveedores ADSI de los proveedores ADSI instalados que aparecen en el registro cuando recibe la primera solicitud de la aplicación cliente.
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec82573c23564c964ebe310cd7eceb917a4565ed2d6fa8aa40b4dc03d1db2d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181118"
---
# <a name="adsi-component-interaction"></a>Interacción de componentes ADSI

El Active Directory de enrutador rellena una tabla de proveedores ADSI de los proveedores ADSI instalados que aparecen en el registro cuando recibe la primera solicitud de la aplicación cliente. Para obtener más información sobre el Registro, vea [Instalar el componente de proveedor de ejemplo](installing-the-example-provider-component.md).

Las operaciones que hacen una solicitud desde un directorio para un puntero a una interfaz en un objeto Active Directory proceden de una función (**GetObject** en Visual Basic o [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) en C o C++), o un método de interfaz ( [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)). En la ilustración siguiente, la aplicación cliente ADSI pasa dicha solicitud de enlace al componente de enrutador ADSI (1). El componente de enrutador identifica el ProgID del proveedor desde la primera parte de ADsPath y usa [**CLSIDFromProgID para**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) buscar el CLSID correspondiente en el registro (2) y carga el componente de proveedor adecuado (3).

![Interacciones de componentes adsi en el proveedor de ejemplo](images/dscspr.png)

En la ilustración anterior, el componente de proveedor crea un objeto Active Directory que representa el elemento de directorio con nombre. El componente de compatibilidad de ADSI realiza **una interfaz QueryInterface** en el identificador de interfaz solicitado. Cuando se recupera un puntero a esa interfaz (4), como con todas las implementaciones de cliente/servidor COM, se vuelve a pasar al cliente (5) y, a partir de ese momento, la aplicación cliente funciona directamente con el componente de proveedor (6).

 

 