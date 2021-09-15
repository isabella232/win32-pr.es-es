---
description: El método WriteIPortableDeviceValuesToBuffer serializa una interfaz IPortableDeviceValues a una matriz de bytes asignada por el autor de la llamada.
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: Método IWpdSerializer::WriteIPortableDeviceValuesToBuffer (PortableDeviceTypes.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574285"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a>IWpdSerializer::WriteIPortableDeviceValuesToBuffer (método)

El **método WriteIPortableDeviceValuesToBuffer** serializa una interfaz **IPortableDeviceValues** a una matriz de bytes asignada por el autor de la llamada.

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

*dwOutputBufferLength* \[ En\]
</dt> <dd>

**DWORD** que especifica el tamaño de *pBuffer*, en bytes.

</dd> <dt>

*pResults* \[ En\]
</dt> <dd>

Puntero a una [**interfaz IPortableDeviceValues**](iportabledevicevalues.md) para serializar.

</dd> <dt>

*pBuffer* \[ out\]
</dt> <dd>

Puntero a un búfer asignado por el autor de la llamada. Para obtener información sobre el tamaño del búfer necesario, llame a **GetSerializedSize**.

</dd> <dt>

*pdwBytesWritten* \[ out\]
</dt> <dd>

Puntero a un **DWORD** que indica el número de bytes que se escribieron realmente en el búfer asignado por el autor de la llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                   | Descripción                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se ha llevado a cabo de forma correcta.<br/>                          |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Un argumento de puntero necesario era **NULL.**<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | El búfer proporcionado por el autor de la llamada no era lo suficientemente grande.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método copia una **interfaz IPortableDeviceValues** en un búfer existente. Si desea asignar un nuevo búfer, use [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWpdSerializer (interfaz)**](iwpdserializer.md)
</dt> </dl>

 

 




