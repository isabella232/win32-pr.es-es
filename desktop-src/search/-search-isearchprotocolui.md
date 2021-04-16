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
ms.openlocfilehash: 3923ddaff014d393690be31c0e0ca2be94a3cb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705491"
---
# <a name="isearchprotocolui-interface"></a>Interfaz ISearchProtocolUI

Proporciona un método para invocar objetos [**ISearchItem**](-search-isearchitem.md) . El host del protocolo llama a los métodos de esta interfaz al procesar las direcciones URL del recopilador. El controlador de protocolo implementa el protocolo para tener acceso a un origen de contenido en su formato nativo y esta interfaz implementa un controlador de protocolo personalizado para expandir los orígenes de datos que se pueden indizar.

## <a name="members"></a>Miembros

La interfaz **ISearchProtocolUI** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISearchProtocolUI** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ISearchProtocolUI** tiene estos métodos.



| Método                                                                       | Descripción                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSearchItemForUrl**](-search-isearchprotocolui-getsearchitemforurl.md) | Obtiene el elemento de búsqueda para los datos especificados. Se llama a este método una vez por cada dirección URL procesada por el recopilador y recupera un puntero al objeto [**ISearchItem**](-search-isearchitem.md) . <br/> |



 

## <a name="remarks"></a>Observaciones

La interfaz **ISearchProtocolUI** solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz **ISearchProtocolUI** y las siguientes API: las interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) y [**ISearchItem**](-search-isearchitem.md) , la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Búsqueda en el escritorio de Windows (WDS) 3,0<br/>          |



 

 
