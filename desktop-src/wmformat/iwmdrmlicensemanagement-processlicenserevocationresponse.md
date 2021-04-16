---
title: Método IWMDRMLicenseManagement ProcessLicenseRevocationResponse (wmdrmsdk. h)
description: El método ProcessLicenseRevocationResponse revoca las licencias del almacén de licencias local. Este método usa un BLOB de revocación de licencias (LRB) recibido de un servidor de revocación de licencias para identificar las licencias que se van a revocar.
ms.assetid: 4428ac44-c3f4-404e-9997-cbc7360faedf
keywords:
- Método ProcessLicenseRevocationResponse formato de Windows Media
- Método ProcessLicenseRevocationResponse formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método ProcessLicenseRevocationResponse
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseRevocationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534ead406107957971bbf1501dff2850478fae08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718801"
---
# <a name="iwmdrmlicensemanagementprocesslicenserevocationresponse-method"></a>IWMDRMLicenseManagement::P método rocessLicenseRevocationResponse

El método **ProcessLicenseRevocationResponse** revoca las licencias del almacén de licencias local. Este método usa un BLOB de revocación de licencias (LRB) recibido de un servidor de revocación de licencias para identificar las licencias que se van a revocar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ProcessLicenseRevocationResponse(
  [in]  BYTE  *pbSignedLRB,
  [in]  DWORD cbSignedLRB,
  [out] BYTE  **ppbSignedACK,
  [out] DWORD *pcbSignedACK
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbSignedLRB* \[ de\]
</dt> <dd>

El BLOB de revocación de licencias (LRB) recibido del servidor de revocación de licencias en respuesta a un desafío que se generó llamando al método [**CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) .

</dd> <dt>

*cbSignedLRB* \[ de\]
</dt> <dd>

Tamaño de LRB en bytes.

</dd> <dt>

*ppbSignedACK* \[ enuncia\]
</dt> <dd>

Dirección de un puntero que recibe la dirección de la confirmación de revocación de licencia. La confirmación se debe enviar al servicio de revocación de licencias. Cuando termine con estos datos, debe liberar la memoria mediante una llamada a **CoTaskMemFree**.

</dd> <dt>

*pcbSignedACK* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe el tamaño de la confirmación en bytes.

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

 

 





