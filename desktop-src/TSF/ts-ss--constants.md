---
title: TS_SS_ constantes (Textstor.h)
description: Las constantes SS \ de TS, definidas antes del tiempo de ejecución en la \_ \_ estructura TS \_ STATUS, describen los estados de documento estáticos.
ms.assetid: 17264527-946a-4648-a4eb-30db751602ab
topic_type:
- apiref
api_name:
- TS_SS_DISJOINTSEL
- TS_SS_REGIONS
- TS_SS_TRANSITORY
- TS_SS_NOHIDDENTEXT
- TS_SS_TKBAUTOCORRECTENABLE
- TS_SS_TKBPREDICTIONENABLE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfb3468b90427bf29e1e16f746fff03ba163ac67513667f241baee9f533615fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950071"
---
# <a name="ts_ss_-constants"></a>Constantes \_ de SS de TS \_ \*

Las constantes de SS de TS, definidas antes del tiempo de ejecución en la \_ \_ \* [**estructura TS \_ STATUS,**](/windows/desktop/api/Textstor/ns-textstor-ts_status) describen los estados de documento estáticos.



| Constante o valor                                                                                                                                                                                                                                                      | Descripción                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TS_SS_DISJOINTSEL"></span><span id="ts_ss_disjointsel"></span><dl> <dt>**TS \_ SS \_ DISJOINTSEL**</dt> <dt>( 0x1 )</dt> </dl>                             | El documento admite varias selecciones.<br/>                                                          |
| <span id="TS_SS_REGIONS"></span><span id="ts_ss_regions"></span><dl> <dt>**TS \_ \_REGIONES DE SS**</dt> <dt>( 0x2 )</dt> </dl>                                         | El documento puede contener varias regiones.<br/>                                                          |
| <span id="TS_SS_TRANSITORY"></span><span id="ts_ss_transitory"></span><dl> <dt>**TS \_ SS \_ TRANSITORY**</dt> <dt>( 0x4 )</dt> </dl>                                | Se espera que el documento tenga un ciclo de uso corto.<br/>                                               |
| <span id="TS_SS_NOHIDDENTEXT"></span><span id="ts_ss_nohiddentext"></span><dl> <dt>**TS \_ SS \_ NOHIDDENTEXT**</dt> <dt>( 0x8 )</dt> </dl>                          | El documento nunca contendrá texto oculto.<br/>                                                        |
| <span id="TS_SS_TKBAUTOCORRECTENABLE"></span><span id="ts_ss_tkbautocorrectenable"></span><dl> <dt>**TS \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>( 0x10 )</dt> </dl> | **A partir de Windows 8:** El documento admite la autocorrección proporcionada por el teclado táctil.<br/>   |
| <span id="TS_SS_TKBPREDICTIONENABLE"></span><span id="ts_ss_tkbpredictionenable"></span><dl> <dt>**TS \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>( 0x20 )</dt> </dl>    | **A partir de Windows 8:** El documento admite sugerencias de texto proporcionadas por el teclado táctil.<br/> |



## <a name="remarks"></a>Comentarios

El **miembro dwStaticFlags** de la **estructura TS \_ STATUS** usa estas constantes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                         |
| Header<br/>                   | <dl> <dt>Textstor.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Textstor.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ESTADO DE \_ TS**](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[**TF \_ STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> </dl>

 

