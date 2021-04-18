---
title: Método IWMDRMSecurity GetMachineCertificate (wmdrmsdk. h)
description: El método GetMachineCertificate recupera el certificado de equipo del subsistema DRM en el equipo cliente.
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- Método GetMachineCertificate formato de Windows Media
- Método GetMachineCertificate formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método GetMachineCertificate
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetMachineCertificate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6c66c54ab9528a458910def5978ec83b191654
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649759"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a>IWMDRMSecurity:: GetMachineCertificate (método)

El método **GetMachineCertificate** recupera el certificado de equipo del subsistema DRM en el equipo cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMachineCertificate(
  [in]      DWORD dwCertificateType,
  [out]     BYTE  rgbVersion[4],
  [out]     BYTE  **ppbCertificate,
  [in, out] DWORD *pcbCertificate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwCertificateType* \[ de\]
</dt> <dd>

Tipo de certificado que se va a recuperar. Establezca en uno de los valores de la tabla siguiente.



| Value                        | Descripción                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| Tipo de certificado de WMDRM \_ \_ \_ v1 | El certificado se recuperará en el formato utilizado por los componentes heredados.            |
| Tipo de certificado de WMDRM \_ \_ \_ V2 | El certificado se recuperará en el formato utilizado por los componentes de Windows Vista. |



 

</dd> <dt>

*rgbVersion \[ 4 \]* \[\]
</dt> <dd>

Matriz de cuatro bytes que especifica la versión del subsistema DRM en el equipo cliente.

</dd> <dt>

*ppbCertificate* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe un puntero a los datos del certificado. Establezca en **null** para que el método proporcione el tamaño de búfer necesario para almacenar el certificado en *pcbCertificate*.

</dd> <dt>

*pcbCertificate* \[ in, out\]
</dt> <dd>

Tamaño del certificado en bytes. Si *ppbCertificate* es **null**, este valor se establecerá en el tamaño del certificado. Si *ppbCertificate* no es **null**, este valor debe establecerse en el tamaño del búfer.

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

 

 





