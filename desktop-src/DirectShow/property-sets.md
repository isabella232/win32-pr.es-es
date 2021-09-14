---
description: Conjuntos de propiedades
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: Conjuntos de propiedades (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdc65efbc99eeed3a5f94ab33ce5ec982975852
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160124"
---
# <a name="property-sets-directshow"></a>Conjuntos de propiedades (DirectShow)

Microsoft DirectShow conjuntos de propiedades para admitir servicios extendidos ofrecidos por hardware y sus controladores y filtros asociados. Los proveedores de hardware y filtros pueden definir nuevas funcionalidades como propiedades, organizarlas en conjuntos de propiedades y publicar la especificación de estos conjuntos de propiedades. Como desarrollador de aplicaciones, puede usar los métodos de la interfaz [**IKsPropertySet**](ikspropertyset.md) para determinar si un controlador o filtro admite un conjunto determinado de propiedades y recuperar o establecer esas propiedades.

Todos los métodos expuestos por **IKsPropertySet** requieren un **GUID** que identifique el conjunto de propiedades (el parámetro *guidPropSet)* y un **DWORD** que identifique la propiedad dentro del conjunto de propiedades (el *parámetro dwPropID).* El *parámetro dwPropID* suele ser miembro de un tipo de datos enumerado.

Las propiedades individuales pueden tener datos asociados que especifique en el parámetro *pPropData* en los [**métodos IKsPropertySet::Set**](ikspropertyset-set.md) [**e IKsPropertySet::Get.**](ikspropertyset-get.md) En estos métodos, los datos de propiedad se escriben como un puntero a `void` . El tipo de datos y el significado de los datos se especifican en la definición del conjunto de propiedades.

En las secciones siguientes se proporciona información sobre los conjuntos de propiedades admitidos en DirectShow:

-   [**Conjunto de propiedades de protección de copia de DVD**](dvd-copy-protection-property-set.md)
-   [**Conjunto de propiedades DVD Dvd Dvd**](dvd-karaoke-property-set.md)
-   [**Conjunto de propiedades de subpicture de DVD**](dvd-subpicture-property-set.md)
-   [Conjunto de propiedades de transporte de dispositivos externos](external-device-transport-property-set.md)
-   [Conjunto de propiedades paso a paso de marco](frame-stepping-property-set.md)
-   [Anclar conjunto de propiedades](pin-property-set.md)
-   [**Conjunto de propiedades de cambio de frecuencia**](rate-change-property-set.md)

 

 



