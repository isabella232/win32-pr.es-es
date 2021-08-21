---
title: Método IWMDRMNetTransmitter SetLicenseChallenge (Wmdrmsdk.h)
description: El método SetLicenseChallenge procesa un desafío de licencia enviado por un Windows drm multimedia para dispositivos de red.
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- SetLicenseChallenge method windows Media Format
- Método SetLicenseChallenge windows Media Format , interfaz IWMDRMNetTransmitter
- IWMDRMNetTransmitter interface windows Media Format , Método SetLicenseChallenge
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
ms.openlocfilehash: 211f8de60cddb153e157af64ee300a4bbaf327d70a1564fbd9e622008c055cb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027573"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a>IWMDRMNetTransmitter::SetLicenseChallenge (método)

El **método SetLicenseChallenge** procesa un desafío de licencia enviado por un Windows DRM multimedia para dispositivos de red.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbLicenseChallenge* \[ En\]
</dt> <dd>

Puntero a los datos de desafío de licencia enviados por un receptor.

</dd> <dt>

*cbLicenseChallenge* \[ En\]
</dt> <dd>

Tamaño del desafío de licencia en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Si este método se realiza correctamente, las llamadas posteriores a los otros métodos de **IWMDRMNetTransmitter** usarán la información del desafío procesado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





