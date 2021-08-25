---
description: Obtiene la ruta de acceso del módulo.
ms.assetid: ff632357-8d4a-4de4-a69a-0be9e380639d
title: _GetModuleFileName función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetModuleFileName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: a10ff54d7f118dc71e12cdb5b29e28d3b3dd6e60c7b51c263af8c62c1264968c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911925"
---
# <a name="_getmodulefilename-function"></a>\_Función GetModuleFileName

\[Esta función es un contenedor sobre la **función GetModuleFileName.** Esta función puede modificarse o no estar disponible en el futuro. Las aplicaciones deben **llamar directamente a GetModuleFileName.**\]

Obtiene la ruta de acceso del módulo. Vea [**GetModuleFileName.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)

## <a name="syntax"></a>Sintaxis


```C++
DWORD _GetModuleFileName(
    ...
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
