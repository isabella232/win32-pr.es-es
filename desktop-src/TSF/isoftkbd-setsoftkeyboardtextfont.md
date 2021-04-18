---
title: Método ISoftKbd SetSoftKeyboardTextFont (Softkbdc. h)
description: El método ISoftKbd SetSoftKeyboardTextFont establece la fuente de texto utilizada por un teclado en pantalla.
ms.assetid: 14705723-4592-40ef-9ebb-1c44c10c3cda
keywords:
- Método SetSoftKeyboardTextFont marco de trabajo de servicios de texto
- Método SetSoftKeyboardTextFont marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método SetSoftKeyboardTextFont
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686112"
---
# <a name="isoftkbdsetsoftkeyboardtextfont-method"></a>ISoftKbd:: SetSoftKeyboardTextFont (método)

El método **ISoftKbd:: SetSoftKeyboardTextFont** establece la fuente de texto utilizada por un teclado en pantalla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSoftKeyboardTextFont(
  [in] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pLogFont* \[ de\]
</dt> <dd>

Puntero a una estructura [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que define la fuente del texto para el teclado en pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Método realizado correctamente.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *pLogFont* no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::GetSoftKeyboardTextFont**](isoftkbd-getsoftkeyboardtextfont.md)
</dt> </dl>

 

