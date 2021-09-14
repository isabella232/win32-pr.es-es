---
title: GXFPF_ constantes (Textstor.h)
description: GXFPF \ constantes especifican la posición de caracteres que se va a devolver en función de las coordenadas de pantalla del punto con \_ respecto a un cuadro de límite de caracteres.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243608"
---
# <a name="gxfpf_-constants"></a>Constantes GXFPF \_ \*

Las constantes GXFPF especifican la posición del carácter que se va a devolver en función de las coordenadas de pantalla del punto en \_ \* relación con un cuadro de límite de caracteres.



| Constante o valor                                                                                                                                                                                                                                | Descripción                                                                                                                                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GXFPF_ROUND_NEAREST"></span><span id="gxfpf_round_nearest"></span><dl> <dt>**GXFPF \_ ROUND \_ NEAREST**</dt> <dt>( 0x1 )</dt> </dl> | Si las coordenadas de pantalla del punto están contenidas en un cuadro de límite de caracteres, la posición de carácter devuelta es el borde delimitador más cercano a las coordenadas de pantalla del punto.<br/> |
| <span id="GXFPF_NEAREST"></span><span id="gxfpf_nearest"></span><dl> <dt>**GXFPF \_ NEAREST**</dt> <dt>( 0x2 )</dt> </dl>                    | Si las coordenadas de pantalla del punto no están contenidas en un cuadro de límite de caracteres, se devuelve la posición de caracteres más cercana.<br/>                                                      |



## <a name="remarks"></a>Observaciones

Los *parámetros dwflags* de los métodos [ITextStoreACP::GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) e [ITfContextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) usan estas constantes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Textstor.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ITextStoreACP::GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)
</dt> <dt>

[ITfContextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)
</dt> </dl>

 

 





