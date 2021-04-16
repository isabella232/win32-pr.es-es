---
title: Constantes de TS_SD_ (Textstor. h)
description: Las constantes de TS \_ SD \_ \ describen los Estados de documentos dinámicos usados por una aplicación en tiempo de ejecución.
ms.assetid: fb673e42-bee7-484e-872a-d709d5ca12f2
topic_type:
- apiref
api_name:
- TS_SD_READONLY
- TS_SD_LOADING
- TS_SD_MASKALL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565bc97b9fa2d1474f1ba36cd8137e63125541e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685948"
---
# <a name="ts_sd_-constants"></a>Constantes de TS \_ SD \_ \*

Las constantes de TS \_ SD \_ \* describen los Estados de documentos dinámicos usados por una aplicación en tiempo de ejecución.



| Constante o valor                                                                                                                                                                                                                                              | Descripción                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TS_SD_READONLY"></span><span id="ts_sd_readonly"></span><dl> <dt>**TS \_ SD \_ ReadOnly**</dt> <dt>(0x1)</dt> </dl>                              | El documento es de solo lectura y no se puede modificar.<br/> |
| <span id="TS_SD_LOADING"></span><span id="ts_sd_loading"></span><dl> <dt>**TS \_ \_Carga de SD**</dt> <dt>(0X2)</dt> </dl>                                 | El documento se está cargando y podría estar incompleto.<br/>  |
| <span id="TS_SD_MASKALL"></span><span id="ts_sd_maskall"></span><dl> <dt>**TS \_ SD \_ MASKALL**</dt> <dt>(TS \_ SD \_ ReadOnly \| TS \_ SD \_ loading)</dt> </dl> | El documento es tanto de solo lectura como de carga.<br/>       |



## <a name="remarks"></a>Observaciones

El miembro **dwDynamicFlags** de la estructura de [ \_ Estado de TS](/windows/desktop/api/Textstor/ns-textstor-ts_status) utiliza estas constantes.

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

[Estado de TS \_](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[Constantes de TF \_ SD \_ \*](tf-sd--constants.md)
</dt> </dl>

 

 





