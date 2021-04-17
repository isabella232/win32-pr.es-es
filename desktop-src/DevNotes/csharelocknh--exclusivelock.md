---
description: Adquiere un bloqueo de lector/escritor.
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: 'CShareLockNH:: ExclusiveLock (método)'
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
ms.openlocfilehash: 8b35b544c10e6dde2887e75971d747feade5517e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661111"
---
# <a name="csharelocknhexclusivelock-method"></a>CShareLockNH:: ExclusiveLock (método)

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

Cada llamada a **ExclusiveLock** se debe emparejar con exactamente una llamada a [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) para evitar el riesgo de un interbloqueo.

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
