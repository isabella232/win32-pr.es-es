---
title: Propiedad IResultType PreceivedType (WdsSharedIDL.h)
description: Esta propiedad contiene la cadena utilizada para identificar el tipo en el índice.
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- PreceivedType, propiedad Legacy Windows Environment Features
- PreceivedType, propiedad Legacy Windows Environment Features , IResultType (Interfaz IResultType)
- IResultType interface Legacy Windows Environment Features , PreceivedType property
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765a770dc07f1fc0287e861ca79fc2aa941ea7cc425fff29e5e4c5772410c06e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014625"
---
# <a name="iresulttypepreceivedtype-property"></a>Propiedad IResultType::P receivedType

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use Windows [Search API](../search/-search-reference-entry-page.md) en su lugar. 

Esta propiedad contiene la cadena utilizada para identificar el tipo en el índice.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valor de propiedad

devuelve la dirección de la cadena identifyint el tipo en el índice.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio sp1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





