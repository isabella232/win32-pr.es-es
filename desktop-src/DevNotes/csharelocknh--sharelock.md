---
description: Obtiene un bloqueo compartido.
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: 'CShareLockNH:: ShareLock (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: d0c77564deceab29a8bee0cbffbd477559117cbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649746"
---
# <a name="csharelocknhsharelock-method"></a>CShareLockNH:: ShareLock (método)

Obtiene un bloqueo compartido.

## <a name="syntax"></a>Sintaxis


```C++
void ShareLock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cada llamada a **ShareLock** se debe emparejar con exactamente una llamada a [**ShareUnlock**](csharelocknh--shareunlock.md). Solo un subproceso que llame correctamente a **ShareLock** puede llamar a **ShareUnlock**; de lo contrario, se puede producir un interbloqueo.

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ShareUnlock**](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
