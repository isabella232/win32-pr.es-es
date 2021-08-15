---
description: Obtiene el período de tiempo, en minutos, desde la última actividad del usuario.
ms.assetid: 2d1e68ad-6f65-4e64-afbf-505b2c9d3423
title: Función GetIdleMinutes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetIdleMinutes
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: d3397de5d792181958891eef9693d29b2d7d4e56f9bbc7f7e1cfef19171625b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404588"
---
# <a name="getidleminutes-function"></a>Función GetIdleMinutes

\[Esta función no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use **la función GetLastInputInfo.**\]

Obtiene el período de tiempo, en minutos, desde la última actividad del usuario.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI GetIdleMinutes(
   DWORD dwReserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwReserved* 
</dt> <dd>

Este parámetro debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de minutos desde la última actividad del usuario.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) Esta función no se exporta por nombre; especifique el ordinal 8 al llamar **a GetProcAddress**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
