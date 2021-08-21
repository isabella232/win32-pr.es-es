---
description: Libera un bloqueo compartido.
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: CShareLockGNI::ShareUnlock (método)
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
ms.openlocfilehash: 2bf59b6e1aa0f6718cece105007a8ba502291c23868aca6ec55283dd7292f8b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162191"
---
# <a name="csharelocknhshareunlock-method"></a>CShareLockGNI::ShareUnlock (método)

Libera un bloqueo compartido.

## <a name="syntax"></a>Sintaxis


```C++
void ShareUnlock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cada llamada a [**ShareLock**](csharelocknh--sharelock.md) debe emparejarse exactamente con una llamada a **ShareUnlock.** Solo un subproceso que llama correctamente **a ShareLock** puede llamar a **ShareUnlock**; De lo contrario, puede producirse un interbloqueo.

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ShareLock**](csharelocknh--sharelock.md)
</dt> </dl>

 

 
