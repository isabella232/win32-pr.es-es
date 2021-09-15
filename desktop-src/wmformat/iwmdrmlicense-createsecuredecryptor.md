---
title: Método IWMDRMLicense CreateSecureDecryptor (Wmdrmsdk.h)
description: El método CreateSecureDecryptor crea un objeto descifrador seguro. El descifrador seguro difiere del descifrador normal en que descifra el contenido y, a continuación, lo vuelve a cifrar según la configuración especificada en los parámetros de este método.
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- Método CreateSecureDecryptor windows Media Format
- Método CreateSecureDecryptor windows Media Format , interfaz IWMDRMLicense
- IWMDRMLicense interface windows Media Format , CreateSecureDecryptor method
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466483"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a>IWMDRMLicense::CreateSecureDecryptor (método)

El **método CreateSecureDecryptor** crea un objeto descifrador seguro. El descifrador seguro difiere del descifrador normal en que descifra el contenido y, a continuación, lo vuelve a cifrar según la configuración especificada en los parámetros de este método.

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

*pbCertificate* \[ En\]
</dt> <dd>

Certificado de la aplicación que realiza la llamada.

</dd> <dt>

*cbCertificate* \[ En\]
</dt> <dd>

Tamaño del certificado en bytes.

</dd> <dt>

*dwCertificateType* \[ En\]
</dt> <dd>

Tipo del certificado. Se establece en XML DE TIPO \_ \_ DE CERTIFICADO \_ WMDRM.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Tipo de protección de sesión que se va a usar para volver a codificar. Debe establecerse en una de las constantes de la tabla siguiente:



| Constante                     | Descripción                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| WMDRM \_ PROTECTION \_ TYPE \_ RC4 | Usa el cifrado RC4 para el cifrado de sesión. Esta es la única protección de sesión admitida para esta versión. |



 

</dd> <dt>

*pbInitializationVector* \[ out\]
</dt> <dd>

Recibe el vector de inicialización. El vector de inicialización es RSA cifrado mediante el esquema de relleno OAEP con la clave pública RSA que se encuentra en el certificado. Establezca en **NULL** para recibir el tamaño de búfer necesario *eninitializationVector*.

</dd> <dt>

*initInitializationVector* \[ in, out\]
</dt> <dd>

En la entrada, el tamaño del búfer pasado *como pbInitializationVector*. En la salida, el tamaño de la parte usada del búfer. Si pasa **NULL para** *pbInitializationVector*, este valor se establece en el tamaño de búfer necesario en la salida.

</dd> <dt>

*ppDecryptor* \[ out\]
</dt> <dd>

Recibe un puntero a [**la interfaz IWMDRMDecrypt**](iwmdrmdecrypt.md) del objeto recién creado.

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

[**IWMDRMLicense (Interfaz)**](iwmdrmlicense.md)
</dt> </dl>

 

 





