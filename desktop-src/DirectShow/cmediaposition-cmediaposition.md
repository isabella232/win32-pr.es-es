---
description: Obtenga información sobre el método de constructor CMediaPosition.CMediaPosition (Ctlutil.h). Este método usa los parámetros "pName" y "pUnk".
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: Constructor CMediaPosition.CMediaPosition (Ctlutil.h):pName, pUnk parameters
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
ms.openlocfilehash: 0df3337c07ed678354515bdf0c665a5d6157f158ac6c2370a8981d8e5028b27e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634814"
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

Puntero al nombre del objeto para fines de depuración. Asigne este parámetro en la memoria estática.

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

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaPosition (clase)**](cmediaposition.md)
</dt> </dl>

 

 




