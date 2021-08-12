---
description: Adquiere un bloqueo de lector/escritor.
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: CShareLockGNI::ExclusiveLock (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 16a5d2ba49d5ff1c25079a99a979d7a0fb4a51ee64d54fa4042152d7b010dc1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667968"
---
# <a name="csharelocknhexclusivelock-method"></a>CShareLockGNI::ExclusiveLock (método)

Adquiere un bloqueo de lector/escritor.

## <a name="syntax"></a>Sintaxis


```C++
void ExclusiveLock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cada llamada a **ExclusiveLock** debe emparejarse con exactamente una llamada a [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) para evitar el riesgo de un interbloqueo.

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
