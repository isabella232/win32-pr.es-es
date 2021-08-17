---
description: Proporciona métodos que definen la interacción entre una interfaz de usuario (UI) y los objetos de espacio de nombres Search creados por el indexador.
ms.assetid: e48c9e5b-9b15-4bc1-91ef-81ba7a05bfbd
title: Interfaz ISearchItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem
api_type:
- COM
api_location: ''
ms.openlocfilehash: de3769f869838cd3a6660229a452ea7fbd96f943ac7421523c523662da205dac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863963"
---
# <a name="isearchitem-interface"></a>Interfaz ISearchItem

Proporciona métodos que definen la interacción entre una interfaz de usuario (UI) y los objetos de espacio de nombres Search creados por el indexador.

## <a name="members"></a>Miembros

La **interfaz ISearchItem** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ISearchItem** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ISearchItem** tiene estos métodos.



| Método                                                         | Descripción                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentFolder**](-search-isearchitem-getparentfolder.md) | Obtiene el **objeto ISearchItem** si la dirección URL representa un origen de datos de Shell real (también conocido como extensión de espacio de nombres de Shell).<br/> |
| [**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))     | Obtiene el objeto de interfaz de usuario (UI) **de ISearchItem**.<br/>                                                                        |



 

## <a name="remarks"></a>Comentarios

[**ISearchItem::GetParentFolder**](-search-isearchitem-getparentfolder.md) solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede ser necesario usar la interfaz **ISearchItem** y las siguientes API: las interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)e [**ISearchProtocolUI,**](-search-isearchprotocolui.md) la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



 

 
