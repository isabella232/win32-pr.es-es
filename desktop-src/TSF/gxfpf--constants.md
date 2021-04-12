---
title: Constantes de GXFPF_ (Textstor. h)
description: GXFPF \_ \ constantes especifican la posición de carácter que se va a devolver en función de las coordenadas de pantalla del punto en relación con un rectángulo de selección de caracteres.
ms.assetid: e69e5a4c-65e6-4d9b-8cb0-962524aa5d39
topic_type:
- apiref
api_name:
- GXFPF_ROUND_NEAREST
- GXFPF_NEAREST
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d2dfc5ce874a7c4ce5b205c9b92436040aa60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489706"
---
# <a name="gxfpf_-constants"></a>Constantes de GXFPF \_ \*

\_ \* Las constantes GXFPF especifican la posición de carácter que se va a devolver en función de las coordenadas de pantalla del punto en relación con un rectángulo de selección de caracteres.



| Constante o valor                                                                                                                                                                                                                                | Descripción                                                                                                                                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GXFPF_ROUND_NEAREST"></span><span id="gxfpf_round_nearest"></span><dl> <dt>**GXFPF \_ REDONDEO \_ más próximo**</dt> <dt>(0x1)</dt> </dl> | Si las coordenadas de pantalla del punto están contenidas en un cuadro de límite de caracteres, la posición de carácter devuelta es el borde de límite más próximo a las coordenadas de pantalla del punto.<br/> |
| <span id="GXFPF_NEAREST"></span><span id="gxfpf_nearest"></span><dl> <dt>**GXFPF \_ MÁS próximo**</dt> <dt>(0X2)</dt> </dl>                    | Si las coordenadas de pantalla del punto no están contenidas en un cuadro de límite de caracteres, se devuelve la posición del carácter más cercano.<br/>                                                      |



## <a name="remarks"></a>Observaciones

Los parámetros *dwFlags* de los métodos [ITextStoreACP:: GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) y [ITfContextOwner:: GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) usan estas constantes.

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

[ITextStoreACP:: GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)
</dt> <dt>

[ITfContextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)
</dt> </dl>

 

 





