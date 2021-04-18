---
title: Constantes de TS_AS_ (Textstor. h)
description: Las marcas siguientes especifican los eventos que llaman a los métodos AdviseSink.
ms.assetid: 8f406b67-f846-4712-b4be-811dbcc6ad55
topic_type:
- apiref
api_name:
- TS_AS_TEXT_CHANGE
- TS_AS_SEL_CHANGE
- TS_AS_LAYOUT_CHANGE
- TS_AS_ATTR_CHANGE
- TS_AS_STATUS_CHANGE
- TS_AS_ALL_SINKS
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b36bdc2c3b559693503b2a8e408a0782855f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686131"
---
# <a name="ts_as_-constants"></a>TS \_ como \_ \* constantes

Las marcas siguientes especifican los eventos que llaman a los métodos **AdviseSink** .



| Constante o valor                                                                                                                                                                                                                                                                                                                                         | Descripción                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="TS_AS_TEXT_CHANGE"></span><span id="ts_as_text_change"></span><dl> <dt>**TS \_ Como \_ \_ cambio de texto**</dt> <dt>(0x1)</dt> </dl>                                                                                                               | El texto se cambia en el documento.<br/>                          |
| <span id="TS_AS_SEL_CHANGE"></span><span id="ts_as_sel_change"></span><dl> <dt>**TS \_ COMO \_ \_ cambio SEL**</dt> <dt>(0X2)</dt> </dl>                                                                                                                  | Texto seleccionado en el documento.<br/>                         |
| <span id="TS_AS_LAYOUT_CHANGE"></span><span id="ts_as_layout_change"></span><dl> <dt>**TS \_ Como \_ \_ cambio de diseño**</dt> <dt>(0x4)</dt> </dl>                                                                                                         | Se cambia el diseño del documento.<br/>                    |
| <span id="TS_AS_ATTR_CHANGE"></span><span id="ts_as_attr_change"></span><dl> <dt>**TS \_ Como \_ \_ cambio de atributo**</dt> <dt>(0x8)</dt> </dl>                                                                                                               | Se cambian los atributos del documento.<br/>                |
| <span id="TS_AS_STATUS_CHANGE"></span><span id="ts_as_status_change"></span><dl> <dt>**TS \_ Como \_ \_ cambio de estado**</dt> <dt>(0x10)</dt> </dl>                                                                                                        | Se cambia el estado del documento.<br/>                    |
| <span id="TS_AS_ALL_SINKS"></span><span id="ts_as_all_sinks"></span><dl> <dt>**TS \_ Dado que \_ todos los \_ receptores**</dt> <dt>(TS \_ as \_ Text cambian de \_ \| TS \_ como \_ SEL \_ Change TS as \| \_ \_ relayout Change TS as ATTR Change \_ \| \_ \_ \_ \| TS \_ as \_ status Change \_ )</dt> </dl> | Uno de los cuatro eventos anteriores se produjo en el documento.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



 

 





