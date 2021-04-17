---
description: Libera un bloqueo compartido.
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: 'CShareLockNH:: ShareUnlock (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 80c4311f4bf66000440dac38da6300888a8e5d59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660483"
---
# <a name="csharelocknhshareunlock-method"></a>CShareLockNH:: ShareUnlock (método)

Libera un bloqueo compartido.

## <a name="syntax"></a>Sintaxis


```C++
void ShareUnlock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cada llamada a [**ShareLock**](csharelocknh--sharelock.md) se debe emparejar con exactamente una llamada a **ShareUnlock**. Solo un subproceso que llame correctamente a **ShareLock** puede llamar a **ShareUnlock**; de lo contrario, se puede producir un interbloqueo.

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ShareLock**](csharelocknh--sharelock.md)
</dt> </dl>

 

 
