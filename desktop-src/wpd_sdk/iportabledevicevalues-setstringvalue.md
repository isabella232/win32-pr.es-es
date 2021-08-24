---
description: El método SetStringValue agrega un nuevo valor de cadena (tipo \_ VT LPWSTR) o sobrescribe uno existente.
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: Método IPortableDeviceValues::SetStringValue (PortableDeviceTypes.h)
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
ms.openlocfilehash: 0c00195823d71a59e706af1c0a627670f583776140772c3b8634ac10d7d95919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806865"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a>IPortableDeviceValues::SetStringValue (método)

El **método SetStringValue** agrega un nuevo valor de cadena (tipo \_ VT LPWSTR) o sobrescribe uno existente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*key* \[ En\]
</dt> <dd>

**REFPROPERTYKEY que** especifica el elemento que se creará o sobrescribirá.

</dd> <dt>

*Valor* \[ En\]
</dt> <dd>

**LPCWSTR** que especifica el nuevo valor. La cadena se copia, por lo que el autor de la llamada puede liberar la memoria asignada para este valor después de llamar a este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Cualquier memoria de clave existente se liberará correctamente.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, vea [Especificar información de cliente](specifying-client-information.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Agregar un recurso a un objeto](adding-a-resource-to-an-object.md)
</dt> <dt>

[**IPortableDeviceValues (Interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[Establecer propiedades para un único objeto](setting-properties-for-a-single-object.md)
</dt> <dt>

[Establecer propiedades para varios objetos](setting-properties-for-multiple-objects.md)
</dt> <dt>

[Especificar información de cliente](specifying-client-information.md)
</dt> <dt>

[Escribir propiedades content-object](writing-content-object-properties.md)
</dt> </dl>

 

 




