---
description: El método SetStringValue agrega un nuevo valor de cadena (Type VT \_ LPWStr) o sobrescribe uno existente.
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: 'IPortableDeviceValues:: SetStringValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 163b5cd81ce8da64fc6d9f4304de5783b248522f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708684"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a>IPortableDeviceValues:: SetStringValue (método)

El método **SetStringValue** agrega un nuevo valor de cadena (Type VT \_ LPWStr) o sobrescribe uno existente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*clave* \[ de de\]
</dt> <dd>

**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.

</dd> <dt>

*Valor* \[ de de\]
</dt> <dd>

**LPCWSTR** que especifica el nuevo valor. Se copia la cadena, por lo que el llamador puede liberar la memoria asignada para este valor después de llamar a este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Cualquier memoria de clave existente se liberará adecuadamente.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, vea [especificar la información del cliente](specifying-client-information.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Agregar un recurso a un objeto](adding-a-resource-to-an-object.md)
</dt> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[Establecer propiedades para un solo objeto](setting-properties-for-a-single-object.md)
</dt> <dt>

[Establecer las propiedades de varios objetos](setting-properties-for-multiple-objects.md)
</dt> <dt>

[Especificar información de cliente](specifying-client-information.md)
</dt> <dt>

[Escritura de propiedades de objetos de contenido](writing-content-object-properties.md)
</dt> </dl>

 

 




