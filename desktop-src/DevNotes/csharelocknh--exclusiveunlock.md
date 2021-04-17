---
description: Libera un bloqueo adquirido mediante ExclusiveLock en modo compartido.
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: 'CShareLockNH:: ExclusiveUnlock (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: f5fae5d6131bfcb386d52880b530f3def9464442
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661110"
---
# <a name="csharelocknhexclusiveunlock-method"></a>CShareLockNH:: ExclusiveUnlock (método)

Libera un bloqueo adquirido mediante [**ExclusiveLock**](csharelocknh--exclusivelock.md) en modo compartido.

## <a name="syntax"></a>Sintaxis


```C++
void ExclusiveUnlock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cada llamada a [**ExclusiveLock**](csharelocknh--exclusivelock.md) se debe emparejar con exactamente una llamada a **ExclusiveUnlock** para evitar el riesgo de un interbloqueo.

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ExclusiveLock**](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
