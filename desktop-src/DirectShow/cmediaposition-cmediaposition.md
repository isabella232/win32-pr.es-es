---
description: Obtenga información sobre el método de constructor CMediaPosition.CMediaPosition (Ctlutil.h). Este método usa los parámetros "pName" y "pUnk".
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: Constructor CMediaPosition.CMediaPosition (Ctlutil.h):pName, parámetros pUnk
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062469"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a>Constructor CMediaPosition.CMediaPosition (Ctlutil.h): pName, parámetros pUnk

Método constructor.

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

Puntero al nombre del objeto para fines de depuración. Asigne este parámetro en memoria estática.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntero al propietario de este objeto o **NULL** si el objeto no se agrega.

</dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Ctlutil.h (incluir Secuencias.h) |
| Biblioteca| Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaPosition (clase)**](cmediaposition.md)
</dt> </dl>

 

 




