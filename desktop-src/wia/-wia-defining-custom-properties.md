---
description: Definir propiedades personalizadas.
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: Definir propiedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b78516913c898e3b3d814e96a40d227cc3cc1cc70c13a290949f91eb9f447c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119348055"
---
# <a name="defining-custom-properties"></a>Definir propiedades personalizadas

**Definir propiedades personalizadas**.

Si es necesario que el minidriver de adquisición de imágenes (WIA) de Windows defina propiedades personalizadas, se debe usar la propiedad WIA PRIVATE DEVPROP para las propiedades de elemento raíz personalizadas y la propiedad \_ \_ WIA \_ PRIVATE ITEMPROP" para otras propiedades de \_ elemento. Estas constantes se definen en *wiadef.h*.

En el código de ejemplo siguiente se muestran las definiciones de tres propiedades de elemento raíz. El identificador de propiedad de la primera propiedad de elemento raíz personalizado, CUSTOM ROOT PROP 1, se define en términos de \_ \_ \_ WIA \_ PRIVATE \_ DEVPROP. Los IDs de propiedad para las propiedades de elementos raíz adicionales se definen en términos de WIA \_ PRIVATE \_ DEVPROP + 1, WIA \_ PRIVATE \_ DEVPROP + 2, y así sucesivamente. El patrón se puede continuar si se necesitan propiedades de elemento raíz personalizadas adicionales.


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



En el ejemplo siguiente se muestran las definiciones de tres propiedades de elemento secundario personalizadas e iDs de propiedad. El identificador de propiedad de la primera propiedad de elemento secundario personalizado, CUSTOM CHILD PROP 1, se define en términos \_ \_ de \_ WIA PRIVATE \_ \_ ITEMPROP. Los IDs de propiedad para propiedades de elementos secundarios adicionales se definen en términos de WIA \_ PRIVATE \_ ITEMPROP + 1, y así sucesivamente. Como antes, el patrón se puede continuar si se necesitan más de estas propiedades de elementos secundarios personalizados.


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



Las propiedades de WIA personalizadas deben tener nombres de propiedad personalizados que estén asociados a los ID de propiedad personalizados. En el código de ejemplo siguiente se muestran las definiciones de tres nombres de propiedad de elemento raíz personalizados. (Estos nombres de propiedad se usan con los ID de propiedad personalizados que se crearon en un ejemplo anterior, donde el nombre de propiedad personalizado incluido en CUSTOM \_ ROOT PROP 1 STR está asociado al id. de propiedad del elemento \_ raíz personalizado CUSTOM ROOT PROP \_ \_ \_ \_ \_ 1).


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> Los nombres de propiedad de WIA *no se* localizan en varios idiomas. Esto se debe a que las aplicaciones pueden leer las propiedades de WIA mediante el identificador de propiedad o el nombre de propiedad. Si se usa el nombre, debe ser una constante, igual que el identificador de propiedad.

 

 

 



