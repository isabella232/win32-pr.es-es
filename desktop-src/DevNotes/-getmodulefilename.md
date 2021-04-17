---
description: Obtiene la ruta de acceso del módulo.
ms.assetid: ff632357-8d4a-4de4-a69a-0be9e380639d
title: _GetModuleFileName función)
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
ms.openlocfilehash: 5bf18e8baac62de6474f4ce1e48a0ae115ced778
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661160"
---
# <a name="_getmodulefilename-function"></a>\_GetModuleFileName, función

\[Esta función es un contenedor de la función **GetModuleFileName** . Esta función puede modificarse o no estar disponible en el futuro. Las aplicaciones deben llamar a **GetModuleFileName** directamente.\]

Obtiene la ruta de acceso del módulo. Vea [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).

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

 

 
