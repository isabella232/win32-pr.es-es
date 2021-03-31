---
description: Proporciona métodos que definen la interacción entre una interfaz de usuario (UI) y los objetos de espacio de nombres de búsqueda creados por el indizador.
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
ms.openlocfilehash: c6c0fd5b534c13f8fae2e6759645ac812fc3986c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423731"
---
# <a name="isearchitem-interface"></a>Interfaz ISearchItem

Proporciona métodos que definen la interacción entre una interfaz de usuario (UI) y los objetos de espacio de nombres de búsqueda creados por el indizador.

## <a name="members"></a>Miembros

La interfaz **ISearchItem** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISearchItem** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ISearchItem** tiene estos métodos.



| Método                                                         | Descripción                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentFolder**](-search-isearchitem-getparentfolder.md) | Obtiene el objeto **ISearchItem** si la dirección URL representa un origen de datos de Shell real (también conocido como una extensión de espacio de nombres de Shell).<br/> |
| [**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))     | Obtiene el objeto de interfaz de usuario (UI) de **ISearchItem**.<br/>                                                                        |



 

## <a name="remarks"></a>Observaciones

[**ISearchItem:: GetParentFolder**](-search-isearchitem-getparentfolder.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz **ISearchItem** y las siguientes API: las interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)y [**ISearchProtocolUI**](-search-isearchprotocolui.md) , la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Búsqueda en el escritorio de Windows (WDS) 3,0<br/>          |



 

 
