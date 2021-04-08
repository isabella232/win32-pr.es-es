---
title: Buscar una lista de atributos para consultar
description: Al buscar objetos de una clase determinada, las comparaciones en el filtro de búsqueda deben especificar atributos que realmente existan en los objetos de esa clase.
ms.assetid: 19d52933-e4b0-414f-9785-871e624da07b
ms.tgt_platform: multiple
keywords:
- Buscar una lista de atributos para consultar AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b6fb6b4d948a7cbc4d76caba9b78e189324eaa
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789537"
---
# <a name="finding-a-list-of-attributes-to-query"></a>Buscar una lista de atributos para consultar

Al buscar objetos de una clase determinada, las comparaciones en el filtro de búsqueda deben especificar atributos que realmente existan en los objetos de esa clase. Para obtener los atributos de la lista en un objeto de una clase determinada, enlace a esa clase en el esquema abstracto y recupere las propiedades [**IADsClass. MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) y **IADsClass. OptionalProperties** . Para obtener más información, vea [leer el esquema abstracto](reading-the-abstract-schema.md).

Además, todos los objetos heredan de la clase abstracta Top. Por lo tanto, puede existir cualquier atributo en la **parte superior** , aunque no se puede establecer en ningún objeto.

Si busca en el catálogo global, asegúrese de especificar atributos en el catálogo global. Los atributos incluidos en el catálogo global tienen el valor de **isMemberOfPartialAttributeSet** establecido en **true** en sus objetos **attributeSchema** . Tenga en cuenta que estos datos no están disponibles en el esquema abstracto; leerlo del objeto **attributeSchema** en el contenedor de esquemas.

En el catálogo global, solo se puede consultar un atributo de vínculo hacia atrás si se cumplen las dos condiciones siguientes: en primer lugar, el atributo se marca para su inclusión en el catálogo global. En segundo lugar, el vínculo de reenvío correspondiente también se marca para su inclusión en el catálogo global. Esto se aplica a los filtros de consulta, así como a los resultados de la consulta. Para obtener más información, vea [atributos vinculados](linked-attributes.md).

Además, se construyen algunos atributos, principalmente en el objeto de usuario. Los filtros de consulta no pueden contener atributos construidos. Los atributos construidos no se pueden evaluar en filtros de consulta; sin embargo, se pueden devolver en los resultados de la consulta. Esto se aplica a todos los contextos de nomenclatura y al catálogo global. Los atributos que se construyen tienen **ADS \_ SYSTEMFLAG \_ ATTR \_ \_ construido** (0x00000004) en la propiedad **systemFlags** en sus objetos **attributeSchema** .

> [!Note]  
> Para obtener más información sobre las clases y los atributos predefinidos [que se](active-directory-domain-services-reference.md)incluyen con el sistema, vea referencia de Active Directory Domain Services. En estas páginas se enumeran los atributos obligatorios y opcionales de cada clase de objeto. En el caso de los atributos, la página de referencia indica si el atributo está indexado, construido, vinculado o en el catálogo global.

 

 

 