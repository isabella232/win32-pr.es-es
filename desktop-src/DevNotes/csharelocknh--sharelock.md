---
description: Obtiene un bloqueo compartido.
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: CShareLockLOCK::ShareLock (método)
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
ms.openlocfilehash: 7fd398228c6d0feb7e63133e8faeefd7a2fd3359bf62e80a8f398a3467424b90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654835"
---
# <a name="csharelocknhsharelock-method"></a>CShareLockLOCK::ShareLock (método)

Obtiene un bloqueo compartido.

## <a name="syntax"></a>Sintaxis


```C++
void ShareLock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cada llamada a **ShareLock** debe emparejarse con exactamente una llamada a [**ShareUnlock**](csharelocknh--shareunlock.md). Solo un subproceso que llama correctamente a **ShareLock** puede llamar a **ShareUnlock**; De lo contrario, puede producirse un interbloqueo.

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ShareUnlock**](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
