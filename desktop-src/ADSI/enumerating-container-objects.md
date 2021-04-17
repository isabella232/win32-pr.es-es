---
title: Enumerar objetos Container
description: Por Convención, todos los elementos de una enumeración en ADSI deben tener el mismo tipo de datos de automatización. Por ejemplo, una enumeración no debe devolver algunos elementos como una variante de tipo VT \_ I4 y otros como una variante del tipo VT \_ BSTR.
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5514596b02521fa869ffd7c712dcac2cacb40192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656183"
---
# <a name="enumerating-container-objects"></a>Enumerar objetos Container

Por Convención, todos los elementos de una enumeración en ADSI deben tener el mismo tipo de datos de automatización. Por ejemplo, una enumeración no debe devolver algunos elementos como una **variante** de tipo **VT \_ I4** y otros como una **variante** del tipo **VT \_ BSTR**.

Para enumerar una lista de los elementos que mantiene un objeto, un cliente solicita la creación de un objeto de enumeración para el tipo de información específico que se muestra. En ADSI, el cliente puede enumerar los objetos de objetos de espacio de nombres, objetos de contenedor genéricos, objetos de colección, objetos de miembro o objetos de esquema. ADSI proporciona un filtro que se puede establecer y modificar para limitar las coincidencias en cualquier enumeración a través de la propiedad [**IADsContainer. Filter**](iadscontainer-property-methods.md) . Puede encontrar ejemplos de implementaciones de objetos de enumerador en el código de componente de proveedor de ejemplo para los siguientes objetos de contenedor de ADs.



| Tipo de objeto         | código         |
|---------------------|--------------|
| Contenedor genérico   | cenumobj. cpp |
| Contenedor de espacio de nombres | cenumns. cpp  |
| Contenedor de esquema    | cenumsch. cpp |



 

Para obtener información del lado cliente, vea [colecciones y grupos](collections-and-groups.md).

 

 




