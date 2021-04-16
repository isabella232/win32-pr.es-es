---
description: El método GetIPortableDeviceValuesFromBuffer deserializa una matriz de bytes en una interfaz IPortableDeviceValues.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: 'IWpdSerializer:: GetIPortableDeviceValuesFromBuffer (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetIPortableDeviceValuesFromBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 639a9455349e1d016b71d9c9717940695e9c0a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670384"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a>IWpdSerializer:: GetIPortableDeviceValuesFromBuffer (método)

El método **GetIPortableDeviceValuesFromBuffer** deserializa una matriz de bytes en una interfaz **IPortableDeviceValues** .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIPortableDeviceValuesFromBuffer(
  [in]  BYTE                  *pBuffer,
  [in]  DWORD                 dwInputBufferLength,
  [out] IPortableDeviceValues **ppParams
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBuffer* \[ de\]
</dt> <dd>

Puntero al búfer que se va a deserializar.

</dd> <dt>

*dwInputBufferLength* \[ de\]
</dt> <dd>

**DWORD** que especifica el tamaño del búfer, en bytes.

</dd> <dt>

*ppParams* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe un puntero a una interfaz [**IPortableDeviceValues**](iportabledevicevalues.md) creada a partir del búfer. La aplicación es responsable de llamar a **Release** en la interfaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                  | Descripción                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | El método se ha llevado a cabo de forma correcta.<br/>                     |
| <dl> <dt>**\_puntero E**</dt> </dl>    | Un argumento de puntero necesario era **null**.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Se produjo un error de conversión no especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




