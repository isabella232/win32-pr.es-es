---
title: Método ISoftKbd GetSoftKeyboardTextFont (Softkbdc. h)
description: El método ISoftKbd GetSoftKeyboardTextFont recupera la fuente de texto utilizada por un teclado en pantalla.
ms.assetid: 73239359-70b4-47d6-abc5-9fee279ed3a6
keywords:
- Método GetSoftKeyboardTextFont marco de trabajo de servicios de texto
- Método GetSoftKeyboardTextFont marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método GetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce939347042415a9060459102cd8a56665ac2de0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150809"
---
# <a name="isoftkbdgetsoftkeyboardtextfont-method"></a>ISoftKbd:: GetSoftKeyboardTextFont (método)

El método **ISoftKbd:: GetSoftKeyboardTextFont** recupera la fuente de texto utilizada por un teclado en pantalla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoftKeyboardTextFont(
  [out] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pLogFont* \[ enuncia\]
</dt> <dd>

Puntero a un búfer en el que este método recupera una estructura [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que define la fuente del texto para el teclado en pantalla.

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

[**ISoftKbd::SetSoftKeyboardTextFont**](isoftkbd-setsoftkeyboardtextfont.md)
</dt> </dl>

 

