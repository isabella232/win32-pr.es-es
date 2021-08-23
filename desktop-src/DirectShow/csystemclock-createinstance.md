---
description: El método CreateInstance crea una nueva instancia de este objeto .
ms.assetid: 5c62f781-0f22-4d8f-8517-272405dd07c5
title: Método CSystemClock.CreateInstance (Sysclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63626804ad4d067e5067170e0fc17cc83c179a906c0e625bb02a3ffb8a4ef197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687335"
---
# <a name="csystemclockcreateinstance-method"></a>Método CSystemClock.CreateInstance

El `CreateInstance` método crea una nueva instancia de este objeto .

## <a name="syntax"></a>Sintaxis


```C++
static CUnknown* WINAPI CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Punk* 
</dt> <dd>

Puntero a la interfaz **IUnknown de agregación.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a una nueva instancia de este objeto .

## <a name="remarks"></a>Comentarios

El generador de clases llama a este método para crear el objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Sysclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




