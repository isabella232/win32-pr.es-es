---
title: Constantes de TS_LF_ (Textstor. h)
description: Las \_ constantes LF \_ de TS \ especifican el tipo de bloqueo del documento.
ms.assetid: f0bb6ef9-a8fc-4331-9210-6c5ba1721a73
topic_type:
- apiref
api_name:
- TS_LF_SYNC
- TS_LF_READ
- TS_LF_READWRITE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6240511fd95e91a7f22477f631178dfab528f1e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685844"
---
# <a name="ts_lf_-constants"></a>\_Constantes de LF de TS \_ \*

Las \_ constantes LF \_ \* de TS especifican el tipo de bloqueo del documento.



| Constante o valor                                                                                                                                                                                                                    | Descripción                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span id="TS_LF_SYNC"></span><span id="ts_lf_sync"></span><dl> <dt>**TS \_ \_Sincronización de LF**</dt> <dt>(0x1)</dt> </dl>                | El documento tiene un bloqueo sincrónico si esta marca se combina con otras marcas.<br/> |
| <span id="TS_LF_READ"></span><span id="ts_lf_read"></span><dl> <dt>**TS \_ \_Lectura de LF**</dt> <dt>(0X2)</dt> </dl>                | El documento tiene un bloqueo de solo lectura y no se puede modificar.<br/>                      |
| <span id="TS_LF_READWRITE"></span><span id="ts_lf_readwrite"></span><dl> <dt>**TS \_ LF \_ ReadWrite**</dt> <dt>(0x6)</dt> </dl> | El documento tiene un bloqueo de lectura/escritura y se puede modificar.<br/>                        |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Bloqueos de documento](document-locks.md)
</dt> <dt>

[ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[ITextStoreACPSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[ITextStoreAnchor::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[ITextStoreAnchorSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> </dl>

 

 





