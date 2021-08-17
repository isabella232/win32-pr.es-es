---
title: Método IWMDRMSecurity CheckCertForRevocation (Wmdrmsdk.h)
description: El método CheckCertForRevocation determina si se ha revocado un certificado.
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- Método CheckCertForRevocation windows Media Format
- Método CheckCertForRevocation windows Media Format , interfaz IWMDRMSecurity
- IWMDRMSecurity interface windows Media Format , CheckCertForRevocation method
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
ms.openlocfilehash: e090dfb655837ad2cf36cf45486488fde1440b499b73f16fdfbdaf2989532687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700791"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a>IWMDRMSecurity::CheckCertForRevocation (método)

El **método CheckCertForRevocation** determina si se ha revocado un certificado.

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

*rguidRevocationList* \[ En\]
</dt> <dd>

GUID que identifica la lista de revocación que se usará. Establezca en uno de los valores de la tabla siguiente.



| Constante GUID                 | Descripción                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| APLICACIÓN WMDRM \_ \_ REVOCATIONTYPE    | Especifica la lista de revocación de certificados de aplicación.                                     |
| DISPOSITIVO WMDRM \_ \_ REVOCATIONTYPE | Especifica la lista de revocación de certificados de dispositivo.                                          |
| WMDRM \_ REVOCATIONTYPE \_ CARDEA | Especifica la lista de revocación de certificados Windows DRM multimedia de Microsoft para dispositivos de red. |



 

</dd> <dt>

*pbCert* \[ En\]
</dt> <dd>

Búfer que contiene el certificado que se buscará.

</dd> <dt>

*cbCert* \[ En\]
</dt> <dd>

Tamaño del búfer *pbCert*, en bytes.

</dd> <dt>

*fRevoked* \[ out\]
</dt> <dd>

En la salida, indica si el certificado está presente en la lista de revocación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMDRMSecurity (interfaz)**](iwmdrmsecurity.md)
</dt> </dl>

 

 





