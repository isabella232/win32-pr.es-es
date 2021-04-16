---
description: Finaliza la supervisión de inactividad.
ms.assetid: 26e52341-77cd-46cd-8b32-e786dfac870e
title: EndIdleDetection función)
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
ms.openlocfilehash: e50679c53123ad140324f7d159ef938367c02af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649857"
---
# <a name="endidledetection-function"></a>EndIdleDetection función)

\[Esta función no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use la función **GetLastInputInfo** .\]

Finaliza la supervisión de inactividad.

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

Devuelve **true** si la función se ejecuta correctamente; de lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) . Esta función no se exporta por nombre; Especifique el ordinal 4 al llamar a **GetProcAddress**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
