---
description: Proporciona métodos para proporcionar la configuración del explorador. La interfaz IItemPreviewerExt solo se admite en Windows XP y Windows Server 2003, y ya no debe usarse.
ms.assetid: d7d6cbb0-18bf-4e68-b7b4-307cadbced5c
title: Interfaz IItemPreviewerExt
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
ms.openlocfilehash: 820ddfdf73d36a7cba968a721872b1e9fb33a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000996"
---
# <a name="iitempreviewerext-interface"></a>Interfaz IItemPreviewerExt

Proporciona métodos para proporcionar la configuración del explorador. La interfaz **IItemPreviewerExt** solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.

## <a name="members"></a>Miembros

La interfaz **IItemPreviewerExt** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IItemPreviewerExt** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IItemPreviewerExt** tiene estos métodos.



| Método                                                                               | Descripción                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md)               | Permite la extensión a contenido enriquecido para una propiedad. <br/>                            |
| [**GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md)                   | Obtiene una parte del cuerpo relacionada para la inserción en el flujo MHTML de salida.<br/>              |
| [**ProcessTransformCommand**](-search-iitempreviewerext-processtransformcommand.md) | Permite el procesamiento de un comando de transformación que se encuentra en una plantilla de vista previa.<br/> |
| [**SuggestBrowserPolicy**](-search-iitempreviewerext-suggestbrowserpolicy.md)       | Sugiere la Directiva de seguridad que se va a aplicar al explorador.<br/>                        |



 

## <a name="remarks"></a>Observaciones

La interfaz **IItemPreviewerExt** solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz **IItemPreviewerExt** y las siguientes API: las interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) y [**ISearchItem**](-search-isearchitem.md) , la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Búsqueda en el escritorio de Windows (WDS) 3,0<br/>          |



 

 
