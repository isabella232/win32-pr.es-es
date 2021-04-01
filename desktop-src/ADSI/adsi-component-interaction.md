---
title: Interacción de componentes ADSI
description: El componente del enrutador Active Directory rellena una tabla del proveedor ADSI de los proveedores ADSI instalados que aparecen en el registro cuando recibe la primera solicitud de la aplicación cliente.
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a9ca749e1083ab86335893bef9f4307faee410
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793804"
---
# <a name="adsi-component-interaction"></a>Interacción de componentes ADSI

El componente del enrutador Active Directory rellena una tabla del proveedor ADSI de los proveedores ADSI instalados que aparecen en el registro cuando recibe la primera solicitud de la aplicación cliente. Para obtener más información sobre el registro, vea [instalar el componente de proveedor de ejemplo](installing-the-example-provider-component.md).

Las operaciones que realizan una solicitud desde un directorio para un puntero a una interfaz en un objeto Active Directory proceden de una función (**GetObject** en Visual Basic o [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) en C o C++) o un método de interfaz ( [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)). En la ilustración siguiente, la aplicación cliente ADSI pasa esta solicitud de enlace al componente del enrutador ADSI (1). El componente router identifica el identificador de programa (ProgID) del proveedor de la primera parte de ADsPath y usa [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) para buscar el CLSID coincidente en el registro (2) y carga el componente de proveedor adecuado (3).

![interacciones de componentes ADSI en el proveedor de ejemplo](images/dscspr.png)

En la ilustración anterior, el componente de proveedor crea un objeto Active Directory que representa el elemento de directorio con nombre. El componente de compatibilidad con ADSI realiza una operación **QueryInterface** en el identificador de interfaz solicitado. Cuando se recupera un puntero a la interfaz (4), al igual que con todas las implementaciones de cliente/servidor COM, se pasa de nuevo al cliente (5) y, desde ese momento, la aplicación cliente trabaja directamente con el componente de proveedor (6).

 

 