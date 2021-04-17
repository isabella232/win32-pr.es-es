---
title: IWMDRMDevice GetMeterChallenge, método
description: El método GetMeterChallenge recupera el desafío de medición.
ms.assetid: 4c122886-46bd-4e63-8e7d-5e6132363662
keywords:
- Método GetMeterChallenge de Windows Media Administrador de dispositivos
- Método GetMeterChallenge de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, método GetMeterChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a916afa90d1db310041f9b92be94d3af9154df4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698515"
---
# <a name="iwmdrmdevicegetmeterchallenge-method"></a>IWMDRMDevice:: GetMeterChallenge (método)

El método **GetMeterChallenge** recupera el desafío de medición.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMeterChallenge(
  [in]  BSTR  bstrMeterCert,
  [out] BYTE  **ppbMeterChallenge,
  [out] DWORD *pcbMeterChallenge
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrMeterCert* \[ de\]
</dt> <dd>

Certificado de medición que el propietario del contenido envía al equipo host para recopilar los datos de medición asociados en el dispositivo

</dd> <dt>

*ppbMeterChallenge* \[ enuncia\]
</dt> <dd>

Resultado de desafío de medición recuperado.

</dd> <dt>

*pcbMeterChallenge* \[ enuncia\]
</dt> <dd>

Tamaño del desafío de medición, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Los datos de medición se recopilan y almacenan en el almacén de datos DRM en el dispositivo para el contenido con la medición habilitada. Se registrarán acciones como Play. Cuando se llama a esta función, el dispositivo recopila los datos de medición en el almacén de datos DRM en forma de un documento XML y lo envía a hostcomputer. Si hay demasiados datos, se envían en fases.

Cuando el equipo host recibe los datos de medición, envía los datos a través de Internet a la dirección URL especificada en el certificado de medición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





