---
description: Indica la versión de CTL3D que se está ejecutando actualmente.
ms.assetid: 38c0842c-417f-4ca1-acc2-3bbadf45c804
title: Función Ctl3dGetVer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dGetVer
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: f29963020290686521d5e3bd165d2c8fac6e5e0c96f34552ad11f725d95567cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654505"
---
# <a name="ctl3dgetver-function"></a>Función Ctl3dGetVer

Indica la versión de CTL3D que se está ejecutando actualmente.

## <a name="syntax"></a>Sintaxis


```C++
WORD Ctl3dGetVer(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor que contiene el número de versión principal en el byte de orden superior y el número de versión secundaria en el byte de orden bajo.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
