---
description: Esta función habilita o deshabilita la compatibilidad con caracteres definidos por el usuario final (EUDC).
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: Función EnableEUDC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnableEUDC
api_type:
- DllExport
api_location:
- Gdi32.dll
ms.openlocfilehash: 5767be62d23e992223500bf7192fc89efe04f03288280c73445378e083cc1613
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117699480"
---
# <a name="enableeudc-function"></a>Función EnableEUDC

Esta función habilita o deshabilita la compatibilidad con caracteres definidos por el usuario final (EUDC).

## <a name="syntax"></a>Sintaxis


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fEnableEUDC* \[ En\]
</dt> <dd>

Valor booleano que se establece **en TRUE** para habilitar EUDC y en **FALSE** para deshabilitar EUDC.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

Si EUDC está deshabilitado, al intentar mostrar caracteres EUDC, faltan glifos o son negativos.

Durante la sesión múltiple, esta función solo afecta a la sesión actual.

Se recomienda usar esta función con Windows XP SP2 o posterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Biblioteca<br/>                  | <dl> <dt>Gdi32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



 

 




