---
description: La interfaz IPortableDeviceValues contiene una colección de pares PROPERTYKEY/PROPVARIANT.
ms.assetid: a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f
title: Interfaz IPortableDeviceValues (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ecdfd91c9ea4ab5202a72015f579d560b37fbffd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698568"
---
# <a name="iportabledevicevalues-interface"></a>Interfaz IPortableDeviceValues

La interfaz **IPortableDeviceValues** contiene una colección de pares **PROPERTYKEY** / **PROPVARIANT** . No es necesario que los valores de la colección sean el mismo VARTYPE.

Los valores se almacenan como pares de clave y valor. cada clave debe ser única en la colección. Los clientes pueden buscar elementos por **PROPERTYKEY** o por índice de base cero. Los valores de datos se almacenan como estructuras **PROPVARIANT** . Puede Agregar o recuperar valores de cualquier tipo mediante los métodos genéricos **SetValue** y **GetValue**, o bien, puede agregar elementos mediante el método específico del tipo de datos agregado.

Los métodos **get...** requieren que el autor de la llamada libere correctamente los valores recuperados. Los métodos **set...** copian el valor en la colección.

Cuando se libera una interfaz **IPortableDeviceValues** , llama a **Clear**, que libera la memoria que se asignó para todos sus miembros adecuadamente.

Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamar a **CoCreate** con **CLSID \_ PortableDeviceValues**.

## <a name="members"></a>Miembros

La interfaz **IPortableDeviceValues** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPortableDeviceValues** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IPortableDeviceValues** tiene estos métodos.



| Método                                                                                                                     | Descripción                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**Claridad**](iportabledevicevalues-clear.md)                                                                               | Elimina todos los elementos de la colección.<br/>                                                                      |
| [**CopyValuesFromPropertyStore**](iportabledevicevalues-copyvaluesfrompropertystore.md)                                   | Copia el contenido de un **IPropertyStore** en la colección.<br/>                                           |
| [**CopyValuesToPropertyStore**](iportabledevicevalues-copyvaluestopropertystore.md)                                       | Copia todos los valores de una colección en una interfaz **IPropertyStore** .<br/>                               |
| [**GetAt**](iportabledevicevalues-getat.md)                                                                               | Recupera un valor de la colección utilizando el índice de base cero proporcionado.<br/>                                  |
| [**GetBoolValue**](iportabledevicevalues-getboolvalue.md)                                                                 | Recupera un valor **booleano** (tipo VT \_ bool) especificado por una clave.<br/>                                              |
| [**GetBufferValue**](iportabledevicevalues-getbuffervalue.md)                                                             | Recupera un valor de matriz de bytes (Type VT \_ Vector \| VT \_ UI1) especificado por una clave.<br/>                               |
| [**GetCount**](iportabledevicevalues-getcount.md)                                                                         | Recupera el número de elementos de la colección.<br/>                                                            |
| [**GetErrorValue**](iportabledevicevalues-geterrorvalue.md)                                                               | Recupera un valor **HRESULT** (tipo VT \_ error) especificado por una clave.<br/>                                         |
| [**GetFloatValue**](iportabledevicevalues-getfloatvalue.md)                                                               | Recupera un valor **float** (tipo VT \_ R4) especificado por una clave.<br/>                                               |
| [**GetGuidValue**](iportabledevicevalues-getguidvalue.md)                                                                 | Recupera un valor **GUID** (tipo VT \_ CLSID) especificado por una clave.<br/>                                             |
| [**GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)                 | Recupera un valor de **IPortableDeviceKeyCollection** (tipo VT \_ desconocido) especificado por una clave.<br/>                  |
| [**GetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md) | Recupera un valor de **IPortableDevicePropVariantCollection** (tipo VT \_ desconocido) especificado por una clave.<br/>          |
| [**GetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)           | Recupera un valor de **IPortableDeviceValuesCollection** (tipo VT \_ desconocido) especificado por una clave.<br/>               |
| [**GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md)                               | Recupera un valor de **IPortableDeviceValues** (tipo VT \_ desconocido) especificado por una clave.<br/>                         |
| [**GetIUnknownValue**](iportabledevicevalues-getiunknownvalue.md)                                                         | Recupera un valor de interfaz **IUnknown** (tipo VT \_ desconocido) especificado por una clave.<br/>                            |
| [**GetKeyValue**](iportabledevicevalues-getkeyvalue.md)                                                                   | Recupera un valor de **PROPERTYKEY** especificado por una clave.<br/>                                                       |
| [**GetSignedIntegerValue**](iportabledevicevalues-getsignedintegervalue.md)                                               | Recupera un valor **Long** (Type VT \_ I4) especificado por una clave.<br/>                                                |
| [**GetSignedLargeIntegerValue**](iportabledevicevalues-getsignedlargeintegervalue.md)                                     | Recupera un valor **LONGLONG** (Type VT \_ i8) especificado por una clave.<br/>                                            |
| [**GetStringValue**](iportabledevicevalues-getstringvalue.md)                                                             | Recupera un valor de cadena (tipo VT \_ LPWStr) especificado por una clave.<br/>                                              |
| [**GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md)                                           | Recupera un valor **ULong** (tipo VT \_ UI4) especificado por una clave.<br/>                                              |
| [**GetUnsignedLargeIntegerValue**](iportabledevicevalues-getunsignedlargeintegervalue.md)                                 | Recupera un valor de **ULONGLONG** (tipo VT \_ UI8) especificado por una clave.<br/>                                          |
| [**GetValue**](iportabledevicevalues-getvalue.md)                                                                         | Recupera un valor de **PROPVARIANT** especificado por una clave.<br/>                                                       |
| [**RemoveValue**](iportabledevicevalues-removevalue.md)                                                                   | Quita un elemento de la colección.<br/>                                                                        |
| [**SetBoolValue**](iportabledevicevalues-setboolvalue.md)                                                                 | Agrega un nuevo valor **booleano** (Type VT \_ bool) o sobrescribe uno existente.<br/>                                 |
| [**SetBufferValue**](iportabledevicevalues-setbuffervalue.md)                                                             | Agrega un nuevo valor de **byte** \* (Type VT \_ Vector \| VT \_ UI1) o sobrescribe uno existente.<br/>                     |
| [**SetErrorValue**](iportabledevicevalues-seterrorvalue.md)                                                               | Agrega un nuevo valor **HRESULT** (tipo VT \_ error) o sobrescribe uno existente.<br/>                                |
| [**SetFloatValue**](iportabledevicevalues-setfloatvalue.md)                                                               | Agrega un nuevo valor **float** (Type VT \_ R4) o sobrescribe uno existente.<br/>                                     |
| [**SetGuidValue**](iportabledevicevalues-setguidvalue.md)                                                                 | Agrega un nuevo valor **GUID** (Type VT \_ CLSID) o sobrescribe uno existente.<br/>                                   |
| [**SetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)                 | Agrega un nuevo valor de **IPortableDeviceKeyCollectionValue** (tipo VT \_ desconocido) o sobrescribe uno existente.<br/>    |
| [**SetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md) | Agrega un nuevo valor de **IPortableDevicePropVariantCollection** (tipo VT \_ desconocido) o sobrescribe uno existente.<br/> |
| [**SetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)           | Agrega un nuevo valor de **IPortableDeviceValuesCollection** (tipo VT \_ desconocido) o sobrescribe uno existente.<br/>      |
| [**SetIPortableDeviceValuesValue**](iportabledevicevalues-setiportabledevicevaluesvalue.md)                               | Agrega un nuevo valor de **IPortableDeviceValues** (tipo VT \_ desconocido) o sobrescribe uno existente.<br/>                |
| [**SetIUnknownValue**](iportabledevicevalues-setiunknownvalue.md)                                                         | Agrega un nuevo valor **IUnknown** (tipo VT \_ desconocido) o sobrescribe uno existente.<br/>                             |
| [**SetKeyValue**](iportabledevicevalues-setkeyvalue.md)                                                                   | Agrega un nuevo valor de **PROPERTYKEY** (tipo VT \_ desconocido) o sobrescribe uno existente.<br/>                          |
| [**SetSignedIntegerValue**](iportabledevicevalues-setsignedintegervalue.md)                                               | Agrega un nuevo valor **Long** (Type VT \_ I4) o sobrescribe uno existente.<br/>                                      |
| [**SetSignedLargeIntegerValue**](iportabledevicevalues-setsignedlargeintegervalue.md)                                     | Agrega un nuevo valor de **LONGLONG** (tipo VT \_ i8) o sobrescribe uno existente.<br/>                                  |
| [**SetStringValue**](iportabledevicevalues-setstringvalue.md)                                                             | Agrega un nuevo valor de cadena (Type VT \_ LPWStr) o sobrescribe uno existente.<br/>                                    |
| [**SetUnsignedIntegerValue**](iportabledevicevalues-setunsignedintegervalue.md)                                           | Agrega un nuevo valor **ULong** (tipo VT \_ UI4) o sobrescribe uno existente.<br/>                                    |
| [**SetUnsignedLargeIntegerValue**](iportabledevicevalues-setunsignedlargeintegervalue.md)                                 | Agrega un nuevo valor de **ULONGLONG** (tipo VT \_ UI8) o sobrescribe uno existente.<br/>                                |
| [**SetValue**](iportabledevicevalues-setvalue.md)                                                                         | Agrega un nuevo valor de **PROPVARIANT** o sobrescribe uno existente.<br/>                                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces de colección**](collection-interfaces.md)
</dt> </dl>

 

