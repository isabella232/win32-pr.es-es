---
title: Propiedad DisplayState IResultProperty (WdsSharedIDL.h)
description: Visibilidad de la propiedad.
ms.assetid: 4fdf6cdb-30bd-4582-a573-a1cc9f4052e6
keywords:
- Características heredadas del entorno de Windows displayState
- Propiedad DisplayState Legacy Windows Environment Features , IResultProperty (Interfaz IResultProperty)
- IResultProperty interface Legacy Windows Environment Features , DisplayState property
topic_type:
- apiref
api_name:
- IResultProperty.DisplayState
- IResultProperty.get_DisplayState
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cf4e8e285479f0c1d15d3c846e12786113410198935df5f83056ee89f39792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755157"
---
# <a name="iresultpropertydisplaystate-property"></a>Propiedad IResultProperty::D isplayState

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Visibilidad de la propiedad.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DisplayState(
  [out, retval] PropertyDisplayState *state
);
```



## <a name="property-value"></a>Valor de propiedad

devuelve un puntero al valor de estado de presentación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





