---
description: La interfaz IPortableDeviceValues contiene una colección de pares PROPERTYKEY/PROPVARIANT.
ms.assetid: a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f
title: Interfaz IPortableDeviceValues (PortableDeviceTypes.h)
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
ms.openlocfilehash: 7f7aaceff66cd817666dd05b92243239f860b2f59a993e4afca1831fc8085de0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930005"
---
# <a name="iportabledevicevalues-interface"></a>Interfaz IPortableDeviceValues

La **interfaz IPortableDeviceValues** contiene una colección de pares **PROPERTYKEY** / **PROPVARIANT.** Los valores de la colección no necesitan ser el mismo VARTYPE.

Los valores se almacenan como pares clave-valor; cada clave debe ser única en la colección. Los clientes pueden buscar elementos por **PROPERTYKEY** o índice de base cero. Los valores de datos se almacenan **como estructuras PROPVARIANT.** Puede agregar o recuperar valores de cualquier tipo mediante los métodos genéricos **SetValue** y **GetValue**, o bien agregar elementos mediante el método específico del tipo de datos agregados.

Los **métodos Get...** requieren que el autor de la llamada libere los valores recuperados correctamente. Los **métodos Set...** copian el valor en la colección.

Cuando se libera una interfaz **IPortableDeviceValues,** llama a **Clear**, que libera la memoria que se asignó para todos sus miembros correctamente.

Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamar a **CoCreate** con **CLSID \_ PortableDeviceValues**.

## <a name="members"></a>Miembros

La **interfaz IPortableDeviceValues** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPortableDeviceValues** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IPortableDeviceValues** tiene estos métodos.



