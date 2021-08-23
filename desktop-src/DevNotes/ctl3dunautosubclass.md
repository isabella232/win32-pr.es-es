---
description: Desactiva la subclases automática.
ms.assetid: 85e5689f-6805-4aad-b97c-aa496e315900
title: Función Ctl3dUnAutoSubclass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: ca7980705ca93ad88b7c9e535abe59c3cdcc2e011130c843f0e89a533ce97599
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654475"
---
# <a name="ctl3dunautosubclass-function"></a>Función Ctl3dUnAutoSubclass

Desactiva la subclases automática.

## <a name="syntax"></a>Sintaxis


```C++
BOOL Ctl3dUnAutoSubclass(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la función se realiza correctamente; de lo contrario, devuelve **FALSE**.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
