---
title: Método ISoftKbd SetSoftKeyboardTextFont (Softkbdc.h)
description: El método ISoftKbd SetSoftKeyboardTextFont establece la fuente de texto utilizada por un teclado suave.
ms.assetid: 14705723-4592-40ef-9ebb-1c44c10c3cda
keywords:
- Método SetSoftKeyboardTextFont Text Services Framework
- Método SetSoftKeyboardTextFont Text Services Framework , interfaz ISoftKbd
- Interfaz ISoftKbd Text Services Framework método , SetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff0a9adce61bc1a671d28c6e5d6ac5b6d329b42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361804"
---
# <a name="isoftkbdsetsoftkeyboardtextfont-method"></a>ISoftKbd::SetSoftKeyboardTextFont (método)

El **método ISoftKbd::SetSoftKeyboardTextFont** establece la fuente de texto utilizada por un teclado suave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSoftKeyboardTextFont(
  [in] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pLogFont* \[ En\]
</dt> <dd>

Puntero a una [**estructura LOGFONTW que**](/windows/win32/api/wingdi/ns-wingdi-logfonta) define la fuente de texto para el teclado suave.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Método realizado correctamente.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El *parámetro pLogFont* no es válido.<br/> |



 

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

[**ISoftKbd::GetSoftKeyboardTextFont**](isoftkbd-getsoftkeyboardtextfont.md)
</dt> </dl>

 

