---
description: El método GetSerializedSize calcula el tamaño de búfer necesario para contener una interfaz IPortableDeviceValues serializada.
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: Método IWpdSerializer::GetSerializedSize (PortableDeviceTypes.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266855"
---
# <a name="iwpdserializergetserializedsize-method"></a>IWpdSerializer::GetSerializedSize (método)

El **método GetSerializedSize** calcula el tamaño de búfer necesario para contener una interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) serializada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSource* \[ En\]
</dt> <dd>

Puntero a una [**interfaz IPortableDeviceValues**](iportabledevicevalues.md) cuyo tamaño desea solicitar.

</dd> <dt>

*pdwSize* \[ out\]
</dt> <dd>

Puntero a un **DWORD** que indica el tamaño de búfer necesario para *serializar pSource*, en bytes.

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

 

 




