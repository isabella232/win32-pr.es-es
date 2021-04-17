---
description: El método GetSerializedSize calcula el tamaño del búfer necesario para contener una interfaz serializada de IPortableDeviceValues.
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: 'IWpdSerializer:: GetSerializedSize (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetSerializedSize
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7b50f7f6158145cd71125b5e5f26649712bb065b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670385"
---
# <a name="iwpdserializergetserializedsize-method"></a>IWpdSerializer:: GetSerializedSize (método)

El método **GetSerializedSize** calcula el tamaño del búfer necesario para contener una interfaz serializada de [**IPortableDeviceValues**](iportabledevicevalues.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSource* \[ de\]
</dt> <dd>

Puntero a una interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) cuyo tamaño se desea solicitar.

</dd> <dt>

*pdwSize* \[ enuncia\]
</dt> <dd>

Puntero a un **valor DWORD** que indica el tamaño del búfer necesario para serializar *pSource*, en bytes.

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

 

 




