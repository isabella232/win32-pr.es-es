---
description: Proporciona métodos para proporcionar la configuración del explorador. La interfaz IItemPreviewerExt solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.
ms.assetid: d7d6cbb0-18bf-4e68-b7b4-307cadbced5c
title: IItemPreviewerExt (interfaz)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8a652e24b87655d7d5ae5f03a944e3e0a5e649c4e680f87c0b023d68407f6a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969754"
---
# <a name="iitempreviewerext-interface"></a>IItemPreviewerExt (interfaz)

Proporciona métodos para proporcionar la configuración del explorador. La **interfaz IItemPreviewerExt** solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.

## <a name="members"></a>Miembros

La **interfaz IItemPreviewerExt** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IItemPreviewerExt** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IItemPreviewerExt** tiene estos métodos.



| Método                                                                               | Descripción                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md)               | Permite que la extensión a contenido enriquecido para una propiedad. <br/>                            |
| [**GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md)                   | Obtiene una parte del cuerpo relacionada para insertarla en la secuencia MHTML de salida.<br/>              |
| [**ProcessTransformCommand**](-search-iitempreviewerext-processtransformcommand.md) | Permite el procesamiento de un comando de transformación encontrado en una plantilla de vista previa.<br/> |
| [**SuggestBrowserPolicy**](-search-iitempreviewerext-suggestbrowserpolicy.md)       | Sugiere la directiva de seguridad que se va a aplicar al explorador.<br/>                        |



 

## <a name="remarks"></a>Comentarios

La **interfaz IItemPreviewerExt** solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz **IItemPreviewerExt** y las SIGUIENTES API: las interfaces [**ISearchProtocolUI,**](-search-isearchprotocolui.md) [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem,**](-search-isearchitem.md) la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



 

 
