---
title: Constantes de TF_SD_ (msctf. h)
description: Las constantes de TF \_ SD \_ \ describen el estado del documento.
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
ms.openlocfilehash: 12ed0d68c8a8afd9299b908eb81a04a31fbd3d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149960"
---
# <a name="tf_sd_-constants"></a>Constantes de TF \_ SD \_ \*

Las constantes de TF \_ SD \_ \* describen el estado del documento.



| Constante o valor                                                                                                                                                                                                                              | Descripción                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TF_SD_READONLY"></span><span id="tf_sd_readonly"></span><dl> <dt>**TF \_ SD \_ ReadOnly**</dt> <dt>(TS \_ SD \_ ReadOnly)</dt> </dl> | El documento es de solo lectura y no se puede modificar.<br/> |
| <span id="TF_SD_LOADING"></span><span id="tf_sd_loading"></span><dl> <dt>**TF \_ \_carga de SD**</dt> <dt>( \_ \_ carga SD de TS)</dt> </dl>     | El documento se está cargando y puede estar incompleto.<br/>    |



## <a name="remarks"></a>Observaciones

El miembro **dwDynamicFlags** de la estructura de [ \_ Estado de TF](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) utiliza estas constantes.

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

[Estado de TF \_](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> <dt>

[Constantes de TS \_ SD \_ \*](ts-sd--constants.md)
</dt> <dt>

[ITfContextOwner:: GetStatus](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getstatus)
</dt> <dt>

[ITfContextOwnerServices:: OnStatusChange](/windows/desktop/api/Msctf/nf-msctf-itfcontextownerservices-onstatuschange)
</dt> <dt>

[ITextStoreACP:: GetStatus](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getstatus)
</dt> <dt>

[ITfStatusSunk:: OnStatusChange](/windows/desktop/api/Msctf/nf-msctf-itfstatussink-onstatuschange)
</dt> </dl>

 

