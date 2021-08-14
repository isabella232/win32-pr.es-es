---
title: Enumerar objetos de contenedor
description: Por convención, todos los elementos de una enumeración en ADSI deben ser del mismo tipo de datos de Automation. Por ejemplo, una enumeración no debe devolver algunos elementos como UNA VARIANTE de tipo VT I4 y otros como \_ UNA VARIANTE de tipo VT \_ BSTR.
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff6bb6d05a34ce6434531338a877d2dd4aaee2cd4df0b38c81b50b7f56db4bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428564"
---
# <a name="enumerating-container-objects"></a>Enumerar objetos de contenedor

Por convención, todos los elementos de una enumeración en ADSI deben ser del mismo tipo de datos de Automation. Por ejemplo, una enumeración no debe devolver algunos elementos como **UNA VARIANTE** de tipo **VT \_ I4** y otros como **UNA VARIANTE** de tipo **VT \_ BSTR**.

Para enumerar una lista de elementos que mantiene un objeto, un cliente solicita la creación de un objeto de enumeración para el tipo específico de información que se muestra. En ADSI, el cliente puede enumerar los objetos en objetos de espacio de nombres, objetos de contenedor genéricos, objetos de colección, objetos miembro u objetos de esquema. ADSI proporciona un filtro que se puede establecer y modificar para limitar las coincidencias de cualquier enumeración a través de la [**propiedad IADsContainer.Filter.**](iadscontainer-property-methods.md) Puede encontrar ejemplos de implementaciones de objetos enumeradores en el código de componente de proveedor de ejemplo para los siguientes objetos de contenedor de ADs.



| Tipo de objeto         | código         |
|---------------------|--------------|
| Contenedor genérico   | cenumobj.cpp |
| Contenedor de espacios de nombres | cenumns.cpp  |
| Contenedor de esquemas    | cenumsch.cpp |



 

Para obtener información del lado cliente, vea [Colecciones y grupos.](collections-and-groups.md)

 

 




