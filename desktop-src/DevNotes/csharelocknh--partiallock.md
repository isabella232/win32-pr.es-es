---
description: Impide que más de un subproceso complete la adquisición de un bloqueo.
ms.assetid: 9cdcc6d5-b2f1-4c88-b859-1c15a80e70a9
title: CShareLockGNI::P artialLock (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 7eae3f0eb57d534ea352b7d1c1e0834ef54dfb42460dfe7b2edc4f6fc07fa013
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162349"
---
# <a name="csharelocknhpartiallock-method"></a>CShareLockGNI::P artialLock (método)

Impide que más de un subproceso complete la adquisición de un bloqueo.

## <a name="syntax"></a>Sintaxis


```C++
void PartialLock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Mientras **PartialLock está** en vigor, otros subprocesos que llaman [**a ShareLock**](csharelocknh--sharelock.md) pueden entrar en el bloqueo.

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
