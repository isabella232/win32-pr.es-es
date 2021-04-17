---
title: Método ISoftKbd AdviseSoftKeyboardEventSink (Softkbdc. h)
description: El método ISoftKbd AdviseSoftKeyboardEventSink instala un receptor de eventos de teclado en pantalla para controlar las notificaciones de OnKeySelection desde el teclado en pantalla.
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- Método AdviseSoftKeyboardEventSink marco de trabajo de servicios de texto
- Método AdviseSoftKeyboardEventSink marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método AdviseSoftKeyboardEventSink
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
ms.openlocfilehash: 6ab17de2104c6104b044f027152cfc45cca968b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422508"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a>ISoftKbd:: AdviseSoftKeyboardEventSink (método)

El método **ISoftKbd:: AdviseSoftKeyboardEventSink** instala un receptor de eventos de teclado en pantalla para controlar las notificaciones de OnKeySelection desde el teclado en pantalla.

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

*dwKeyboardId* \[ de\]
</dt> <dd>

Identificador del teclado en pantalla.

</dd> <dt>

*riid* \[ de\]
</dt> <dd>

Identificador de interfaz para la interfaz de receptor.

</dd> <dt>

*punk* \[ de\]
</dt> <dd>

Puntero a [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) para la interfaz de receptor especificada por *riid*. Este parámetro no se puede establecer en **null**.

</dd> <dt>

*pdwCookie* \[ enuncia\]
</dt> <dd>

Puntero al búfer en el que este método recupera la "cookie" de teclado blando utilizada para la conexión al cliente. La cookie debe ser única para cada conexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Método realizado correctamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o más parámetros no son válidos.<br/> |



 

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

[**ISoftKbd::UnadviseSoftKeyboardEventSink**](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

