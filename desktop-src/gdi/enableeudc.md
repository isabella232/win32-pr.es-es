---
description: Esta función habilita o deshabilita la compatibilidad con los caracteres definidos por el usuario final (EUDC).
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: EnableEUDC función)
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
ms.openlocfilehash: 755ce2e0a659593b17487e86e28f5d454e48122c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984975"
---
# <a name="enableeudc-function"></a>EnableEUDC función)

Esta función habilita o deshabilita la compatibilidad con los caracteres definidos por el usuario final (EUDC).

## <a name="syntax"></a>Sintaxis


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fEnableEUDC* \[ de\]
</dt> <dd>

Valor booleano que se establece en **true** para habilitar EUDC y en **false** para deshabilitar EUDC.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Si se deshabilita EUDC, si se intentan mostrar los caracteres de EUDC, se producirán glifos que faltan o que son incorrectos.

Durante la sesión múltiple, esta función solo afecta a la sesión actual.

Se recomienda usar esta función con Windows XP SP2 o posterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Biblioteca<br/>                  | <dl> <dt>Gdi32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



 

 




