---
title: Método ISoftKbd UnadviseSoftKeyboardEventSink (Softkbdc.h)
description: El método ISoftKbd UnadviseSoftKeyboardEventSink quita un receptor de eventos de teclado flexible.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- Método UnadviseSoftKeyboardEventSink Text Services Framework
- Método UnadviseSoftKeyboardEventSink Text Services Framework , interfaz ISoftKbd
- Interfaz ISoftKbd Text Services Framework , método UnadviseSoftKeyboardEventSink
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
ms.openlocfilehash: 2a77129d1b5df024964af4ab19318963708d4b3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361798"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a>ISoftKbd::UnadviseSoftKeyboardEventSink (método)

El **método ISoftKbd::UnadviseSoftKeyboardEventSink** quita un receptor de eventos de teclado flexible.

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

Identificador del cliente que posee el receptor de eventos de teclado flexible. Este valor se pasó cuando el receptor de eventos se instaló mediante [ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                                   | Descripción                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Método realizado correctamente.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | El *parámetro tid* no es válido.<br/>                    |
| <dl> <dt>**CONNECT \_ E \_ NOCONNECTION**</dt> </dl> | No se encontró el receptor de asesoramiento identificado por *tid.*<br/> |



 

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

[ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





