---
description: Definir propiedades personalizadas.
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: Definir propiedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd91ee4d4e657ce0d6c01330d85e8df4ef57a36d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697174"
---
# <a name="defining-custom-properties"></a>Definir propiedades personalizadas

**Definir propiedades personalizadas**.

Si es necesario que el minicontrolador de adquisición de imágenes de Windows (WIA) defina las propiedades personalizadas, \_ se \_ debe usar la propiedad DEVPROP privada de WIA para las propiedades de los elementos raíz personalizados y la \_ \_ propiedad ITEMPROP privada de WIA para otras propiedades de elemento. Estas constantes se definen en *wiadef. h*.

En el ejemplo de código siguiente se muestran definiciones de tres propiedades de elemento raíz. El identificador de propiedad de la primera propiedad de elemento raíz personalizado \_ , \_ prop \_ . raíz personalizada 1, se define en términos de \_ DEVPROP privado de WIA \_ . Los identificadores de propiedad para las propiedades adicionales de los elementos raíz se definen en términos de WIA \_ Private \_ DEVPROP + 1, WIA \_ Private \_ DEVPROP + 2, etc. El patrón puede continuar si se necesitan propiedades adicionales del elemento raíz personalizado.


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



En el ejemplo siguiente se muestran definiciones de tres propiedades de elementos secundarios y identificadores de propiedad personalizados. El identificador de propiedad de la primera propiedad de elemento secundario personalizada, CUSTOM \_ Child \_ prop \_ 1, se define en términos de \_ ITEMPROP privado de WIA \_ . Los identificadores de propiedad para las propiedades adicionales de los elementos secundarios se definen en términos de \_ ITEMPROPs privados de WIA \_ + 1, etc. Como antes, el patrón puede continuar si se necesitan más de estas propiedades de elemento secundario personalizadas.


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



Las propiedades de WIA personalizadas deben tener nombres de propiedad personalizados que estén asociados a los identificadores de las propiedades personalizadas. En el ejemplo de código siguiente se muestran definiciones de tres nombres de propiedad de elementos raíz personalizados. (Estos nombres de propiedad se usan con los identificadores de propiedad personalizados que se crearon en un ejemplo anterior, donde el nombre de la propiedad personalizada contenía el personalizado \_ \_La Prop raíz \_ 1 \_ Str está asociada al identificador de la propiedad del elemento raíz personalizado \_ \_ prop \_ .


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> Los nombres de las propiedades de WIA *no* se localizan en varios idiomas. Esto se debe a que las aplicaciones pueden leer las propiedades de WIA mediante el identificador de propiedad o el nombre de la propiedad. Si se usa el nombre, debe ser una constante, del mismo modo que el identificador de la propiedad es.

 

 

 



