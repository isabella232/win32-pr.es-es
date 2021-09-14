---
title: TS_SD_ constantes (Textstor.h)
description: Las constantes de TS \_ SD \_ \ describen los estados de documento dinámicos que usa una aplicación en tiempo de ejecución.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068782"
---
# <a name="ts_sd_-constants"></a>Constantes \_ sd \_ \* de TS

Las constantes de TS \_ SD \_ \* describen los estados de documento dinámicos que usa una aplicación en tiempo de ejecución.



| Constante o valor                                                                                                                                                                                                                                              | Descripción                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TS_SD_READONLY"></span><span id="ts_sd_readonly"></span><dl> <dt>**TS \_ SD \_ READONLY**</dt> <dt>( 0x1 )</dt> </dl>                              | El documento es de solo lectura y no se puede modificar.<br/> |
| <span id="TS_SD_LOADING"></span><span id="ts_sd_loading"></span><dl> <dt>**TS \_ SD \_ LOADING**</dt> <dt>( 0x2 )</dt> </dl>                                 | El documento se está cargando y puede estar incompleto.<br/>  |
| <span id="TS_SD_MASKALL"></span><span id="ts_sd_maskall"></span><dl> <dt>**TS \_ SD \_ MASKALL**</dt> <dt>( TS SD \_ \_ READONLY \| TS SD LOADING \_ \_ )</dt> </dl> | El documento es de solo lectura y se carga.<br/>       |



## <a name="remarks"></a>Observaciones

El **miembro dwDynamicFlags** de la [estructura TS \_ STATUS](/windows/desktop/api/Textstor/ns-textstor-ts_status) usa estas constantes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Textstor.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ESTADO DE \_ TS](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[Constantes \_ de TF SD \_ \*](tf-sd--constants.md)
</dt> </dl>

 

 





