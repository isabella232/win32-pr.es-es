---
description: Recupera el identificador de clase para este filtro.
ms.assetid: f0559437-5d0d-4522-a3dc-947e3494b576
title: Método CPersistStream.GetClassID (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7603541eae4f431327a91777488a740afb7f628b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062421"
---
# <a name="cpersiststreamgetclassid-method"></a>Método CPersistStream.GetClassID

Recupera el identificador de clase para este filtro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pClsID* 
</dt> <dd>

Puntero a una estructura CLSID. Copie el identificador de clase aquí.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pstream.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPersistStream (clase)**](cpersiststream.md)
</dt> </dl>

 

 




