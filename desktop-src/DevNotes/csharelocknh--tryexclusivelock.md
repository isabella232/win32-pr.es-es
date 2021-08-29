---
description: Obtiene un bloqueo exclusivamente si ningún otro lo contiene actualmente.
ms.assetid: d655b89c-f2c8-4965-a21b-f539b1598296
title: CShareLockLOCK::TryExclusiveLock (método)
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
ms.openlocfilehash: 28bd569c287b00cf6b0a146022ade6ce7f7bf29d5ced9eb5ef62341c873059c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654665"
---
# <a name="csharelocknhtryexclusivelock-method"></a>CShareLockLOCK::TryExclusiveLock (método)

Obtiene un bloqueo exclusivamente si ningún otro lo contiene actualmente.

## <a name="syntax"></a>Sintaxis


```C++
BOOL TryExclusiveLock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la función se realiza correctamente; de lo contrario, devuelve **FALSE**.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
