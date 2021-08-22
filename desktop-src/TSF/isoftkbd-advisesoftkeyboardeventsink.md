---
title: Método ISoftKbd AdviseSoftKeyboardEventSink (Softkbdc.h)
description: El método ISoftKbd AdviseSoftKeyboardEventSink instala un receptor de eventos de teclado soft para controlar las notificaciones OnKeySelection desde el teclado soft.
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- Método AdviseSoftKeyboardEventSink Text Services Framework
- Método AdviseSoftKeyboardEventSink Text Services Framework , interfaz ISoftKbd
- Interfaz ISoftKbd Text Services Framework método , AdviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.AdviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a3a734e66bb319bb7e24b6ca3b27299f984f33b98772c1cc446c40e3f27426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877992"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a>ISoftKbd::AdviseSoftKeyboardEventSink (método)

El **método ISoftKbd::AdviseSoftKeyboardEventSink** instala un receptor de eventos de teclado soft para controlar las notificaciones OnKeySelection desde el teclado suave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AdviseSoftKeyboardEventSink(
  [in]  DWORD    dwKeyboardId,
  [in]  REFIID   riid,
  [in]  IUnknown *punk,
  [out] DWORD    *pdwCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwKeyboardId* \[ En\]
</dt> <dd>

Identificador del teclado suave.

</dd> <dt>

*riid* \[ En\]
</dt> <dd>

Identificador de interfaz para la interfaz del receptor.

</dd> <dt>

*así como* \[ En\]
</dt> <dd>

Puntero a [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) para la interfaz de receptor especificada por *riid*. Este parámetro no se puede establecer en **NULL.**

</dd> <dt>

*pdwCookie* \[ out\]
</dt> <dd>

Puntero al búfer en el que este método recupera la "cookie" de teclado soft usada para la conexión al cliente. La cookie debe ser única para cada conexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Valor                                                                                        | Descripción                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Método realizado correctamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o varios parámetros no son válidos.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::UnadviseSoftKeyboardEventSink**](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

