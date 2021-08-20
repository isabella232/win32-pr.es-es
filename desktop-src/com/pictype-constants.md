---
title: Constantes PICTYPE (OleCtl.h)
description: Describa el tipo de un objeto de imagen devuelto por IPicture get Type, así como para describir el tipo de imagen en el miembro picType de la estructuraDESCDESC que se pasa a \_ OleCreatePictureIndirect.
ms.assetid: 79f10687-f0eb-4b5e-a1a9-9186dbd0b51f
topic_type:
- apiref
api_name:
- PICTYPE_UNINITIALIZED
- PICTYPE_NONE
- PICTYPE_BITMAP
- PICTYPE_METAFILE
- PICTYPE_ICON
- PICTYPE_ENHMETAFILE
api_location:
- OleCtl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa6ac7be72ba34616a1ae8d596efbad3af761760c8f5e5c2bfa5dc8362593748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567655"
---
# <a name="pictype-constants"></a>Constantes PICTYPE

Describa el tipo de un objeto de imagen devuelto por [**IPicture::get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), así como para describir el tipo de imagen en el **miembro picType** de la estructura [**DEDESC QUE**](/windows/win32/api/olectl/ns-olectl-pictdesc) se pasa a [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).



| Constante o valor                                                                                                                                                                                                                                  | Descripción                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <dt>**PICTYPE \_ UNINITIALIZED**</dt> <dt>(-1)</dt> </dl> | El objeto de imagen no está inicializado actualmente. Este valor solo es válido como valor devuelto de [**IPicture::get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) y no es válido con la [**estructura DEDESC.**](/windows/win32/api/olectl/ns-olectl-pictdesc)<br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <dt>**PICTYPE \_ NONE**</dt> <dt>0</dt> </dl>                               | Se creará un nuevo objeto de imagen sin un estado inicializado. Este valor solo es válido en la [**estructura DEDESC.**](/windows/win32/api/olectl/ns-olectl-pictdesc)<br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <dt>**PICTYPE \_ BITMAP**</dt> <dt>1</dt> </dl>                         | El tipo de imagen es un mapa de bits. Cuando este valor se produce en la [**estructura PKDESC,**](/windows/win32/api/olectl/ns-olectl-pictdesc) significa que el **campo bmp** de esa estructura contiene los parámetros de inicialización pertinentes.<br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <dt>**PICTYPE \_ METAFILE**</dt> <dt>2</dt> </dl>                   | El tipo de imagen es un metarchivo. Cuando este valor se produce en la [**estructuraDESCDESC,**](/windows/win32/api/olectl/ns-olectl-pictdesc) significa que el **campo wmf** de esa estructura contiene los parámetros de inicialización pertinentes.<br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <dt>**PICTYPE \_ ICONO**</dt> <dt>3</dt> </dl>                               | El tipo de imagen es un icono. Cuando este valor se produce en la [**estructuraDESCDESC,**](/windows/win32/api/olectl/ns-olectl-pictdesc) significa que el campo **de icono** de esa estructura contiene los parámetros de inicialización pertinentes.<br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <dt>**PICTYPE \_ ENHMETAFILE**</dt> <dt>4</dt> </dl>          | El tipo de imagen es un metarchivo mejorado. Cuando este valor se produce en la [**estructuraDESCDESC,**](/windows/win32/api/olectl/ns-olectl-pictdesc) significa que el campo **emf** de esa estructura contiene los parámetros de inicialización pertinentes.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>OleCtl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPicture::get \_ (Tipo)**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[**PICDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





