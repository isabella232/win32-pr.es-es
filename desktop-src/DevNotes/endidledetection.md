---
description: Finaliza la supervisión de la inactividad.
ms.assetid: 26e52341-77cd-46cd-8b32-e786dfac870e
title: Función EndIdleDetection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: a2ba6732b9221d4d4d43e670d0d42d39363d50dffc0d2d4b0daf378b10dd292e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691415"
---
# <a name="endidledetection-function"></a>Función EndIdleDetection

\[Esta función no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use **la función GetLastInputInfo.**\]

Finaliza la supervisión de la inactividad.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI EndIdleDetection(
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

Devuelve **TRUE** si la función se realiza correctamente; de lo contrario, devuelve **FALSE**.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) Esta función no se exporta por nombre; especifique el ordinal 4 al llamar **a GetProcAddress**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
