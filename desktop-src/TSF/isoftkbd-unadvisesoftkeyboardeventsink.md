---
title: Método ISoftKbd UnadviseSoftKeyboardEventSink (Softkbdc. h)
description: El método ISoftKbd UnadviseSoftKeyboardEventSink quita un receptor de eventos de teclado en pantalla.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- Método UnadviseSoftKeyboardEventSink marco de trabajo de servicios de texto
- Método UnadviseSoftKeyboardEventSink marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método UnadviseSoftKeyboardEventSink
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803241"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a>ISoftKbd:: UnadviseSoftKeyboardEventSink (método)

El método **ISoftKbd:: UnadviseSoftKeyboardEventSink** quita un receptor de eventos de teclado en pantalla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TID* \[ de\]
</dt> <dd>

Identificador del cliente que posee el receptor de eventos de teclado en pantalla. Este valor se pasó cuando se instaló el receptor de eventos mediante [ISoftKbd:: AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                                   | Descripción                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                    | Método realizado correctamente.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | El parámetro *TID* no es válido.<br/>                    |
| <dl> <dt>**CONECTAR \_ E \_ noconnection**</dt> </dl> | No se encontró el receptor de notificaciones identificado por *TID* .<br/> |



 

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

[ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





