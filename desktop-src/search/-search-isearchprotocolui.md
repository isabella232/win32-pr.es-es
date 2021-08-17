---
description: Proporciona un método para invocar objetos ISearchItem.
ms.assetid: b52fd64b-b03a-4d02-a64f-201f6b7d5045
title: Interfaz ISearchProtocolUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4794c0a2de43c08645af5ea7d44d0dbd872fe6fc88c33f5fcdb830955fc594be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463020"
---
# <a name="isearchprotocolui-interface"></a>Interfaz ISearchProtocolUI

Proporciona un método para invocar objetos [**ISearchItem.**](-search-isearchitem.md) El host de protocolo llama a los métodos de esta interfaz al procesar direcciones URL del recopilador. El controlador de protocolo implementa el protocolo para acceder a un origen de contenido en su formato nativo y esta interfaz implementa un controlador de protocolo personalizado para expandir los orígenes de datos que se pueden indexar.

## <a name="members"></a>Miembros

La **interfaz ISearchProtocolUI** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ISearchProtocolUI** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ISearchProtocolUI** tiene estos métodos.



| Método                                                                       | Descripción                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSearchItemForUrl**](-search-isearchprotocolui-getsearchitemforurl.md) | Obtiene el elemento de búsqueda de los datos especificados. Se llama a este método una vez por cada dirección URL procesada por el recopilador y recupera un puntero al [**objeto ISearchItem.**](-search-isearchitem.md) <br/> |



 

## <a name="remarks"></a>Comentarios

La **interfaz ISearchProtocolUI** solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede ser necesario usar la interfaz **ISearchProtocolUI** y las SIGUIENTES API: las interfaces [**IItemPreviewerExt,**](-search-iitempreviewerext.md) [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem,**](-search-isearchitem.md) la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



 

 
