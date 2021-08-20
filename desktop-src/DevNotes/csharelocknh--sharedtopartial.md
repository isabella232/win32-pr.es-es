---
description: Cambia un bloqueo compartido a un bloqueo parcial.
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: CShareLockGNI::SharedToPartial (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.SharedToPartial
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8f2cc895786655754a3fcf56c6efe745467c12328867b1dc021a257ba1519652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162210"
---
# <a name="csharelocknhsharedtopartial-method"></a>CShareLockGNI::SharedToPartial (método)

Cambia un bloqueo compartido a un bloqueo parcial.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se obtiene el bloqueo parcial; de lo contrario, devuelve **FALSE** y el bloqueo permanece en modo compartido.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
