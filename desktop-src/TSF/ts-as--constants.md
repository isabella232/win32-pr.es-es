---
title: TS_AS_ constantes (Textstor.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068798"
---
# <a name="ts_as_-constants"></a>Constantes \_ as de TS \_ \*

Las marcas siguientes especifican los eventos que llaman a los **métodos AdviseSink.**



| Constante o valor                                                                                                                                                                                                                                                                                                                                         | Descripción                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="TS_AS_TEXT_CHANGE"></span><span id="ts_as_text_change"></span><dl> <dt>**TS \_ AS \_ TEXT \_ CHANGE**</dt> <dt>( 0x1 )</dt> </dl>                                                                                                               | El texto cambia en el documento.<br/>                          |
| <span id="TS_AS_SEL_CHANGE"></span><span id="ts_as_sel_change"></span><dl> <dt>**TS \_ AS \_ SEL \_ CHANGE**</dt> <dt>( 0x2 )</dt> </dl>                                                                                                                  | El texto está seleccionado en el documento.<br/>                         |
| <span id="TS_AS_LAYOUT_CHANGE"></span><span id="ts_as_layout_change"></span><dl> <dt>**TS \_ AS \_ LAYOUT \_ CHANGE**</dt> <dt>( 0x4 )</dt> </dl>                                                                                                         | Se cambia el diseño del documento.<br/>                    |
| <span id="TS_AS_ATTR_CHANGE"></span><span id="ts_as_attr_change"></span><dl> <dt>**TS \_ AS \_ ATTR \_ CHANGE**</dt> <dt>( 0x8 )</dt> </dl>                                                                                                               | Se cambian los atributos del documento.<br/>                |
| <span id="TS_AS_STATUS_CHANGE"></span><span id="ts_as_status_change"></span><dl> <dt>**TS \_ AS \_ STATUS \_ CHANGE**</dt> <dt>( 0x10 )</dt> </dl>                                                                                                        | Se cambia el estado del documento.<br/>                    |
| <span id="TS_AS_ALL_SINKS"></span><span id="ts_as_all_sinks"></span><dl> <dt>**TS \_ AS \_ ALL \_ SINKS**</dt> <dt>( TS AS TEXT CHANGE \_ \_ \_ \| TS AS \_ \_ SEL CHANGE \_ \| TS AS LAYOUT CHANGE \_ \_ \_ \| TS AS \_ \_ ATTR CHANGE \_ \| TS AS STATUS CHANGE \_ \_ \_ )</dt> </dl> | Uno de los cuatro eventos anteriores se produjo en el documento.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Textstor.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor.idl</dt> </dl> |



 

 





