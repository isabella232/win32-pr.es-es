---
title: Método IWMDRMLicense CreateSecureDecryptor (wmdrmsdk. h)
description: El método CreateSecureDecryptor crea un objeto descifrador seguro. El descifrador seguro difiere del descifrador normal en que descifra el contenido y, a continuación, lo vuelve a cifrar según la configuración especificada en los parámetros de este método.
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- Método CreateSecureDecryptor formato de Windows Media
- Método CreateSecureDecryptor formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método CreateSecureDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateSecureDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ededb4c985e345c1e40563d02c87bfe447b8960f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708168"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a>IWMDRMLicense:: CreateSecureDecryptor (método)

El método **CreateSecureDecryptor** crea un objeto descifrador seguro. El descifrador seguro difiere del descifrador normal en que descifra el contenido y, a continuación, lo vuelve a cifrar según la configuración especificada en los parámetros de este método.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateSecureDecryptor(
  [in]      BYTE          *pbCertificate,
  [in]      DWORD         cbCertificate,
  [in]      DWORD         dwCertificateType,
  [in]      DWORD         dwFlags,
  [out]     BYTE          *pbInitializationVector,
  [in, out] DWORD         *pcbInitializationVector,
  [out]     IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbCertificate* \[ de\]
</dt> <dd>

Certificado de la aplicación que realiza la llamada.

</dd> <dt>

*cbCertificate* \[ de\]
</dt> <dd>

Tamaño del certificado en bytes.

</dd> <dt>

*dwCertificateType* \[ de\]
</dt> <dd>

Tipo del certificado. Establezca en \_ tipo de certificado WMDRM \_ \_ xml.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

El tipo de protección de sesión que se va a usar para la recodificación. Debe establecerse en una de las constantes de la tabla siguiente:



| Constante                     | Descripción                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| Tipo de protección de WMDRM \_ \_ \_ RC4 | Usa el cifrado RC4 para el cifrado de sesión. Esta es la única protección de sesión compatible para esta versión. |



 

</dd> <dt>

*pbInitializationVector* \[ enuncia\]
</dt> <dd>

Recibe el vector de inicialización. El vector de inicialización es RSA cifrado mediante el esquema de relleno OAEP con la clave pública RSA que se encuentra en el certificado. Establezca en **null** para recibir el tamaño de búfer necesario en *pcbInitializationVector*.

</dd> <dt>

*pcbInitializationVector* \[ in, out\]
</dt> <dd>

En la entrada, el tamaño del búfer pasado como *pbInitializationVector*. En la salida, tamaño de la parte utilizada del búfer. Si pasa **null** para *pbInitializationVector*, este valor se establece en el tamaño de búfer necesario en la salida.

</dd> <dt>

*ppDecryptor* \[ enuncia\]
</dt> <dd>

Recibe un puntero a la interfaz [**IWMDRMDecrypt**](iwmdrmdecrypt.md) del objeto recién creado.

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

[**Interfaz IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





