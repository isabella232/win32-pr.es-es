---
title: TS_SHIFT_ constantes (Textstor.h)
description: La interfaz \_ IAnchor usa las constantes mayús\ de TS para la manipulación del texto oculto y \_ el recuento de caracteres.
ms.assetid: 93329238-f6e8-432e-9167-550a02b33b46
topic_type:
- apiref
api_name:
- TS_SHIFT_COUNT_HIDDEN
- TS_SHIFT_HALT_HIDDEN
- TS_SHIFT_HALT_VISIBLE
- TS_SHIFT_COUNT_ONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b0ff9a4fc8fa93ecc386c09670cb33cdc4d86049d13dcff5ea708692746a1ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118873590"
---
# <a name="ts_shift_-constants"></a>Constantes \_ MAYÚS \_ \* de TS

La interfaz \_ \_ \* **IAnchor** usa las constantes de TS Shift para la manipulación del recuento de caracteres y texto oculto.



| Constante o valor                                                                                                                                                                                                                                       | Descripción                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_SHIFT_COUNT_HIDDEN"></span><span id="ts_shift_count_hidden"></span><dl> <dt>**TS \_ MAYÚS \_ COUNT \_ HIDDEN**</dt> <dt>( 0x1 )</dt> </dl> | Especifica que el delimitador se desplazará al siguiente límite de región, incluido el límite de una región de texto oculta. Si no se establece, el delimitador se desplazará más allá de cualquier texto oculto adyacente hasta que se encuentra una región de texto visible.<br/> |
| <span id="TS_SHIFT_HALT_HIDDEN"></span><span id="ts_shift_halt_hidden"></span><dl> <dt>**TS \_ MAYÚS \_ HALT \_ HIDDEN**</dt> <dt>( 0x2 )</dt> </dl>    | No se usa.<br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_HALT_VISIBLE"></span><span id="ts_shift_halt_visible"></span><dl> <dt>**TS \_ MAYÚS \_ HALT \_ VISIBLE**</dt> <dt>( 0x4 )</dt> </dl> | No se usa.<br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_COUNT_ONLY"></span><span id="ts_shift_count_only"></span><dl> <dt>**TS \_ MAYÚS \_ COUNT \_ ONLY**</dt> <dt>( 0x8 )</dt> </dl>       | El delimitador no se desplaza.<br/>                                                                                                                                                                                                           |



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

[IAnchor::ShiftRegion](/windows/desktop/api/Textstor/nf-textstor-ianchor-shiftregion)
</dt> </dl>

 

 





