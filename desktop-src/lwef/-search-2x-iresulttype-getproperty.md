---
title: Propiedad IResultType GetProperty (WdsSharedIDL.h)
description: Esta propiedad contiene información de propiedad especificada.
ms.assetid: 04c810f2-c781-4384-93ae-1060466e2bc4
keywords:
- Propiedades GetProperty Heredadas Windows environment
- Propiedad GetProperty Legacy Windows Environment Features , IResultType (interfaz)
- IResultType interface Legacy Windows Environment Features , GetProperty property
topic_type:
- apiref
api_name:
- IResultType.GetProperty
- IResultType.get_GetProperty
- IResultType.put_GetProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f35a0f2bce8fb4e098a2452b6d5575fa9843283562f7f1d051b588d9a0c8cd05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481109"
---
# <a name="iresulttypegetproperty-property"></a>IResultType::GetProperty, propiedad

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Esta propiedad contiene información de propiedad especificada.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GetProperty(
  [in]          VARIANT        index
);

HRESULT get_GetProperty(
  [out, retval] ISrsultPropery **prop
);
```



## <a name="property-value"></a>Valor de propiedad

Establece la dirección de la información de propiedad especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





