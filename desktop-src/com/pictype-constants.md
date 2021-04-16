---
title: Constantes PICTYPE (OleCtl. h)
description: Describa el tipo de un objeto de imagen tal y como lo devolvió el tipo IPicture Get \_ , así como para describir el tipo de imagen en el miembro picType de la estructura PICTDESC que se pasa a OleCreatePictureIndirect.
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
ms.openlocfilehash: bebf8ad8f678e9b6e463ade9f149b2e1d4bab529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695888"
---
# <a name="pictype-constants"></a>Constantes de PICTYPE

Describa el tipo de un objeto de imagen tal y como lo devolvió [**IPicture:: get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), así como para describir el tipo de imagen en el miembro **PicType** de la estructura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) que se pasa a [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).



| Constante o valor                                                                                                                                                                                                                                  | Descripción                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <dt>**PICTYPE \_ No INICIALIZAdo**</dt> <dt>(-1)</dt> </dl> | El objeto de imagen no está inicializado actualmente. Este valor solo es válido como valor devuelto de [**IPicture:: get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) y no es válido con la estructura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .<br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <dt>**PICTYPE \_ NINGUNO**</dt> <dt>0</dt> </dl>                               | Se creará un nuevo objeto de imagen sin un estado inicializado. Este valor solo es válido en la estructura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .<br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <dt>**PICTYPE \_ MAPA de bits**</dt> <dt>1</dt> </dl>                         | El tipo de imagen es un mapa de bits. Cuando este valor se produce en la estructura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa que el campo **BMP** de esa estructura contiene los parámetros de inicialización correspondientes.<br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <dt>**PICTYPE \_ METARCHIVO**</dt> <dt>2</dt> </dl>                   | El tipo de imagen es un metarchivo. Cuando este valor se produce en la estructura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa que el campo **WMF** de esa estructura contiene los parámetros de inicialización correspondientes.<br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <dt>**PICTYPE \_ ICONO**</dt> <dt>3</dt> </dl>                               | El tipo de imagen es un icono. Cuando este valor se produce en la estructura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa que el campo **Icon** de esa estructura contiene los parámetros de inicialización correspondientes.<br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <dt>**PICTYPE \_ ENHMETAFILE**</dt> <dt>4</dt> </dl>          | El tipo de imagen es un metarchivo mejorado. Cuando este valor se produce en la estructura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa que el campo **EMF** de esa estructura contiene los parámetros de inicialización correspondientes.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>OleCtl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPicture:: get ( \_ tipo)**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





