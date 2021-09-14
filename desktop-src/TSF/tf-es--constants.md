---
title: TF_ES_ constantes (Msctf.h)
description: Las siguientes son constantes usadas por el método RequestEditSession de ITfContext.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374815"
---
# <a name="tf_es_-constants"></a>Constantes \_ de TF ES \_ \*

Las siguientes son constantes usadas por el [método ITfContext::RequestEditSession.](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession)



| Constante o valor                                                                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                             |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_ES_ASYNCDONTCARE"></span><span id="tf_es_asyncdontcare"></span><dl> <dt>**TF \_ ES \_ ASYNCDONTCARE**</dt> <dt>( 0 )</dt> </dl> | La sesión de edición puede producirse de forma sincrónica o asincrónica, a discreción del administrador. El administrador intentará programar una sesión de edición sincrónica para mejorar el rendimiento. Este valor no se puede combinar con los valores de TF \_ ES \_ ASYNC o TF \_ ES \_ SYNC.<br/>                                                                         |
| <span id="TF_ES_SYNC"></span><span id="tf_es_sync"></span><dl> <dt>**TF \_ ES \_ SYNC**</dt> <dt>( 0x1 )</dt> </dl>                          | La sesión de edición debe ser sincrónica o se producirá un error en la solicitud (con TF \_ E \_ SYNCHRONOUS). Esta marca solo debe usarse en situaciones documentadas (como el control de pulsaciones de teclas) en las que se puede esperar que se pueda realizar correctamente. De lo contrario, es probable que se producirá un error en la llamada. Este valor no se puede combinar con los valores \_ de TF ES \_ ASYNCDONTCARE o TF \_ ES \_ ASYNC.<br/> |
| <span id="TF_ES_READ"></span><span id="tf_es_read"></span><dl> <dt>**TF \_ ES \_ READ**</dt> <dt>( 0x2 )</dt> </dl>                          | Solicita acceso de solo lectura al contexto.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="TF_ES_READWRITE"></span><span id="tf_es_readwrite"></span><dl> <dt>**TF \_ ES \_ READWRITE**</dt> <dt>( 0x6 )</dt> </dl>           | Solicita acceso de lectura y escritura al contexto.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="TF_ES_ASYNC"></span><span id="tf_es_async"></span><dl> <dt>**TF \_ ES \_ ASYNC**</dt> <dt>( 0x8 )</dt> </dl>                       | La sesión de edición debe ser asincrónica o se producirá un error en la solicitud. Este valor no se puede combinar con los valores \_ TF ES \_ ASYNCDONTCARE o TF \_ ES \_ SYNC.<br/>                                                                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                      |
| Encabezado<br/>                   | <dl> <dt>Msctf.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ITfContext::RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession)
</dt> </dl>

 

 





