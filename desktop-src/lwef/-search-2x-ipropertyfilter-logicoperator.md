---
title: Propiedad IPropertyFilter LogicOperator (WdsSharedIDL. h)
description: Operador lógico que se va a usar al aplicar un filtro.
ms.assetid: 9461c7a3-1c70-41bf-a4fe-8dacd4d2ba49
keywords:
- Propiedad LogicOperator características de entorno heredado de Windows
- Propiedad LogicOperator características de entorno heredado de Windows, interfaz IPropertyFilter
- Interfaz IPropertyFilter características del entorno heredado de Windows, propiedad LogicOperator
topic_type:
- apiref
api_name:
- IPropertyFilter.LogicOperator
- IPropertyFilter.get_LogicOperator
- IPropertyFilter.put_LogicOperator
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c514ae6231a9d83063b4a294680bdd3949c91102
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493066"
---
# <a name="ipropertyfilterlogicoperator-property"></a>IPropertyFilter:: LogicOperator (propiedad)

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Operador lógico que se va a usar al aplicar un filtro.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_LogicOperator(
  [in]          FilterLogicOperator op
);

HRESULT get_LogicOperator(
  [out, retval] FilterLogicOperator *op
);
```



## <a name="property-value"></a>Valor de propiedad

Establece el tipo de operador lógico.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                             |
| Redistribuible<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Encabezado<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





