---
title: Método ISoftKbd UnadviseSoftKeyboardEventSink (Softkbdc.h)
description: El método ISoftKbd UnadviseSoftKeyboardEventSink quita un receptor de eventos de teclado soft.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- Método UnadviseSoftKeyboardEventSink Text Services Framework
- Método UnadviseSoftKeyboardEventSink Text Services Framework interfaz , ISoftKbd
- Interfaz ISoftKbd Text Services Framework método , UnadviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.UnadviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90552c09e47d8a51f413f0588b12c8da5d44e665a6a5a51a79dc31717c6d56c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877115"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a>ISoftKbd::UnadviseSoftKeyboardEventSink (método)

El **método ISoftKbd::UnadviseSoftKeyboardEventSink** quita un receptor de eventos de teclado soft.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tid* \[ En\]
</dt> <dd>

Identificador del cliente que posee el receptor de eventos de teclado flexible. Este valor se pasó cuando se instaló el receptor de eventos [mediante ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Valor                                                                                                   | Descripción                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Método realizado correctamente.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | El *parámetro tid* no es válido.<br/>                    |
| <dl> <dt>**CONNECT \_ E \_ NOCONNECTION**</dt> </dl> | No se encontró el receptor de aviso identificado por *tid.*<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





