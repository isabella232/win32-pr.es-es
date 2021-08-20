---
title: Colecciones y grupos
description: ADSI usa objetos de colección para representar cualquier conjunto arbitrario de elementos de un servicio de directorio que se puede representar con el mismo tipo de datos.
ms.assetid: 03257cc9-f354-4e1c-8880-936a7acac3ef
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, using, colecciones y grupos
- ADSI de colecciones
- adsi de grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c872caec4734e8ab47b032ca9fc72f0aa57c8d51abc5e5a41a569794a4389905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017661"
---
# <a name="collections-and-groups"></a>Colecciones y grupos

ADSI usa objetos de colección para representar cualquier conjunto arbitrario de elementos de un servicio de directorio que se puede representar con el mismo tipo de datos. Los objetos de colección se definen como un conjunto de valores **VARIANT,** que representan cualquiera de los tipos de datos válidos de Automation. Los objetos de colección pueden representar información persistente, como listas de control de acceso e información volátil, como trabajos de impresión en una cola de impresión.

La convención COM estándar para enumerar el contenido de un objeto de colección (o contenedor) es crear un objeto enumerador que admita [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), que tiene métodos para pasar por la lista de objetos de colección. Las interfaces de ADSI que suministran el método **get \_ \_ NewEnum** (tenga en cuenta los dos caracteres de subrayado) son [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) e [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection). ADSI también proporciona las funciones auxiliares [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) y [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) para programas de C y C++ para simplificar la enumeración. Los clientes de Automation usan la enumeración implícitamente cuando llaman a **Next** en un **bucle For.**

Los grupos son simplemente colecciones de objetos que admiten [**la interfaz IADsMembers.**](/windows/desktop/api/Iads/nn-iads-iadsmembers)

 

 