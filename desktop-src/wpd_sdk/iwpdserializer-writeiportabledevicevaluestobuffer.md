---
description: El método WriteIPortableDeviceValuesToBuffer serializa una interfaz IPortableDeviceValues a una matriz de bytes asignada por el llamador.
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: 'IWpdSerializer:: WriteIPortableDeviceValuesToBuffer (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.WriteIPortableDeviceValuesToBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2a8f8b374f967f7231881d9e0eca6434e9c57e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721571"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a>IWpdSerializer:: WriteIPortableDeviceValuesToBuffer (método)

El método **WriteIPortableDeviceValuesToBuffer** serializa una interfaz **IPortableDeviceValues** a una matriz de bytes asignada por el llamador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WriteIPortableDeviceValuesToBuffer(
  [in]  DWORD                 dwOutputBufferLength,
  [in]  IPortableDeviceValues *pResults,
  [out] BYTE                  *pBuffer,
  [out] DWORD                 *pdwBytesWritten
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwOutputBufferLength* \[ de\]
</dt> <dd>

**DWORD** que especifica el tamaño de *pBuffer*, en bytes.

</dd> <dt>

*pResults* \[ de\]
</dt> <dd>

Puntero a una interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) que se va a serializar.

</dd> <dt>

*pBuffer* \[ enuncia\]
</dt> <dd>

Puntero a un búfer asignado por el llamador. Para obtener información sobre el tamaño del búfer necesario, llame a **GetSerializedSize**.

</dd> <dt>

*pdwBytesWritten* \[ enuncia\]
</dt> <dd>

Puntero a un **valor DWORD** que indica el número de bytes que se ha escrito realmente en el búfer asignado por el llamador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                   | Descripción                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se ha llevado a cabo de forma correcta.<br/>                          |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Un argumento de puntero necesario era **null**.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | El búfer proporcionado por el autor de la llamada no era lo suficientemente grande.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método copia una interfaz **IPortableDeviceValues** en un búfer existente. Si desea asignar un nuevo búfer, use [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




