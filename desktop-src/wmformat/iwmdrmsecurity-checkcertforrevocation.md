---
title: Método IWMDRMSecurity CheckCertForRevocation (wmdrmsdk. h)
description: El método CheckCertForRevocation determina si se ha revocado un certificado.
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- Método CheckCertForRevocation formato de Windows Media
- Método CheckCertForRevocation formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método CheckCertForRevocation
topic_type:
- apiref
api_name:
- IWMDRMSecurity.CheckCertForRevocation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2439085c6483720e84956ef9932f4f1ab95535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649578"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a>IWMDRMSecurity:: CheckCertForRevocation (método)

El método **CheckCertForRevocation** determina si se ha revocado un certificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckCertForRevocation(
  [in]  REFGUID rguidRevocationList,
  [in]  BYTE    *pbCert,
  [in]  DWORD   cbCert,
  [out] BOOL    *fRevoked
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rguidRevocationList* \[ de\]
</dt> <dd>

GUID que identifica la lista de revocación que se va a usar. Establezca en uno de los valores de la tabla siguiente.



| Constante GUID                 | Descripción                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| \_aplicación REVOCATIONTYPE de WMDRM \_    | Especifica la lista de revocación de certificados de la aplicación.                                     |
| \_dispositivo REVOCATIONTYPE \_ WMDRM | Especifica la lista de revocación de certificados de dispositivo.                                          |
| \_CARDEA REVOCATIONTYPE \_ WMDRM | Especifica la lista de revocación de certificados de DRM de Microsoft Windows Media para dispositivos de red. |



 

</dd> <dt>

*pbCert* \[ de\]
</dt> <dd>

Búfer que contiene el certificado que se va a buscar.

</dd> <dt>

*cbCert* \[ de\]
</dt> <dd>

Tamaño del búfer *pbCert*, en bytes.

</dd> <dt>

*fRevoked* \[ enuncia\]
</dt> <dd>

En la salida, indica si el certificado está presente en la lista de revocación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





