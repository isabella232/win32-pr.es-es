---
description: El calificador ViewSpaces define los nombres y la ubicación de los espacios de nombres donde se encuentran las instancias de origen. Puede especificar cualquier combinación de espacios de nombres en equipos locales o remotos.
ms.assetid: 15d71bb6-842d-4f5a-b2e3-e9f60f0aea3b
ms.tgt_platform: multiple
title: Calificador viewSpaces
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
ms.openlocfilehash: edaec0328d67ad540a12e3393aabf5b973112bbf00f64f735d6a5f64cf338365
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049903"
---
# <a name="viewspaces-qualifier"></a>Calificador viewSpaces

El **calificador ViewSpaces define** los nombres y la ubicación de los espacios de nombres donde se encuentran las instancias de origen. Puede especificar cualquier combinación de espacios de nombres en equipos locales o remotos.

En el ejemplo siguiente se enumeran dos espacios de nombres en el equipo local.


```mof
ViewSpaces{"\\\\.\\root\\LocalNamespace",
     "\\\\.\\root\\RemoteNamespace"}
```



El [proveedor View](view-provider.md) coincide con las consultas de origen del calificador [ViewSources](viewsources-qualifier.md) con los espacios de nombres enumerados en el calificador **ViewSpaces** en el orden en que se enumeran las consultas y los espacios de nombres. Normalmente, hay una relación uno a uno entre el número de espacios de nombres enumerados en el calificador **ViewSpaces** y las consultas enumeradas en el **calificador ViewSources.** En algunos casos, es posible que desee que las consultas enumeradas en el calificador ViewSources se ejecuten en dos o más espacios de nombres. Puede usar un signo de dos puntos "::" para separar varios espacios de nombres que evaluará una de las consultas de la **matriz ViewSources.**

En el ejemplo siguiente, la primera consulta de la matriz [**ViewSources**](viewsources-qualifier.md) se ejecutará en el espacio de nombres del primer par de comillas, la segunda consulta en los tres espacios de nombres del segundo par de comillas y la tercera consulta en los dos espacios de nombres del tercer par de comillas.


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



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Calificadores específicos del proveedor de vistas**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




