---
title: Constantes de TS_ATTR_ (Textstor. h)
description: '\_Se usan las constantes de TS ATTR \_ \ para obtener y cambiar los valores de los atributos del documento. Estas constantes forman los valores posibles de las marcas de campo de bits en los métodos ITextStoreACP y ITextStoreAnchor.'
ms.assetid: e99a44ba-c41a-4dd7-9475-dd37159081fd
topic_type:
- apiref
api_name:
- TS_ATTR_FIND_BACKWARDS
- TS_ATTR_FIND_WANT_OFFSET
- TS_ATTR_FIND_UPDATESTART
- TS_ATTR_FIND_WANT_VALUE
- TS_ATTR_FIND_WANT_END
- TS_ATTR_FIND_HIDDEN
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa26b8a725475a3d88b07cce1dccd0ac7fa1a98e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491890"
---
# <a name="ts_attr_-constants"></a>\_Constantes de atributo de TS \_ \*

Las \_ constantes ATTR \_ \* de TS se utilizan para obtener y cambiar los valores de los atributos del documento. Estas constantes forman los valores posibles de las marcas de campo de bits en los métodos [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) y [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .



| Constante o valor                                                                                                                                                                                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_ATTR_FIND_BACKWARDS"></span><span id="ts_attr_find_backwards"></span><dl> <dt>**TS \_ ATTR \_ Buscar \_ hacia atrás**</dt> <dt>(0x1)</dt> </dl>        | Buscar hacia atrás desde el carácter inicial o la posición del delimitador para la posición en la que se produce una transición en un valor de atributo del documento. El valor predeterminado es buscar hacia delante.<br/>                                                                                                                                                                                    |
| <span id="TS_ATTR_FIND_WANT_OFFSET"></span><span id="ts_attr_find_want_offset"></span><dl> <dt>**TS \_ ATRIBUTO \_ busque \_ el \_ desplazamiento deseado**</dt> <dt>(0X2)</dt> </dl> | Devuelve el número de caracteres entre el carácter de inicio o la posición del delimitador (**acpStart** en [ITextStoreACP:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) o en el **Inicio** en [ITextStoreAnchor:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) y la posición en la que se produce la transición de un atributo.<br/> |
| <span id="TS_ATTR_FIND_UPDATESTART"></span><span id="ts_attr_find_updatestart"></span><dl> <dt>**TS \_ ATTR \_ Buscar \_ UPDATESTART**</dt> <dt>(0x4)</dt> </dl>  | Lo usa [ITextStoreAnchor:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) para colocar el delimitador de entrada en la siguiente transición de atributo, si se encuentra uno. De lo contrario, el delimitador de entrada no se modifica.<br/>                                                                                                                             |
| <span id="TS_ATTR_FIND_WANT_VALUE"></span><span id="ts_attr_find_want_value"></span><dl> <dt>**TS \_ ATTR \_ Buscar \_ \_ valor deseado**</dt> <dt>(0x8)</dt> </dl>    | Cargar los valores de atributo de documento admitidos en la estructura [ \_ ATTRVAL de TS](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) .<br/>                                                                                                                                                                                                                                                              |
| <span id="TS_ATTR_FIND_WANT_END"></span><span id="ts_attr_find_want_end"></span><dl> <dt>**TS \_ ATTR \_ Buscar \_ desea \_ Finalizar**</dt> <dt>(0x10)</dt> </dl>         | Lo usa [ITextStoreACP:: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) y [ITextStoreAnchor:: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) para obtener los valores de atributo del documento que terminan en el carácter o posición delimitador especificados.<br/>               |
| <span id="TS_ATTR_FIND_HIDDEN"></span><span id="ts_attr_find_hidden"></span><dl> <dt>**TS \_ ATTR \_ Buscar \_ oculto**</dt> <dt>(0x20)</dt> </dl>                | Reservado.<br/>                                                                                                                                                                                                                                                                                                                                               |



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

[ATTRID de TS \_](ts-attrid.md)
</dt> <dt>

[ATTRVAL de TS \_](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> <dt>

[ITextStoreACP:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[ITextStoreACP:: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[ITextStoreAnchor::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> </dl>

 

 





