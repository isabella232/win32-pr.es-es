---
description: El método GetBufferFromIPortableDeviceValues serializa una interfaz IPortableDeviceValues enviada a una matriz de bytes asignada. La matriz de bytes devuelta se asigna al llamador y debe liberarla el llamador mediante CoTaskMemFree.
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: 'IWpdSerializer:: GetBufferFromIPortableDeviceValues (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetBufferFromIPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44f4e9e7011e6a4766183307e81ef7e783da899f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718627"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a>IWpdSerializer:: GetBufferFromIPortableDeviceValues (método)

El método **GetBufferFromIPortableDeviceValues** serializa una interfaz **IPortableDeviceValues** enviada a una matriz de bytes asignada. La matriz de bytes devuelta se asigna al llamador y debe liberarla el llamador mediante **CoTaskMemFree**.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBufferFromIPortableDeviceValues(
  [in]  IPortableDeviceValues *pSource,
  [out] BYTE                  **ppBuffer,
  [out] DWORD                 *pdwBufferSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSource* \[ de\]
</dt> <dd>

Puntero a una interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) que se va a serializar.

</dd> <dt>

*ppBuffer* \[ enuncia\]
</dt> <dd>

Puntero a un **byte \* *_ que contiene los datos serializados. Dispositivos portátiles de Windows asigna esta memoria; el autor de la llamada debe liberarlo llamando a _* CoTaskMemFree**.

</dd> <dt>

*pdwBufferSize* \[ enuncia\]
</dt> <dd>

Puntero a un **valor DWORD** que especifica el tamaño del búfer asignado, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                   | Descripción                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se ha llevado a cabo de forma correcta.<br/>                                       |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Un argumento de puntero necesario era **null**.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No había suficiente memoria disponible para crear el búfer.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




