---
title: TF_SS_ constantes (Msctf.h)
description: Las constantes SS \ de TF, definidas antes del tiempo de ejecución en la \_ estructura DE ESTADO de \_ \_ TF, describen los estados de documento estáticos.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476333"
---
# <a name="tf_ss_-constants"></a>Constantes \_ de TF \_ \* SS

Las constantes de TF SS, definidas antes del tiempo de ejecución en la \_ \_ \* estructura TF [**\_ STATUS,**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) describen los estados de documento estáticos.



| Constante o valor                                                                                                                                                                                                                                                                              | Descripción                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TF_SS_DISJOINTSEL"></span><span id="tf_ss_disjointsel"></span><dl> <dt>**TF \_ SS \_ DISJOINTSEL**</dt> <dt>( TS \_ SS \_ DISJOINTSEL )</dt> </dl>                                     | El documento admite varias selecciones.<br/>                                                          |
| <span id="TF_SS_REGIONS"></span><span id="tf_ss_regions"></span><dl> <dt>**TF \_ REGIONES \_ DE SS**</dt> <dt>( REGIONES DE \_ SS DE \_ TS )</dt> </dl>                                                     | El documento puede contener varias regiones.<br/>                                                          |
| <span id="TF_SS_TRANSITORY"></span><span id="tf_ss_transitory"></span><dl> <dt>**TF \_ SS \_ TRANSITORY**</dt> <dt>( TS \_ SS \_ TRANSITORY )</dt> </dl>                                         | Se espera que el documento tenga un ciclo de uso corto.<br/>                                               |
| <span id="TF_SS_TKBAUTOCORRECTENABLE"></span><span id="tf_ss_tkbautocorrectenable"></span><dl> <dt>**TF \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>( TS \_ SS \_ TKBAUTOCORRECTENABLE )</dt> </dl> | **A partir de Windows 8:** El documento admite la autocorrección proporcionada por el teclado táctil.<br/>   |
| <span id="TF_SS_TKBPREDICTIONENABLE"></span><span id="tf_ss_tkbpredictionenable"></span><dl> <dt>**TF \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>( \_ TS SS \_ TKBPREDICTIONENABLE )</dt> </dl>     | **A partir de Windows 8:** El documento admite sugerencias de texto proporcionadas por el teclado táctil.<br/> |



## <a name="remarks"></a>Observaciones

El **miembro dwStaticFlags** de la estructura TF \_ STATUS usa estas constantes.

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

[**TF \_ STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> </dl>

 

