---
title: Propiedad IPropertyFilter LogicOperator (WdsSharedIDL.h)
description: Operador lógico que se usará al aplicar un filtro.
ms.assetid: 9461c7a3-1c70-41bf-a4fe-8dacd4d2ba49
keywords:
- Características heredadas del entorno de Windows logicOperator
- Propiedad LogicOperator Heredada de Windows Environment Features , interfaz IPropertyFilter
- IPropertyFilter interface Legacy Windows Environment Features , LogicOperator property
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
ms.openlocfilehash: 1fb4638edbb839581ad20ab6c860afc918b0ddd08e5fe6a36fc92f0dd4cea4a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963835"
---
# <a name="ipropertyfilterlogicoperator-property"></a>Propiedad IPropertyFilter::LogicOperator

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la API [Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Operador lógico que se usará al aplicar un filtro.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


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
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio sp1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





