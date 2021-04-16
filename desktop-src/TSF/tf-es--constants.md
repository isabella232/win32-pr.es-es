---
title: Constantes de TF_ES_ (msctf. h)
description: Las siguientes son constantes que usa el método ITfContext RequestEditSession.
ms.assetid: 5498329f-3302-4f66-bdec-cab7db0cdc0e
topic_type:
- apiref
api_name:
- TF_ES_ASYNCDONTCARE
- TF_ES_SYNC
- TF_ES_READ
- TF_ES_READWRITE
- TF_ES_ASYNC
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ed96adc1d6f6d66671e91f7a70bce856663e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686132"
---
# <a name="tf_es_-constants"></a>Constantes de TF \_ es \_ \*

Las siguientes son constantes que usa el método [ITfContext:: RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) .



| Constante o valor                                                                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                             |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_ES_ASYNCDONTCARE"></span><span id="tf_es_asyncdontcare"></span><dl> <dt>**TF \_ ES \_ ASYNCDONTCARE**</dt> <dt>(0)</dt> </dl> | La sesión de edición puede realizarse de forma sincrónica o asincrónica, a discreción del administrador. El administrador intentará programar una sesión de edición sincrónica para mejorar el rendimiento. Este valor no se puede combinar con los \_ valores de sincronización de TF es \_ Async o TF \_ es \_ .<br/>                                                                         |
| <span id="TF_ES_SYNC"></span><span id="tf_es_sync"></span><dl> <dt>**TF \_ \_Sincronización es**</dt> <dt>(0x1)</dt> </dl>                          | La sesión de edición debe ser sincrónica o se producirá un error en la solicitud (con TF \_ E \_ Synchronous). Esta marca solo se debe usar en situaciones documentadas (por ejemplo, el control de pulsaciones de teclas), donde se puede esperar que se realice correctamente. De lo contrario, es probable que se produzca un error en la llamada. Este valor no se puede combinar con los \_ valores de TF es \_ ASYNCDONTCARE o TF \_ es \_ Async.<br/> |
| <span id="TF_ES_READ"></span><span id="tf_es_read"></span><dl> <dt>**TF \_ ES \_ leída**</dt> <dt>(0X2)</dt> </dl>                          | Solicita acceso de solo lectura al contexto.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="TF_ES_READWRITE"></span><span id="tf_es_readwrite"></span><dl> <dt>**TF \_ ES \_ ReadWrite**</dt> <dt>(0x6)</dt> </dl>           | Solicita acceso de lectura/escritura al contexto.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="TF_ES_ASYNC"></span><span id="tf_es_async"></span><dl> <dt>**TF \_ S \_ Async**</dt> <dt>(0x8)</dt> </dl>                       | La sesión de edición debe ser asincrónica o se producirá un error en la solicitud. Este valor no se puede combinar con los \_ valores de sincronización TF es \_ ASYNCDONTCARE o TF \_ es \_ .<br/>                                                                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                      |
| Encabezado<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ITfContext::RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession)
</dt> </dl>

 

 





