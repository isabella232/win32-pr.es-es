---
description: Copia un certificado en una cadena codificada.
ms.assetid: bae7fb57-6b44-4aac-a635-b5b82de1f68d
title: ICertificate2::Export (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Export
- ICertificate2.Export
- ICertificate.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f002be332097baa0ad0947367259d15f0657d276770682b709402e2f0a333290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771772"
---
# <a name="icertificate2export-method"></a>ICertificate2::Export (método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Export** copia un certificado en una cadena codificada. La cadena codificada se puede escribir en un archivo o importarse en un nuevo [**objeto Certificate.**](certificate.md)

## <a name="syntax"></a>Sintaxis


```VB
Certificate.Export( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EncodingType* \[ en, opcional\]
</dt> <dd>

Valor de la enumeración [**CAPICOM \_ ENCODING \_ TYPE**](capicom-encoding-type.md) que especifica el tipo de codificación para la operación de exportación. El valor predeterminado es **CAPICOM \_ ENCODE \_ BASE64.** En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ ENCODE \_ ANY**</dt> </dl>          | Este tipo de codificación solo se usa cuando los datos de entrada tienen un tipo de codificación desconocido. Si este valor se usa para especificar el tipo de codificación de la salida, se usará CAPICOM \_ ENCODE \_ BASE64 en su lugar. Introducido en CAPICOM 2.0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CODIFICACIÓN \_ CAPICOM \_ BASE64**</dt> </dl> | Los datos se guardan como una cadena codificada en base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM \_ ENCODE \_ BINARY**</dt> </dl> | Los datos se guardan como una secuencia binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cadena que contiene el certificado exportado en el formato de codificación especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos criptografía](cryptography-objects.md)
</dt> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
