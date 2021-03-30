---
description: Conjuntos de propiedades
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: Conjuntos de propiedades (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdc65efbc99eeed3a5f94ab33ce5ec982975852
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422868"
---
# <a name="property-sets-directshow"></a>Conjuntos de propiedades (DirectShow)

Microsoft DirectShow usa conjuntos de propiedades para admitir los servicios extendidos ofrecidos por el hardware y sus controladores y filtros asociados. Los proveedores de hardware y filtro pueden definir nuevas capacidades como propiedades, organizarlas en conjuntos de propiedades y publicar la especificación de estos conjuntos de propiedades. Como desarrollador de la aplicación, puede usar los métodos de la interfaz [**IKsPropertySet**](ikspropertyset.md) para determinar si un controlador o filtro admite un conjunto determinado de propiedades y recuperar o establecer esas propiedades.

Todos los métodos expuestos por **IKsPropertySet** requieren un **GUID** que identifique el conjunto de propiedades (el parámetro *GuidPropSet* ) y un **valor DWORD** que identifique la propiedad dentro del conjunto de propiedades (el parámetro *dwPropID* ). El parámetro *dwPropID* normalmente es un miembro de un tipo de datos enumerados.

Las propiedades individuales pueden tener los datos asociados que se especifican en el parámetro *pPropData* en los métodos [**IKsPropertySet:: set**](ikspropertyset-set.md) y [**IKsPropertySet:: get**](ikspropertyset-get.md) . En estos métodos, los datos de la propiedad se escriben como un puntero a `void` . El tipo de datos y el significado de los datos se especifican en la definición del conjunto de propiedades.

En las secciones siguientes se proporciona información sobre los conjuntos de propiedades admitidos en DirectShow:

-   [**Conjunto de propiedades de protección de copia de DVD**](dvd-copy-protection-property-set.md)
-   [**Conjunto de propiedades de Karaoke de DVD**](dvd-karaoke-property-set.md)
-   [**Conjunto de propiedades de subimagen de DVD**](dvd-subpicture-property-set.md)
-   [Conjunto de propiedades de transporte de dispositivo externo](external-device-transport-property-set.md)
-   [Conjunto de propiedades de ejecución de fotogramas](frame-stepping-property-set.md)
-   [Conjunto de propiedades de PIN](pin-property-set.md)
-   [**Conjunto de propiedades de cambio de velocidad**](rate-change-property-set.md)

 

 



