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
ms.openlocfilehash: 264997448aea028c5725d207ce4b301d369a092c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070010"
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

Puntero a la interfaz **IUnknown de** agregación.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a una nueva instancia de este objeto .

## <a name="remarks"></a>Observaciones

El generador de clases llama a este método para crear el objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Sysclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




