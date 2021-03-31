---
title: Constantes de TF_SS_ (msctf. h)
description: Las constantes de TF \_ SS \_ \, definidas antes del tiempo de ejecución en la estructura de estado de TF \_ , describen los Estados de documento estático.
ms.assetid: 371aeeda-f081-4506-ba51-79c6a8bc8768
topic_type:
- apiref
api_name:
- TF_SS_DISJOINTSEL
- TF_SS_REGIONS
- TF_SS_TRANSITORY
- TF_SS_TKBAUTOCORRECTENABLE
- TF_SS_TKBPREDICTIONENABLE
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1028b78e74ed10c572feb904baa8ec395087ee3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079476"
---
# <a name="tf_ss_-constants"></a>Constantes de TF \_ SS \_ \*

Las constantes de TF \_ SS \_ \* , definidas antes del tiempo de ejecución en la estructura de [**\_ Estado de TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) , describen los Estados de documento estático.



| Constante o valor                                                                                                                                                                                                                                                                              | Descripción                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TF_SS_DISJOINTSEL"></span><span id="tf_ss_disjointsel"></span><dl> <dt>**TF \_ SS \_ DISJOINTSEL**</dt> <dt>(TS \_ SS \_ DISJOINTSEL)</dt> </dl>                                     | El documento admite selecciones múltiples.<br/>                                                          |
| <span id="TF_SS_REGIONS"></span><span id="tf_ss_regions"></span><dl> <dt>**TF \_ \_regiones de SS**</dt> <dt>(regiones de TS \_ SS \_ )</dt> </dl>                                                     | El documento puede contener varias regiones.<br/>                                                          |
| <span id="TF_SS_TRANSITORY"></span><span id="tf_ss_transitory"></span><dl> <dt>**TF \_ SS \_ transitorio**</dt> <dt>(TS \_ SS \_ transitorio)</dt> </dl>                                         | Se espera que el documento tenga un ciclo de uso breve.<br/>                                               |
| <span id="TF_SS_TKBAUTOCORRECTENABLE"></span><span id="tf_ss_tkbautocorrectenable"></span><dl> <dt>**TF \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>(TS \_ SS \_ TKBAUTOCORRECTENABLE)</dt> </dl> | **A partir de Windows 8:** El documento admite la corrección automática proporcionada por el teclado táctil.<br/>   |
| <span id="TF_SS_TKBPREDICTIONENABLE"></span><span id="tf_ss_tkbpredictionenable"></span><dl> <dt>**TF \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>(TS \_ SS \_ TKBPREDICTIONENABLE)</dt> </dl>     | **A partir de Windows 8:** El documento admite las sugerencias de texto que proporciona el teclado táctil.<br/> |



## <a name="remarks"></a>Observaciones

El miembro **dwStaticFlags** de la estructura de estado de TF \_ utiliza estas constantes.

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

[**Estado de TF \_**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> </dl>

 

