---
description: La función GetFrameMacType devuelve el tipo MAC del marco.
ms.assetid: 8d3da770-1392-4638-a267-32c2dae289b0
title: Función GetFrameMacType (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b85accc64a6e29424e3f65d070bafcf29bb3ec0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173585"
---
# <a name="getframemactype-function"></a>Función GetFrameMacType

La **función GetFrameMacType** devuelve el tipo MAC del marco.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI GetFrameMacType(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ En\]
</dt> <dd>

Identificador del marco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el tipo MAC del marco, que puede tener uno de los siguientes valores.

-   TIPO DE MAC \_ \_ DESCONOCIDO
-   ETHERNET \_ DE TIPO \_ MAC
-   TOKENRING \_ DE \_ TIPO MAC
-   FDDI \_ DE TIPO \_ MAC

## <a name="remarks"></a>Observaciones

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función GetFrameMacType.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




