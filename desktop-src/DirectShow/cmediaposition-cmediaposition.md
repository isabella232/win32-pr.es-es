---
description: Obtenga información sobre el método de constructor CMediaPosition. CMediaPosition (Ctlutil. h). Este método usa los parámetros ' pName ' y ' pUnk '.
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: Constructor CMediaPosition. CMediaPosition (Ctlutil. h)-pName, parámetros pUnk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e65f034e5f8857b21bc706bce45aa74c3c3cf966
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105670271"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a>Constructor CMediaPosition. CMediaPosition (Ctlutil. h)-pName, parámetros pUnk

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Puntero al nombre del objeto, para la depuración. Asigne este parámetro en la memoria estática.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntero al propietario de este objeto, o **null** si no se agrega el objeto.

</dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Ctlutil. h (incluir streams. h) |
| Biblioteca| Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




