---
description: El método CopyValuesFromPropertyStore copia el contenido de un IPropertyStore en la colección.
ms.assetid: 887c9569-ff76-41cf-8782-62c59c04e831
title: Método IPortableDeviceValues::CopyValuesFromPropertyStore (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesFromPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0944edff81a62652851bc2c18b58f47f5d33d09ad7da6ba5a2eda95919c54dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963714"
---
# <a name="iportabledevicevaluescopyvaluesfrompropertystore-method"></a>IPortableDeviceValues::CopyValuesFromPropertyStore (método)

El **método CopyValuesFromPropertyStore** copia el contenido de **un IPropertyStore** en la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CopyValuesFromPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStore* \[ En\]
</dt> <dd>

Puntero a un **IPropertyStore** para copiar en la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método convierte automáticamente todos los valores **\_ BSTR de VT** en valores **\_ LPWSTR de VT.**

Muchas aplicaciones o componentes externos que se comunican con la aplicación, como algunas aplicaciones de shell, usan la **interfaz IPropertyStore.** Este método proporciona una manera rápida y sencilla de intercambiar datos con estos programas.

Este método se admite en Windows Vista y versiones posteriores de Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPortableDeviceValues (interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::CopyValuesToPropertyStore**](iportabledevicevalues-copyvaluestopropertystore.md)
</dt> </dl>

 

 




