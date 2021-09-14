---
description: Define métodos para obtener información sobre las propiedades de un elemento de búsqueda. Esta interfaz solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.
ms.assetid: 0fef34c5-f20f-475a-9223-5cb73079c842
title: Interfaz IItemPropertyBag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4da3db21947de6d35ef5e848499efc7f22633f7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262556"
---
# <a name="iitempropertybag-interface"></a>Interfaz IItemPropertyBag

Define métodos para obtener información sobre las propiedades de un elemento de búsqueda. Esta interfaz solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.

## <a name="members"></a>Members

La **interfaz IItemPropertyBag** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IItemPropertyBag** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IItemPropertyBag** tiene estos métodos.



| Método                                                      | Descripción                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85)) | Obtiene un recuento del número de propiedades del bolsa de propiedades.<br/>                     |
| [**GetPropertyInfo**](iitempropertybag-getpropertyinfo.md) | Obtiene la información necesaria para leer o guardar las propiedades en el bolsa de propiedades.<br/> |
| [**Lectura**](iitempropertybag-read.md)                       | Hace que una o varias propiedades se lean desde el bolsa de propiedades.<br/>                   |
| [**Escritura**](iitempropertybag-write.md)                     | Hace que una o varias propiedades se guarden en el bolsa de propiedades.<br/>                  |



 

## <a name="remarks"></a>Observaciones

La **interfaz IItemPropertyBag** solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede ser necesario usar la interfaz **IItemPropertyBag** y las siguientes API: las interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISearchItem,**](-search-isearchitem.md) las estructuras [**LINKINFO**](-search-linkinfo.md) y [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) y la enumeración [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



 

 
