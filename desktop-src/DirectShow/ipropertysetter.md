---
description: La interfaz IPropertySetter establece las propiedades en un efecto o transición en DirectShow Editing Services (DES). Para usar esta interfaz, cree una instancia de un objeto establecedor de propiedad (CLSID PropertySetter) y asócialo a un efecto o transición llamando al método \_ IAMTimelineObj::SetPropertySetter. Para obtener más información, vea Trabajar con efectos y transiciones. Normalmente, una aplicación solo debe llamar al método IPropertySetter::ClearProps para borrar las propiedades existentes y el método IPropertySetter::AddProp para agregar nuevas propiedades. Otros componentes de DES llaman a los demás métodos de esta interfaz.
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: Interfaz IPropertySetter (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c6dc32c25c85893eeb2e9872bcf67be974489ec82fdd4d09c19a2341f6867ade
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831035"
---
# <a name="ipropertysetter-interface"></a>Interfaz IPropertySetter

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IPropertySetter` interfaz establece propiedades en un efecto o transición en DirectShow Editing [Services](directshow-editing-services.md) (DES).

Para usar esta interfaz, cree una instancia de un objeto establecedor de propiedad (CLSID PropertySetter) y asócialo a un efecto o transición llamando al método \_ [**IAMTimelineObj::SetPropertySetter.**](iamtimelineobj-setpropertysetter.md) Para obtener más información, [vea Trabajar con efectos y transiciones.](working-with-effects-and-transitions.md)

Normalmente, una aplicación solo debe llamar al método [**IPropertySetter::ClearProps**](ipropertysetter-clearprops.md) para borrar las propiedades existentes y al método [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) para agregar nuevas propiedades. Otros componentes de DES llaman a los demás métodos de esta interfaz.

## <a name="members"></a>Miembros

La **interfaz IPropertySetter** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IPropertySetter** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IPropertySetter** tiene estos métodos.



| Método                                               | Descripción                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddProp**](ipropertysetter-addprop.md)           | Agrega una propiedad al setter de propiedad, con una matriz de pares de tiempo-valor que definen el valor de la propiedad durante un intervalo de tiempo.<br/> |
| [**ClearProps**](ipropertysetter-clearprops.md)     | Borra todos los datos de propiedad del setter de propiedad.<br/>                                                                                 |
| [**CloneProps**](ipropertysetter-cloneprops.md)     | Clona un conjunto de propiedades de este establecedor de propiedades y las agrega a un nuevo establecedor de propiedades.<br/>                                       |
| [**FreeProps**](ipropertysetter-freeprops.md)       | Libera los recursos asignados por el [**método IPropertySetter::GetProps.**](ipropertysetter-getprops.md)<br/>                             |
| [**GetProps**](ipropertysetter-getprops.md)         | Recupera las propiedades establecidas en este objeto con sus valores correspondientes.<br/>                                                      |
| [**LoadFromBlob**](ipropertysetter-loadfromblob.md) | Carga los datos de propiedad desde un formato de persistencia.<br/>                                                                                     |
| [**LoadXML**](ipropertysetter-loadxml.md)           | Carga los datos de propiedad expresados lenguaje de marcado extensible (XML).<br/>                                                                 |
| [**PrintXML**](ipropertysetter-printxml.md)         | Convierte los datos de propiedad en una cadena XML.<br/>                                                                                         |
| [**SaveToBlob**](ipropertysetter-savetoblob.md)     | Guarda los datos de propiedad en un formato de persistencia.<br/>                                                                                   |
| [**SetProps**](ipropertysetter-setprops.md)         | Establece las propiedades del objeto de destino en el estado adecuado para la hora especificada.<br/>                                          |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
