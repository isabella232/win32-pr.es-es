---
title: TF_SD_ constantes (Msctf.h)
description: Las constantes \_ de TF SD \ \_ describen el estado del documento.
ms.assetid: 953d39cd-8af1-4c86-8fb8-8b8ec917c631
topic_type:
- apiref
api_name:
- TF_SD_READONLY
- TF_SD_LOADING
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3763af61afaf96c5024cf5adecd07f9491e4d43ee0f34f3d376d866a45146383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950584"
---
# <a name="tf_sd_-constants"></a>Constantes \_ de TF SD \_ \*

Las constantes \_ DE \_ \* TF describen el estado del documento.



| Constante o valor                                                                                                                                                                                                                              | Descripción                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TF_SD_READONLY"></span><span id="tf_sd_readonly"></span><dl> <dt>**TF \_ SD \_ READONLY**</dt> <dt>( TS SD \_ \_ READONLY )</dt> </dl> | El documento es de solo lectura y no se puede modificar.<br/> |
| <span id="TF_SD_LOADING"></span><span id="tf_sd_loading"></span><dl> <dt>**TF \_ SD \_ LOADING**</dt> <dt>( TS SD LOADING \_ \_ )</dt> </dl>     | El documento se está cargando y puede estar incompleto.<br/>    |



## <a name="remarks"></a>Comentarios

El **miembro dwDynamicFlags** de la [estructura TF \_ STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) usa estas constantes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                      |
| Header<br/>                   | <dl> <dt>Msctf.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[TF \_ STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> <dt>

[Constantes \_ sd \_ \* de TS](ts-sd--constants.md)
</dt> <dt>

[ITfContextOwner::GetStatus](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getstatus)
</dt> <dt>

[ITfContextOwnerServices::OnStatusChange](/windows/desktop/api/Msctf/nf-msctf-itfcontextownerservices-onstatuschange)
</dt> <dt>

[ITextStoreACP::GetStatus](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getstatus)
</dt> <dt>

[ITfStatusSunk::OnStatusChange](/windows/desktop/api/Msctf/nf-msctf-itfstatussink-onstatuschange)
</dt> </dl>

 

