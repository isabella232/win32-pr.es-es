---
title: Método IWMDRMLicenseManagement ProcessLicenseRevocationResponse (Wmdrmsdk.h)
description: El método ProcessLicenseRevocationResponse revoca las licencias del almacén de licencias local. Este método usa un blob de revocación de licencias (LRB) recibido de un servidor de revocación de licencias para identificar las licencias que se deben revocar.
ms.assetid: 4428ac44-c3f4-404e-9997-cbc7360faedf
keywords:
- Formato multimedia del método ProcessLicenseRevocationResponse
- Método ProcessLicenseRevocationResponse windows Media Format , interfaz IWMDRMLicenseManagement
- IWMDRMLicenseManagement interface windows Media Format , ProcessLicenseRevocationResponse method
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
ms.openlocfilehash: d58c33f79db575dec37d7d2ac51e3c65b10416b9ca35a50084f36a56693854be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930315"
---
# <a name="iwmdrmlicensemanagementprocesslicenserevocationresponse-method"></a>Método IWMDRMLicenseManagement::P rocessLicenseRevocationResponse

El **método ProcessLicenseRevocationResponse** revoca las licencias del almacén de licencias local. Este método usa un blob de revocación de licencias (LRB) recibido de un servidor de revocación de licencias para identificar las licencias que se deben revocar.

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

*pbSignedLRB* \[ En\]
</dt> <dd>

Blob de revocación de licencias (LRB) recibido del servidor de revocación de licencias en respuesta a un desafío generado al llamar al [**método CreateLicenseRevocationChallenge.**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md)

</dd> <dt>

*cbSignedLRB* \[ En\]
</dt> <dd>

Tamaño del LRB en bytes.

</dd> <dt>

*ppbSignedACK* \[ out\]
</dt> <dd>

Dirección de un puntero que recibe la dirección de la confirmación de revocación de licencia. La confirmación debe enviarse al servicio de revocación de licencias. Cuando termine con estos datos, debe liberar la memoria llamando a **CoTaskMemFree**.

</dd> <dt>

*pwSignedACK* \[ out\]
</dt> <dd>

Dirección de una variable que recibe el tamaño de la confirmación en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMLicenseManagement (interfaz)**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





