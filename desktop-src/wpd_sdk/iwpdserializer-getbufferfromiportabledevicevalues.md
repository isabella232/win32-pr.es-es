---
description: El método GetBufferFromIPortableDeviceValues serializa una interfaz IPortableDeviceValues enviada a una matriz de bytes asignada. La matriz de bytes devuelta se asigna al autor de la llamada y el autor de la llamada debe liberarla mediante CoTaskMemFree.
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: Método IWpdSerializer::GetBufferFromIPortableDeviceValues (PortableDeviceTypes.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574292"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a>Método IWpdSerializer::GetBufferFromIPortableDeviceValues

El **método GetBufferFromIPortableDeviceValues** serializa una interfaz **IPortableDeviceValues** enviada a una matriz de bytes asignada. La matriz de bytes devuelta se asigna al autor de la llamada y la debe liberar el autor de la llamada **mediante CoTaskMemFree.**

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

*pSource* \[ En\]
</dt> <dd>

Puntero a una [**interfaz IPortableDeviceValues**](iportabledevicevalues.md) para serializar.

</dd> <dt>

*ppBuffer* \[ out\]
</dt> <dd>

Puntero a un **byte _ que contiene los datos \* *serializados. Windows Dispositivos portátiles asigna esta memoria; El autor de la llamada debe liberarlo llamando a _* CoTaskMemFree**.

</dd> <dt>

*pdwBufferSize* \[ out\]
</dt> <dd>

Puntero a un **DWORD** que especifica el tamaño del búfer asignado, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                   | Descripción                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se ha llevado a cabo de forma correcta.<br/>                                       |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Un argumento de puntero necesario era **NULL.**<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No había suficiente memoria disponible para crear el búfer.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWpdSerializer (interfaz)**](iwpdserializer.md)
</dt> </dl>

 

 




