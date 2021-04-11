---
description: El calificador ViewSpaces define los nombres y la ubicación de los espacios de nombres donde se encuentran las instancias de origen. Puede especificar cualquier combinación de espacios de nombres en equipos locales o remotos.
ms.assetid: 15d71bb6-842d-4f5a-b2e3-e9f60f0aea3b
ms.tgt_platform: multiple
title: Calificador ViewSpaces
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSpaces
api_type:
- NA
api_location: ''
ms.openlocfilehash: 683f5596497f3c1e1ad0f2b85eaaa1460177a0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279096"
---
# <a name="viewspaces-qualifier"></a>Calificador ViewSpaces

El **calificador ViewSpaces** define los nombres y la ubicación de los espacios de nombres donde se encuentran las instancias de origen. Puede especificar cualquier combinación de espacios de nombres en equipos locales o remotos.

En el ejemplo siguiente se muestran dos espacios de nombres en el equipo local.


```mof
ViewSpaces{"\\\\.\\root\\LocalNamespace",
     "\\\\.\\root\\RemoteNamespace"}
```



El [proveedor de vistas](view-provider.md) hace coincidir las consultas de origen del [calificador ViewSources](viewsources-qualifier.md) con los espacios de nombres enumerados en el calificador **ViewSpaces** en el orden en que se muestran las consultas y los espacios de nombres. Normalmente, hay una relación uno a uno entre el número de espacios de nombres enumerados en el calificador **ViewSpaces** y las consultas enumeradas en el calificador **ViewSources** . En algunos casos, puede que desee que las consultas enumeradas en el calificador ViewSources se ejecuten en dos o más espacios de nombres. Puede usar un signo de dos puntos dobles "::" para separar varios espacios de nombres que se evaluarán mediante una de las consultas de la matriz **ViewSources** .

En el ejemplo siguiente, la primera consulta de la matriz [**ViewSources**](viewsources-qualifier.md) se ejecutará en el espacio de nombres en el primer par de Comillas, en la segunda consulta con los tres espacios de nombres en el segundo par de Comillas, y en la tercera consulta con los dos espacios de nombres del tercer par de Comillas.


```mof
ViewSpaces
    {
    "\\\\.\\root\\LocalNamespace",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace2::
        \\\\.\\root\\RemoteNamespace3",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace3"
    }
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Calificadores específicos del proveedor de vistas**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




