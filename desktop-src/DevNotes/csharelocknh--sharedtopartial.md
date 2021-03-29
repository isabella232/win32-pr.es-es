---
description: Cambia un bloqueo compartido a un bloqueo parcial.
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: 'CShareLockNH:: SharedToPartial (método)'
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
ms.openlocfilehash: a997c5a437063a4c55b74d837dc77fd506688158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660484"
---
# <a name="csharelocknhsharedtopartial-method"></a>CShareLockNH:: SharedToPartial (método)

Cambia un bloqueo compartido a un bloqueo parcial.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si se obtiene el bloqueo parcial; de lo contrario, devuelve **false** y el bloqueo permanece en modo compartido.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
