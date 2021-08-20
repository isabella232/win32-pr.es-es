---
title: Buscar una lista de atributos para consultar
description: Al buscar objetos de una clase determinada, las comparaciones en el filtro de búsqueda deben especificar los atributos que existen realmente en los objetos de esa clase.
ms.assetid: 19d52933-e4b0-414f-9785-871e624da07b
ms.tgt_platform: multiple
keywords:
- Buscar una lista de atributos para consultar AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0edfee59c42a8cf07be05ab31e58c0298f7285c8a02de659257e3b3cd14bfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189195"
---
# <a name="finding-a-list-of-attributes-to-query"></a>Buscar una lista de atributos para consultar

Al buscar objetos de una clase determinada, las comparaciones en el filtro de búsqueda deben especificar los atributos que existen realmente en los objetos de esa clase. Para obtener los atributos de lista de un objeto de una clase determinada, enlace a esa clase en el esquema abstracto y recupere las propiedades [**IADsClass.MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) e **IADsClass.OptionalProperties.** Para obtener más información, vea [Leer el esquema abstracto](reading-the-abstract-schema.md).

Además, todos los objetos heredan de la clase abstracta superior. Por lo tanto, cualquier atributo de **la** parte superior puede existir, aunque no se pueda establecer, en cualquier objeto.

Si busca en el catálogo global, asegúrese de especificar atributos en el catálogo global. Los atributos incluidos en el catálogo global tienen **isMemberOfPartialAttributeSet** establecido en **TRUE** en sus **objetos attributeSchema.** Tenga en cuenta que estos datos no están disponibles en el esquema abstracto; léalo desde el **objeto attributeSchema** en el contenedor de esquemas.

En el catálogo global, solo se puede consultar un atributo de vínculo posterior si se cumplen las dos condiciones siguientes: en primer lugar, el atributo se marca para su inclusión en el catálogo global. En segundo lugar, el vínculo hacia delante correspondiente también se marca para su inclusión en el catálogo global. Esto se aplica a los filtros de consulta, así como a los resultados de la consulta. Para obtener más información, vea [Atributos vinculados.](linked-attributes.md)

Además, se construyen algunos atributos, principalmente en el objeto de usuario. Los filtros de consulta no pueden contener atributos construidos. Los atributos construidos no se pueden evaluar en filtros de consulta; sin embargo, se pueden devolver en los resultados de la consulta. Esto se aplica a todos los contextos de nomenclatura y al catálogo global. Los atributos que se construyen tienen **ADS \_ SYSTEMFLAG \_ ATTR \_ IS \_ CONSTRUCTED** (0x00000004) en la propiedad **systemFlags** en sus **objetos attributeSchema.**

> [!Note]  
> Para obtener más información sobre las clases predefinidas y los atributos incluidos con el sistema, [vea Active Directory Domain Services referencia](active-directory-domain-services-reference.md). Estas páginas enumera los atributos obligatorios y opcionales de cada clase de objeto. Para los atributos, la página de referencia indica si el atributo está indexado, construido, vinculado o en el catálogo global.

 

 

 