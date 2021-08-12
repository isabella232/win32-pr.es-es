---
description: Obtenga información sobre el método de constructor CMediaPosition.CMediaPosition (Ctlutil.h). Este método usa los parámetros "pName", "pUnk" y "phr".
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: Constructor CMediaPosition.CMediaPosition (Ctlutil.h)
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
ms.openlocfilehash: 101678ebcb851ef0fcdc8eeaa202435ca80eb796555c81e5e5d95eb4998131c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655266"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a>Constructor CMediaPosition.CMediaPosition (Ctlutil.h): pName, pUnk, phr parameters

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
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

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a un **valor HRESULT.**

</dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Ctlutil.h (incluir Secuencias.h) |
| Biblioteca| Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaPosition (clase)**](cmediaposition.md)
</dt> </dl>

 

 




