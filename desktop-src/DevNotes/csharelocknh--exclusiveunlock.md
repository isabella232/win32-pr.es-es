---
description: Libera un bloqueo adquirido mediante ExclusiveLock en modo compartido.
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: CShareLockGNI::ExclusiveUnlock (método)
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
ms.openlocfilehash: 20d614f733b1668e3dea7619629cf2833f1d6af40384e679aea79a7a48279724
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667841"
---
# <a name="csharelocknhexclusiveunlock-method"></a>CShareLockGNI::ExclusiveUnlock (método)

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

Cada llamada a [**ExclusiveLock**](csharelocknh--exclusivelock.md) debe emparejarse con exactamente una llamada a **ExclusiveUnlock** para evitar el riesgo de un interbloqueo.

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ExclusiveLock**](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
