---
description: El método GetIPortableDeviceValuesFromBuffer deserializa una matriz de bytes en una interfaz IPortableDeviceValues.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: Método IWpdSerializer::GetIPortableDeviceValuesFromBuffer (PortableDeviceTypes.h)
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
ms.openlocfilehash: ac33bf0cfb04363d40e4efeff13db1cb2504ce2dcb7ece4d9b10ac3d08dff83f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054965"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a>IWpdSerializer::GetIPortableDeviceValuesFromBuffer (método)

El **método GetIPortableDeviceValuesFromBuffer** deserializa una matriz de bytes en una **interfaz IPortableDeviceValues.**

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

*pBuffer* \[ En\]
</dt> <dd>

Puntero al búfer que se deserializa.

</dd> <dt>

*dwInputBufferLength* \[ En\]
</dt> <dd>

**DWORD** que especifica el tamaño del búfer, en bytes.

</dd> <dt>

*ppParams* \[ out\]
</dt> <dd>

Dirección de una variable que recibe un puntero a una [**interfaz IPortableDeviceValues**](iportabledevicevalues.md) creada a partir del búfer. La aplicación es responsable de llamar a **Release** en la interfaz .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                  | Descripción                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | El método se ha llevado a cabo de forma correcta.<br/>                     |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | Un argumento de puntero necesario era **NULL.**<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Error de conversión no especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWpdSerializer (interfaz)**](iwpdserializer.md)
</dt> </dl>

 

 




