---
title: Propiedad IResultType DisplayName (WdsSharedIDL. h)
description: Nombre para mostrar localizado del tipo
ms.assetid: 21695ba3-aa6d-419b-961a-0643caa5ea1f
keywords:
- Propiedad DisplayName características de entorno de Windows heredadas
- Propiedad DisplayName características de entorno de Windows heredadas, interfaz IResultType
- Interfaz IResultType características del entorno heredado de Windows, propiedad DisplayName
topic_type:
- apiref
api_name:
- IResultType.DisplayName
- IResultType.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94080a2b5c6121bbaa9b611a7d55c2d5aaeed5e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705131"
---
# <a name="iresulttypedisplayname-property"></a>IResultType::D propiedad isplayName

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Nombre para mostrar localizado del tipo:

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valor de propiedad

Devuelve la dirección del nombre para mostrar adaptado para el tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                             |
| Redistribuible<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Encabezado<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





