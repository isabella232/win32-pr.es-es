---
description: 'La interfaz IPropertySetter establece propiedades en un efecto o transición en los servicios de edición de DirectShow (DES). Para usar esta interfaz, cree una instancia de un objeto setter de propiedad (CLSID \_ PropertySetter) y asóciela con un efecto o transición llamando al método IAMTimelineObj:: SetPropertySetter. Para obtener más información, vea trabajar con efectos y transiciones. normalmente, una aplicación solo necesita llamar al método IPropertySetter:: ClearProps para borrar las propiedades existentes y el método IPropertySetter:: AddProp para agregar nuevas propiedades. Otros componentes DES llaman a los otros métodos de esta interfaz.'
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: Interfaz IPropertySetter (QEDIT. h)
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
ms.openlocfilehash: 8f8aaadea2f0fb63287775294a7c61f01b3730df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680508"
---
# <a name="ipropertysetter-interface"></a>Interfaz IPropertySetter

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IPropertySetter` interfaz establece las propiedades de un efecto o una transición en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).

Para usar esta interfaz, cree una instancia de un objeto setter de propiedad (CLSID \_ PropertySetter) y asóciela con un efecto o transición llamando al método [**IAMTimelineObj:: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) . Para obtener más información, vea [trabajar con efectos y transiciones](working-with-effects-and-transitions.md).

Normalmente, una aplicación solo necesita llamar al método [**IPropertySetter:: ClearProps**](ipropertysetter-clearprops.md) para borrar las propiedades existentes y el método [**IPropertySetter:: AddProp**](ipropertysetter-addprop.md) para agregar nuevas propiedades. Otros componentes DES llaman a los otros métodos de esta interfaz.

## <a name="members"></a>Miembros

La interfaz **IPropertySetter** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IPropertySetter** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IPropertySetter** tiene estos métodos.



| Método                                               | Descripción                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddProp**](ipropertysetter-addprop.md)           | Agrega una propiedad al establecedor de propiedad, con una matriz de pares de valor de tiempo que definen el valor de la propiedad en un intervalo de tiempo.<br/> |
| [**ClearProps**](ipropertysetter-clearprops.md)     | Borra todos los datos de propiedad del establecedor de propiedad.<br/>                                                                                 |
| [**CloneProps**](ipropertysetter-cloneprops.md)     | Clona un conjunto de propiedades de este establecedor de propiedad y los agrega a un nuevo establecedor de propiedad.<br/>                                       |
| [**FreeProps**](ipropertysetter-freeprops.md)       | Libera los recursos asignados por el método [**IPropertySetter:: GetProps**](ipropertysetter-getprops.md) .<br/>                             |
| [**GetProps**](ipropertysetter-getprops.md)         | Recupera las propiedades establecidas en este objeto, con sus valores correspondientes.<br/>                                                      |
| [**LoadFromBlob**](ipropertysetter-loadfromblob.md) | Carga los datos de propiedad desde un formato de persistencia.<br/>                                                                                     |
| [**LoadXML**](ipropertysetter-loadxml.md)           | Carga los datos de propiedad expresados en lenguaje de marcado extensible (XML).<br/>                                                                 |
| [**PrintXML**](ipropertysetter-printxml.md)         | Convierte los datos de propiedad en una cadena XML.<br/>                                                                                         |
| [**SaveToBlob**](ipropertysetter-savetoblob.md)     | Guarda los datos de propiedad en un formato de persistencia.<br/>                                                                                   |
| [**SetProps**](ipropertysetter-setprops.md)         | Establece las propiedades del objeto de destino en el estado adecuado para el tiempo especificado.<br/>                                          |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