| Método                                                                                                                     | Descripción                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**Borrar**](iportabledevicevalues-clear.md)                                                                               | Elimina todos los elementos de la colección.<br/>                                                                      |
| [**CopyValuesFromPropertyStore**](iportabledevicevalues-copyvaluesfrompropertystore.md)                                   | Copia el contenido de **un IPropertyStore** en la colección.<br/>                                           |
| [**CopyValuesToPropertyStore**](iportabledevicevalues-copyvaluestopropertystore.md)                                       | Copia todos los valores de una colección en una **interfaz IPropertyStore.**<br/>                               |
| [**GetAt**](iportabledevicevalues-getat.md)                                                                               | Recupera un valor de la colección mediante el índice de base cero proporcionado.<br/>                                  |
| [**GetBoolValue**](iportabledevicevalues-getboolvalue.md)                                                                 | Recupera un **valor BOOL** (tipo VT \_ BOOL) especificado por una clave.<br/>                                              |
| [**GetBufferValue**](iportabledevicevalues-getbuffervalue.md)                                                             | Recupera un valor de matriz de bytes (tipo VT \_ VECTOR \| VT \_ UI1) especificado por una clave.<br/>                               |
| [**GetCount**](iportabledevicevalues-getcount.md)                                                                         | Recupera el número de elementos de la colección.<br/>                                                            |
| [**GetErrorValue**](iportabledevicevalues-geterrorvalue.md)                                                               | Recupera un **valor HRESULT** (tipo VT \_ ERROR) especificado por una clave.<br/>                                         |
| [**GetFloatValue**](iportabledevicevalues-getfloatvalue.md)                                                               | Recupera un valor **FLOAT** (tipo VT \_ R4) especificado por una clave.<br/>                                               |
| [**GetGuidValue**](iportabledevicevalues-getguidvalue.md)                                                                 | Recupera un **valor GUID** (tipo VT \_ CLSID) especificado por una clave.<br/>                                             |
| [**GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)                 | Recupera un **valor IPortableDeviceKeyCollection** (tipo VT \_ UNKNOWN) especificado por una clave.<br/>                  |
| [**GetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md) | Recupera un **valor IPortableDevicePropVariantCollection** (tipo VT \_ UNKNOWN) especificado por una clave.<br/>          |
| [**GetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)           | Recupera un **valor IPortableDeviceValuesCollection** (tipo VT \_ UNKNOWN) especificado por una clave.<br/>               |
| [**GetIPortableDeviceValuesValues**](iportabledevicevalues-getiportabledevicevaluesvalue.md)                               | Recupera un **valor IPortableDeviceValues** (tipo VT \_ UNKNOWN) especificado por una clave.<br/>                         |
| [**GetIUnknownValue**](iportabledevicevalues-getiunknownvalue.md)                                                         | Recupera un valor **de interfaz IUnknown** (tipo VT \_ UNKNOWN) especificado por una clave.<br/>                            |
| [**GetKeyValue**](iportabledevicevalues-getkeyvalue.md)                                                                   | Recupera un **valor PROPERTYKEY** especificado por una clave.<br/>                                                       |
| [**GetSignedIntegerValue**](iportabledevicevalues-getsignedintegervalue.md)                                               | Recupera un **valor LONG** (tipo VT \_ I4) especificado por una clave.<br/>                                                |
| [**GetSignedLargeIntegerValue**](iportabledevicevalues-getsignedlargeintegervalue.md)                                     | Recupera un **valor LONGLONG** (tipo VT \_ I8) especificado por una clave.<br/>                                            |
| [**GetStringValue**](iportabledevicevalues-getstringvalue.md)                                                             | Recupera un valor de cadena (tipo \_ VT LPWSTR) especificado por una clave.<br/>                                              |
| [**GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md)                                           | Recupera un **valor ULONG** (tipo VT \_ UI4) especificado por una clave.<br/>                                              |
| [**GetUnsignedLargeIntegerValue**](iportabledevicevalues-getunsignedlargeintegervalue.md)                                 | Recupera un **valor ULONGLONG** (tipo VT \_ UI8) especificado por una clave.<br/>                                          |
| [**GetValue**](iportabledevicevalues-getvalue.md)                                                                         | Recupera un **valor PROPVARIANT** especificado por una clave.<br/>                                                       |
| [**RemoveValue**](iportabledevicevalues-removevalue.md)                                                                   | Quita un elemento de la colección.<br/>                                                                        |
| [**SetBoolValue**](iportabledevicevalues-setboolvalue.md)                                                                 | Agrega un nuevo **valor booleano** (tipo VT \_ BOOL) o sobrescribe uno existente.<br/>                                 |
| [**SetBufferValue**](iportabledevicevalues-setbuffervalue.md)                                                             | Agrega un nuevo valor **BYTE** \* (tipo VT VECTOR VT \_ \| \_ UI1) o sobrescribe uno existente.<br/>                     |
| [**SetErrorValue**](iportabledevicevalues-seterrorvalue.md)                                                               | Agrega un nuevo **valor HRESULT** (tipo VT \_ ERROR) o sobrescribe uno existente.<br/>                                |
| [**SetFloatValue**](iportabledevicevalues-setfloatvalue.md)                                                               | Agrega un nuevo **valor FLOAT** (tipo VT \_ R4) o sobrescribe uno existente.<br/>                                     |
| [**SetGuidValue**](iportabledevicevalues-setguidvalue.md)                                                                 | Agrega un nuevo **valor GUID** (tipo VT \_ CLSID) o sobrescribe uno existente.<br/>                                   |
| [**SetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)                 | Agrega un nuevo **valor IPortableDeviceKeyCollectionValue** (tipo VT \_ UNKNOWN) o sobrescribe uno existente.<br/>    |
| [**SetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md) | Agrega un nuevo **valor IPortableDevicePropVariantCollection** (tipo VT \_ UNKNOWN) o sobrescribe uno existente.<br/> |
| [**SetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)           | Agrega un nuevo **valor IPortableDeviceValuesCollection** (tipo VT \_ UNKNOWN) o sobrescribe uno existente.<br/>      |
| [**SetIPortableDeviceValuesValues**](iportabledevicevalues-setiportabledevicevaluesvalue.md)                               | Agrega un nuevo **valor IPortableDeviceValues** (tipo VT \_ UNKNOWN) o sobrescribe uno existente.<br/>                |
| [**SetIUnknownValue**](iportabledevicevalues-setiunknownvalue.md)                                                         | Agrega un nuevo **valor IUnknown** (tipo VT \_ UNKNOWN) o sobrescribe uno existente.<br/>                             |
| [**SetKeyValue**](iportabledevicevalues-setkeyvalue.md)                                                                   | Agrega un nuevo **valor PROPERTYKEY** (tipo VT \_ UNKNOWN) o sobrescribe uno existente.<br/>                          |
| [**SetSignedIntegerValue**](iportabledevicevalues-setsignedintegervalue.md)                                               | Agrega un nuevo **valor LONG** (tipo VT \_ I4) o sobrescribe uno existente.<br/>                                      |
| [**SetSignedLargeIntegerValue**](iportabledevicevalues-setsignedlargeintegervalue.md)                                     | Agrega un nuevo **valor LONGLONG** (tipo VT \_ I8) o sobrescribe uno existente.<br/>                                  |
| [**SetStringValue**](iportabledevicevalues-setstringvalue.md)                                                             | Agrega un nuevo valor de cadena (tipo \_ VT LPWSTR) o sobrescribe uno existente.<br/>                                    |
| [**SetUnsignedIntegerValue**](iportabledevicevalues-setunsignedintegervalue.md)                                           | Agrega un nuevo **valor ULONG** (tipo VT \_ UI4) o sobrescribe uno existente.<br/>                                    |
| [**SetUnsignedLargeIntegerValue**](iportabledevicevalues-setunsignedlargeintegervalue.md)                                 | Agrega un nuevo **valor ULONGLONG** (tipo VT \_ UI8) o sobrescribe uno existente.<br/>                                |
| [**SetValue**](iportabledevicevalues-setvalue.md)                                                                         | Agrega un nuevo **valor PROPVARIANT** o sobrescribe uno existente.<br/>                                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces de colección**](collection-interfaces.md)
</dt> </dl>

 

