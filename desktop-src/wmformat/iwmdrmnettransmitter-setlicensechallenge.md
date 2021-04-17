---
title: Método IWMDRMNetTransmitter SetLicenseChallenge (wmdrmsdk. h)
description: El método SetLicenseChallenge procesa un desafío de licencia enviado por un receptor de Windows Media DRM para dispositivos de red.
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- Método SetLicenseChallenge formato de Windows Media
- Método SetLicenseChallenge formato de Windows Media, interfaz IWMDRMNetTransmitter
- Interfaz IWMDRMNetTransmitter formato de Windows Media, método SetLicenseChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.SetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94b83ca615896039a592d147fe8c14d15493cec0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679140"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a>IWMDRMNetTransmitter:: SetLicenseChallenge (método)

El método **SetLicenseChallenge** procesa un desafío de licencia enviado por un receptor de Windows Media DRM para dispositivos de red.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbLicenseChallenge* \[ de\]
</dt> <dd>

Puntero a los datos de desafío de licencia enviados por un receptor.

</dd> <dt>

*cbLicenseChallenge* \[ de\]
</dt> <dd>

Tamaño del desafío de la licencia en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Si este método se ejecuta correctamente, las llamadas subsiguientes a los otros métodos de **IWMDRMNetTransmitter** utilizarán la información del desafío procesado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





