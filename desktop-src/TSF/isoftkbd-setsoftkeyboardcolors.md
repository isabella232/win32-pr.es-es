---
title: Método ISoftKbd SetSoftKeyboardColors (Softkbdc.h)
description: El método ISoftKbd SetSoftKeyboardColors establece el color del teclado suave para el tipo de color especificado.
ms.assetid: 1abbff35-a5ef-4119-9367-60b6e0961c59
keywords:
- Método SetSoftKeyboardColors Text Services Framework
- Método SetSoftKeyboardColors Text Services Framework , interfaz ISoftKbd
- Interfaz ISoftKbd Text Services Framework método , SetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38357331db2440c35ca7557d08c97729fde9c9f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361805"
---
# <a name="isoftkbdsetsoftkeyboardcolors-method"></a>ISoftKbd::SetSoftKeyboardColors (método)

El **método ISoftKbd::SetSoftKeyboardColors** establece el color del teclado suave para el tipo de color especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSoftKeyboardColors(
  [in] COLORTYPE colorType,
  [in] COLORREF  Color
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*colorType* \[ En\]
</dt> <dd>

Valor que especifica el tipo de color para el teclado suave. Los valores posibles se definen para la [**enumeración COLORTYPE.**](/windows/win32/api/icm/ne-icm-colortype)

</dd> <dt>

*Color* \[ En\]
</dt> <dd>

Valor [**COLORREF**](/windows/desktop/gdi/colorref) de 32 bits que especifica un color RGB.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Método realizado correctamente.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno de los parámetros no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::GetSoftKeyboardColors**](isoftkbd-getsoftkeyboardcolors.md)
</dt> <dt>

[**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> </dl>

 

