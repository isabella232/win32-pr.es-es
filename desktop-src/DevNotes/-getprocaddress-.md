---
description: Obtiene la dirección de una función de un archivo DLL.
ms.assetid: e425948c-5588-4a4f-994c-4e608af18439
title: _Función GetProcAddress_
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetProcAddress_
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: d35d623ff7c7873534bd835c138dba490274e5caddf839fc71765cda59b9f00f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053205"
---
# <a name="_getprocaddress_-function"></a>\_Función \_ GetProcAddress

\[Esta función es un contenedor sobre la **función GetProcAddress.** Esta función puede modificarse o no estar disponible en el futuro. Las aplicaciones deben **llamar directamente a GetProcAddress.**\]

Obtiene la dirección de una función de un archivo DLL. Vea [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).

## <a name="syntax"></a>Sintaxis


```C++
FARPROC _GetProcAddress_(
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

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 
