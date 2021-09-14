---
title: TS_ATTR_ constantes (Textstor.h)
description: Las constantes ATTR \ de \_ \_ TS se usan para obtener y cambiar los valores de los atributos del documento. Estas constantes forman valores posibles de marcas de campo de bits en los métodos ITextStoreACP e ITextStoreAnchor.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068794"
---
# <a name="ts_attr_-constants"></a>Constantes \_ ATTR de \_ \* TS

Las constantes \_ ATTR de \_ \* TS se usan para obtener y cambiar los valores de los atributos del documento. Estas constantes forman valores posibles de marcas de campo de bits en los métodos [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) [e ITextStoreAnchor.](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)



| Constante o valor                                                                                                                                                                                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_ATTR_FIND_BACKWARDS"></span><span id="ts_attr_find_backwards"></span><dl> <dt>**TS \_ ATTR \_ FIND \_ BACKWARDS**</dt> <dt>( 0x1 )</dt> </dl>        | Busque hacia atrás desde el carácter inicial o la posición delimitadora de la posición en la que se produce una transición en un valor de atributo de documento. El valor predeterminado es buscar hacia delante.<br/>                                                                                                                                                                                    |
| <span id="TS_ATTR_FIND_WANT_OFFSET"></span><span id="ts_attr_find_want_offset"></span><dl> <dt>**TS \_ ATTR \_ FIND \_ WANT \_ OFFSET**</dt> <dt>( 0x2 )</dt> </dl> | Devuelve el número de caracteres entre el carácter de inicio o la posición delimitadora **(acpStart** en [ITextStoreACP::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) o **paStart** en [ITextStoreAnchor::FindNextAttrTransition)](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) y la posición en la que se produce una transición de atributo.<br/> |
| <span id="TS_ATTR_FIND_UPDATESTART"></span><span id="ts_attr_find_updatestart"></span><dl> <dt>**TS \_ ATTR \_ FIND \_ UPDATESTART**</dt> <dt>( 0x4 )</dt> </dl>  | Usado por [ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) para colocar el delimitador de entrada en la siguiente transición de atributo, si se encuentra uno. De lo contrario, el delimitador de entrada no se modifica.<br/>                                                                                                                             |
| <span id="TS_ATTR_FIND_WANT_VALUE"></span><span id="ts_attr_find_want_value"></span><dl> <dt>**TS \_ ATTR \_ FIND \_ WANT \_ VALUE**</dt> <dt>( 0x8 )</dt> </dl>    | Cargue los valores de atributo de documento admitidos en la [ \_ estructura ATTRVAL de TS.](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)<br/>                                                                                                                                                                                                                                                              |
| <span id="TS_ATTR_FIND_WANT_END"></span><span id="ts_attr_find_want_end"></span><dl> <dt>**TS \_ ATTR \_ FIND \_ WANT \_ END**</dt> <dt>( 0x10 )</dt> </dl>         | Usado por [ITextStoreACP::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) e [ITextStoreAnchor::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) para obtener los valores de atributo del documento que terminan en la posición de carácter o delimitador especificada.<br/>               |
| <span id="TS_ATTR_FIND_HIDDEN"></span><span id="ts_attr_find_hidden"></span><dl> <dt>**TS \_ ATTR \_ FIND \_ HIDDEN**</dt> <dt>( 0x20 )</dt> </dl>                | Reservado.<br/>                                                                                                                                                                                                                                                                                                                                               |



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

[TS \_ ATTRID](ts-attrid.md)
</dt> <dt>

[ATTRVAL de TS \_](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> <dt>

[ITextStoreACP::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[ITextStoreACP::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[ITextStoreAnchor::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> </dl>

 

 





