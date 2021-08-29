---
description: Cierra el subárbol del Registro sin conexión especificado y libera la memoria asignada para el subárbol.
ms.assetid: e30a92dd-8533-406f-ad63-96306f125d78
title: Función ORCloseHive (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4852112ff1de3d0650c78b07a2ebbba780e89a485a176cf610fd2cf7b1fa234f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824835"
---
# <a name="orclosehive-function"></a>Función ORCloseHive

Cierra el subárbol del Registro sin conexión especificado y libera la memoria asignada para el subárbol.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ORCloseHive(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Identificador* \[ En\]
</dt> <dd>

Identificador de la clave raíz del subárbol del Registro sin conexión que se va a cerrar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror.h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM SYSTEM para obtener una descripción genérica del \_ \_ error.

## <a name="remarks"></a>Comentarios

La **función ORCloseHive** libera toda la memoria asignada por las funciones del Registro sin conexión en nombre del subárbol especificado.

Para conservar los cambios en el subárbol, llame a la [**función ORSaveHive**](orsavehive.md) antes de llamar a **ORCloseHive**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows Biblioteca del Registro sin conexión versión 1.0 o posterior<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| Archivo DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**OROpenHive**](oropenhive.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> </dl>

 

 
