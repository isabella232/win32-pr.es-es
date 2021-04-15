---
title: Constantes de TS_SHIFT_ (Textstor. h)
description: La \_ \_ interfaz IAnchor utiliza las constantes Shift de TS para manipular el texto oculto y el recuento de caracteres.
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
ms.openlocfilehash: 98f3a11463aea1633079d771bf6a8b333475865e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422331"
---
# <a name="ts_shift_-constants"></a>\_Constantes de desplazamiento de TS \_ \*

La \_ \_ \* interfaz **IAnchor** utiliza las constantes de desplazamiento de TS para manipular el texto oculto y el recuento de caracteres.



| Constante o valor                                                                                                                                                                                                                                       | Descripción                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_SHIFT_COUNT_HIDDEN"></span><span id="ts_shift_count_hidden"></span><dl> <dt>**TS \_ Número de TURNOs \_ \_ oculto**</dt> <dt>(0x1)</dt> </dl> | Especifica que el delimitador se desplazará al límite de la región siguiente, incluido el límite de una región de texto oculto. Si no se establece, el delimitador se desplazará más allá de cualquier texto oculto adyacente hasta que se encuentre una región de texto visible.<br/> |
| <span id="TS_SHIFT_HALT_HIDDEN"></span><span id="ts_shift_halt_hidden"></span><dl> <dt>**TS \_ DESPLAZAMIENTO \_ detenido \_ oculto**</dt> <dt>(0X2)</dt> </dl>    | No se utiliza.<br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_HALT_VISIBLE"></span><span id="ts_shift_halt_visible"></span><dl> <dt>**TS \_ Mayús \_ Halt \_ visible**</dt> <dt>(0x4)</dt> </dl> | No se utiliza.<br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_COUNT_ONLY"></span><span id="ts_shift_count_only"></span><dl> <dt>**TS \_ \_ \_ Solo recuento de desplazamiento**</dt> <dt>(0x8)</dt> </dl>       | No se desplaza el delimitador.<br/>                                                                                                                                                                                                           |



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

[IAnchor::ShiftRegion](/windows/desktop/api/Textstor/nf-textstor-ianchor-shiftregion)
</dt> </dl>

 

 





