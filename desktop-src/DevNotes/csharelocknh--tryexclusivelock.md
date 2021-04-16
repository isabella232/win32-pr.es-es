---
description: Obtiene un bloqueo de forma exclusiva si ningún otro lo mantiene actualmente.
ms.assetid: d655b89c-f2c8-4965-a21b-f539b1598296
title: 'CShareLockNH:: TryExclusiveLock (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.TryExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8465e247807c4229821acef552e0786a5604a3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649745"
---
# <a name="csharelocknhtryexclusivelock-method"></a>CShareLockNH:: TryExclusiveLock (método)

Obtiene un bloqueo de forma exclusiva si ningún otro lo mantiene actualmente.

## <a name="syntax"></a>Sintaxis


```C++
BOOL TryExclusiveLock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si la función se ejecuta correctamente; de lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
