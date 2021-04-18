---
title: Método IWMDRMLicenseManagement CreateLicenseRevocationChallenge (wmdrmsdk. h)
description: El método CreateLicenseRevocationChallenge genera un desafío de revocación de licencia.
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- Método CreateLicenseRevocationChallenge formato de Windows Media
- Método CreateLicenseRevocationChallenge formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método CreateLicenseRevocationChallenge
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseRevocationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7fd0acb41b9a2548e5be708611529bea92e131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718765"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a>IWMDRMLicenseManagement:: CreateLicenseRevocationChallenge (método)

El método **CreateLicenseRevocationChallenge** genera un desafío de revocación de licencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateLicenseRevocationChallenge(
  [in]  BYTE  *pbMachineID,
  [in]  DWORD cbMachineID,
  [in]  BYTE  *pbChallenge,
  [in]  DWORD cbChallenge,
  [out] BYTE  **ppbChallengeOutput,
  [out] DWORD *pcbChallengeOutput
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbMachineID* \[ de\]
</dt> <dd>

Identificador de equipo especificado por el usuario. Este valor se utiliza para consultar una licencia en el servidor y debe ajustarse al formato que use el servidor de licencias.

</dd> <dt>

*cbMachineID* \[ de\]
</dt> <dd>

Tamaño, en bytes, del identificador de la máquina.

</dd> <dt>

*pbChallenge* \[ de\]
</dt> <dd>

Datos de desafío especificados por el usuario. Estos datos, además del identificador de equipo, se usan para consultar el servidor de licencias para obtener las licencias que se van a revocar.

</dd> <dt>

*cbChallenge* \[ de\]
</dt> <dd>

Tamaño, en bytes, de los datos de desafío.

</dd> <dt>

*ppbChallengeOutput* \[ enuncia\]
</dt> <dd>

Dirección de un puntero que recibe la dirección de la salida del desafío. Este búfer son los datos que se envían al servicio de revocación de licencias. Cuando termine con estos datos, debe liberar la memoria mediante una llamada a **CoTaskMemFree**.

</dd> <dt>

*pcbChallengeOutput* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe el tamaño de los datos de salida de desafío asignados, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





