---
title: Colecciones y grupos
description: ADSI usa objetos de colección para representar cualquier conjunto arbitrario de elementos de un servicio de directorio que se puede representar con el mismo tipo de datos.
ms.assetid: 03257cc9-f354-4e1c-8880-936a7acac3ef
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usar, colecciones y grupos
- ADSI de colecciones
- grupos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f0f4d699d8dde0c3d70c7449dfe146212b2b30
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995615"
---
# <a name="collections-and-groups"></a>Colecciones y grupos

ADSI usa objetos de colección para representar cualquier conjunto arbitrario de elementos de un servicio de directorio que se puede representar con el mismo tipo de datos. Los objetos de colección se definen como un conjunto de valores **Variant** que representan cualquiera de los tipos de datos de automatización válidos. Los objetos de colección pueden representar tanto la información persistente como las listas de control de acceso y la información volátil, como los trabajos de impresión en una cola de impresión.

La Convención COM estándar para mostrar el contenido de un objeto de colección (o contenedor) consiste en crear un objeto de enumerador que admita [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), que tiene métodos para recorrer la lista de objetos de colección. Las interfaces de ADSI que proporcionan el método **Get \_ \_ NewEnum** (observe los dos subrayados) son [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) y [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection). ADSI también proporciona las funciones auxiliares [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) y [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) para los programas de C y C++ con el fin de simplificar la enumeración. Los clientes de automatización utilizan la enumeración implícitamente cuando llaman a **Next** en un bucle **for** .

Los grupos son simplemente colecciones de objetos que admiten la interfaz [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) .

 

 