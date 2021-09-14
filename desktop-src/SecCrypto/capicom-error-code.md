---
description: Define códigos de error devueltos por CAPICOM.
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: CAPICOM_ERROR_CODE enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ERROR_CODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: abdd2556ace3e3c3c82ccdeedc907d77f9ce1702
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171174"
---
# <a name="capicom_error_code-enumeration"></a>CAPICOM \_ ERROR \_ CODE (enumeración)

El **tipo de enumeración \_ CAPICOM ERROR \_ CODE** define códigos de error devueltos por CAPICOM.

> [!Note]  
> Visual Basic Los errores de Scripting Edition devuelven **un valor Err.number** mayor que cero. Para esos errores, **los valores de Err.Description** proporcionan información sobre la causa del error. Además de los errores Visual Basic Scripting Edition, los errores CAPICOM devuelven los códigos definidos por **CAPICOM \_ ERROR \_ CODE**.

 

## <a name="members"></a>Members




| Miembro | Descripción | Value | 
|--------|-------------|-------|
| <strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong> | Se usó un tipo de codificación que no es válido.<br /> En la lista siguiente se muestran los tipos de codificación válidos:<ul><li>CAPICOM_ENCODE_ANY</li><li>CAPICOM_ENCODE_BASE64</li><li>CAPICOM_ENCODE_BINARY</li></ul><br /> | 0x80880100 | 
| <strong>CAPICOM_E_EKU_INVALID_OID</strong> | No se puede establecer la propiedad <a href="eku-oid.md"><strong>OID</strong></a> del <a href="eku.md"><strong>objeto EKU</strong></a> porque la <a href="eku-name.md"><strong>propiedad Name</strong></a> no está establecida en CAPICOM_EKU_OTHER.<br /> Establezca la <a href="eku-name.md"><strong>propiedad Name</strong></a> en CAPICOM_EKU_OTHER antes de establecer la <a href="eku-oid.md"><strong>propiedad OID.</strong></a><br /> | 0x80880200 | 
| <strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong> | La <a href="eku-oid.md"><strong>propiedad OID</strong></a> del <a href="eku.md"><strong>objeto EKU</strong></a> no se ha inicializado. <br /> Establezca la <a href="eku-name.md"><strong>propiedad Name</strong></a> en cualquier cosa que no sea CAPICOM_EKU_OTHER o establezca la propiedad <strong>Name</strong> en CAPICOM_EKU_OTHER y la propiedad <a href="eku-oid.md"><strong>OID</strong></a> en un valor.<br /> | 0x80880201 | 
| <strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong> | El <a href="certificate.md"><strong>objeto Certificate</strong></a> no se ha inicializado.<br /> Normalmente, este código de error se devuelve cuando se crea una instancia <a href="certificate.md"><strong>de un objeto Certificate</strong></a> pero no se asocia a un certificado digital. Para asociar el objeto a un certificado digital, asígnelo a un objeto <strong>Certificate</strong> existente o llame al <a href="certificate-import.md"><strong>método Import.</strong></a><br /> | 0x80880210 | 
| <strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong> | El <a href="certificate.md"><strong>objeto</strong></a> Certificate no tiene una clave privada asociada.<br /> Este código de error se devuelve cuando se intenta firmar datos mediante <a href="certificate.md"><strong></strong></a> la clave privada del firmante, pero el objeto Certificate asociado al objeto <a href="signer.md"><strong>Signer</strong></a> no se puede usar para la operación de firma.<br /> | 0x80880211 | 
| <strong>CAPICOM_E_CHAIN_NOT_BUILT</strong> | El <a href="chain.md"><strong>objeto Chain</strong></a> no se ha inicializado. <br /> Para inicializar el <a href="chain.md"><strong>objeto Chain,</strong></a> llame al <a href="chain-build.md"><strong>método Build.</strong></a><br /> | 0x80880220 | 
| <strong>CAPICOM_E_STORE_NOT_OPENED</strong> | El <a href="store.md"><strong>objeto Store</strong></a> no se ha inicializado. <br /> Para inicializar <a href="store.md"><strong>el objeto Store,</strong></a> llame al <a href="store-open.md"><strong>método</strong></a> Open.<br /> | 0x80880230 | 
| <strong>CAPICOM_E_STORE_EMPTY</strong> | El <a href="store.md"><strong>objeto Store</strong></a> no contiene ningún objeto <a href="certificate.md"><strong>Certificate.</strong></a><br /> | 0x80880231 | 
| <strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong> | El <em>parámetro OpenMode</em> del <a href="store-open.md"><strong>método Store.Open</strong></a> no contiene un valor válido de CAPICOM_STORE_OPEN_MODE.<br /> En la lista siguiente se muestran los valores válidos de CAPICOM_STORE_OPEN_MODE:<ul><li>CAPICOM_STORE_OPEN_READ_ONLY</li><li>CAPICOM_STORE_OPEN_READ_WRITE</li><li>CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</li><li>CAPICOM_STORE_OPEN_EXISTING_ONLY</li><li>CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</li></ul><br /> | 0x80880232 | 
| <strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong> | El <em>valor SaveAs</em> pasado al <a href="store-export.md"><strong>método Export</strong></a> del objeto <a href="store.md"><strong>Store</strong></a> no era válido. <br /> En la lista siguiente se muestran los valores <em>válidos de SaveAs:</em><ul><li>CAPICOM_STORE_SAVE_AS_SERIALIZED</li><li>CAPICOM_STORE_SAVE_AS_PKCS7</li></ul><br /> | 0x80880233 | 
| <strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong> | La <a href="attribute-name.md"><strong>propiedad Name</strong></a> del objeto <a href="attribute.md"><strong>Attribute</strong></a> no se ha inicializado. <br /> Establezca la <a href="attribute-name.md"><strong>propiedad Name.</strong></a><br /> | 0x80880240 | 
| <strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong> | La <a href="attribute-value.md"><strong>propiedad Value</strong></a> del objeto <a href="attribute.md"><strong>Attribute</strong></a> no se ha inicializado. <br /> Establezca la <a href="attribute-value.md"><strong>propiedad</strong></a> Value.<br /> | 0x80880241 | 
| <strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong> | La <a href="attribute-name.md"><strong>propiedad Name</strong></a> del objeto <a href="attribute.md"><strong>Attribute</strong></a> no es válida. <br /> En la lista siguiente se muestran los nombres de atributo válidos:<ul><li>CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</li><li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</li><li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</li></ul><br /> | 0x80880242 | 
| <strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong> | La <a href="attribute-value.md"><strong>propiedad Value</strong></a> del objeto <a href="attribute.md"><strong>Attribute</strong></a> no es válida porque el tipo de datos no coincide con el tipo de datos indicado por la <strong>propiedad Name.</strong> <br /> Por ejemplo, si la <a href="attribute-value.md"><strong>propiedad Name</strong></a> se establece en CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, el tipo de datos debe ser <strong>DATE</strong>.<br /> | 0x80880243 | 
| <strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong> | El <a href="signer.md"><strong>objeto Signer</strong></a> no se ha inicializado. <br /> Para inicializar el <a href="signer.md"><strong>objeto Signer,</strong></a> establezca la <a href="signer-certificate.md"><strong>propiedad Certificate.</strong></a><br /> | 0x80880250 | 
| <strong>CAPICOM_E_SIGNER_NOT_FOUND</strong> | El firmante no se encuentra en el <a href="signeddata.md"><strong>objeto SignedData.</strong></a> <br /> Normalmente, esto no sucede con un <a href="signeddata.md"><strong>objeto SignedData</strong></a> creado por CAPICOM; sin embargo, si un producto de terceros creó el objeto <strong>SignedData,</strong> es posible que el certificado del firmante no se incluya en la estructura PKCS #7 firmante.<br /> | 0x80880251 | 
| <strong>CAPICOM_E_SIGNER_NO_CHAIN</strong> | No <a href="chain.md"><strong>se encuentra</strong></a> un objeto Chain en el objeto <a href="signer.md"><strong>Signer.</strong></a><br /> | 0x80880252 // v2.0 | 
| <strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong> | Se intenta usar el firmante de una manera que no es válida.<br /> | 0x80880253 //v2.0 | 
| <strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong> | El <a href="signeddata.md"><strong>objeto SignedData</strong></a> no se ha inicializado. <br /> Para inicializar <a href="signeddata.md"><strong>el objeto SignedData,</strong></a> establezca la <a href="signeddata-content.md"><strong>propiedad Content</strong></a> o llame al <a href="signeddata-verify.md"><strong>método Verify.</strong></a><br /> | 0x80880260 | 
| <strong>CAPICOM_E_SIGN_INVALID_TYPE</strong> | El <a href="signeddata.md"><strong>objeto SignedData</strong></a> contiene un tipo que no es válido. <br /> Normalmente, esto sucede cuando se intenta comprobar un mensaje con sobres con un <a href="signeddata.md"><strong>objeto SignedData</strong></a> o viceversa.<br /> | 0x80880261 | 
| <strong>CAPICOM_E_SIGN_NOT_SIGNED</strong> | El <a href="signeddata.md"><strong>objeto SignedData</strong></a> no se ha firmado. <br /> Para firmar el <a href="signeddata.md"><strong>objeto SignedData,</strong></a> llame al <a href="signeddata-sign.md"><strong>método Sign.</strong></a><br /> | 0x80880262 | 
| <strong>CAPICOM_E_INVALID_ALGORITHM</strong> | El valor del algoritmo para <a href="algorithm-name.md"><strong>la propiedad Name</strong></a> del objeto <a href="algorithm.md"><strong>Algorithm</strong></a> no es válido. <br /> En la lista siguiente se muestran los valores de algoritmo válidos para la <a href="algorithm-name.md"><strong>propiedad</strong></a> Name:<ul><li>CAPICOM_ENCRYPTION_ALGORITHM_RC2</li><li>CAPICOM_ENCRYPTION_ALGORITHM_RC4</li><li>CAPICOM_ENCRYPTION_ALGORITHM_DES</li><li>CAPICOM_ENCRYPTION_ALGORITHM_3DES</li></ul><br /> | 0x80880270 | 
| <strong>CAPICOM_E_INVALID_KEY_LENGTH</strong> | El valor de longitud de clave para <a href="algorithm-keylength.md"><strong>la propiedad KeyLength</strong></a> del <a href="algorithm.md"><strong>objeto Algorithm</strong></a> no es válido. <br /> En la lista siguiente se muestran los valores de longitud de clave válidos para <a href="algorithm-keylength.md"><strong>la propiedad KeyLength:</strong></a><ul><li>CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</li><li>CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</li><li>CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</li><li>CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</li></ul><br /> | 0x80880271 | 
| <strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong> | El <a href="envelopeddata.md"><strong>objeto EnvelopedData</strong></a> no se ha inicializado. <br /> Para inicializar <a href="envelopeddata.md"><strong>el objeto EnvelopedData,</strong></a> establezca la <a href="envelopeddata-content.md"><strong>propiedad Content</strong></a> o llame al <a href="envelopeddata-decrypt.md"><strong>método Decrypt.</strong></a><br /> | 0x80880280 | 
| <strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong> | El <a href="envelopeddata.md"><strong>objeto EnvelopedData</strong></a> contiene un tipo que no es válido. <br /> Normalmente, esto sucede cuando se intenta comprobar un mensaje firmado con un objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> o viceversa.<br /> | 0x80880281 | 
| <strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong> | No se especifica ningún destinatario en el objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> cuando se llama al método <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> de un objeto <strong>EnvelopedData.</strong> <br /> Para agregar un destinatario, llame al <a href="recipients-add.md"><strong>método Recipients.Add.</strong></a><br /> | 0x80880282 | 
| <strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong> | El destinatario no se encuentra en el <a href="envelopeddata.md"><strong>objeto EnvelopedData.</strong></a> <br /> Normalmente, esto no sucede con un objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> creado por CAPICOM; sin embargo, si un producto de terceros creó el objeto <strong>EnvelopedData,</strong> es posible que el certificado del destinatario no se incluya en la PKCS #7 cliente.<br /> | 0x80880283 | 
| <strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong> | El <a href="encrypteddata.md"><strong>objeto EncryptedData</strong></a> no se ha inicializado. <br /> Para inicializar <a href="encrypteddata.md"><strong>el objeto EncryptedData,</strong></a> establezca la <a href="encrypteddata-content.md"><strong>propiedad Content</strong></a> o llame al <a href="encrypteddata-decrypt.md"><strong>método Decrypt.</strong></a><br /> | 0x80880290 | 
| <strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong> | El <a href="encrypteddata.md"><strong>objeto EncryptedData</strong></a> no es un tipo válido. <br /> Normalmente, esto significa que los datos están dañados.<br /> | 0x80880291 | 
| <strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong> | No se ha inicializado el secreto de un objeto <a href="encrypteddata.md"><strong>EncryptedData.</strong></a> <br /> Para inicializar el secreto de un <a href="encrypteddata.md"><strong>objeto EncryptedData,</strong></a> llame al <a href="encrypteddata-setsecret.md"><strong>método SetSecret.</strong></a><br /> | 0x80880292 | 
| <strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong> | El <a href="privatekey.md"><strong>objeto PrivateKey</strong></a> no se ha inicializado.<br /> | 0x80880300 // v2.0 | 
| <strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong> | No se puede exportar el objeto <a href="privatekey.md"><strong>PrivateKey.</strong></a><br /> | 0x80880301 // v2.0 | 
| <strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong> | El <a href="encodeddata.md"><strong>objeto EncodedData</strong></a> no se ha inicializado.<br /> | 0x80880320 // v2.0 | 
| <strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong> | El <a href="extension.md"><strong>objeto</strong></a> Extension no se ha inicializado.<br /> | 0x80880330 // v2.0 | 
| <strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong> | La <a href="extendedproperty-propid.md"><strong>propiedad PropID</strong></a> del <a href="extendedproperty.md"><strong>objeto ExtendedProperty</strong></a> no se ha inicializado.<br /> | 0x80880340 // v2.0 | 
| <strong>CAPICOM_E_FIND_INVALID_TYPE</strong> | El <em>parámetro FindType</em> del <a href="certificates-find.md"><strong>método Certificates.Find</strong></a> no es un valor de la <a href="capicom-certificate-find-type.md"><strong>enumeración CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> datos.<br /> | 0x80880350 // v2.0 | 
| <strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong> | La directiva predefinida especificada para la operación de búsqueda no es válida.<br /> | 0x80880351 // v2.0 | 
| <strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong> | El <a href="signedcode.md"><strong>objeto SignedCode</strong></a> no se ha inicializado.<br /> | 0x80880360 // v2.0 | 
| <strong>CAPICOM_E_CODE_NOT_SIGNED</strong> | El <a href="signedcode.md"><strong>objeto SignedCode</strong></a> no se ha firmado.<br /> Para firmar el <a href="signedcode.md"><strong>objeto SignedCode,</strong></a> llame al <a href="signedcode-sign.md"><strong>método Sign.</strong></a><br /> | 0x80880361 // v2.0 | 
| <strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong> | No <a href="signedcode-description.md"><strong>se</strong></a> ha inicializado la propiedad Description del objeto <a href="signedcode.md"><strong>SignedCode.</strong></a><br /> | 0x80880362 // v2.0 | 
| <strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong> | La <a href="signedcode-descriptionurl.md"><strong>propiedad DescriptionURL</strong></a> del <a href="signedcode.md"><strong>objeto SignedCode</strong></a> no se ha inicializado.<br /> | 0x80880363 // v2.0 | 
| <strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong> | El <em>parámetro URL</em> del método <a href="signedcode-timestamp.md"><strong>SignedCode.Timestamp</strong></a> no es válido.<br /> | 0x80880364 // v2.0 | 
| <strong>CAPICOM_E_HASH_NO_DATA</strong> | El <a href="hasheddata.md"><strong>objeto HashedData</strong></a> no contiene ningún dato.<br /> | 0x80880370 // v2.0 | 
| <strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong> | El tipo de conversión no es válido.<br /> | 0x80880380 // v2.0 | 
| <strong>CAPICOM_E_NOT_SUPPORTED</strong> | La operación solicitada no se admite en la plataforma actual. <br /> | 0x80880900 | 
| <strong>CAPICOM_E_UI_DISABLED</strong> | Al firmar, no <a href="signer-certificate.md"><strong>se ha</strong></a> establecido la propiedad Certificate del objeto <a href="signer.md"><strong>Signer,</strong></a> pero se ha deshabilitado la solicitud del certificado de usuario. <br /> Habilite el símbolo del sistema estableciendo la propiedad <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> del objeto <a href="settings.md"><strong>Configuración</strong></a> o establezca la propiedad <a href="signer-certificate.md"><strong>Certificate</strong></a> del <a href="signer.md"><strong>objeto Signer.</strong></a><br /> | 0x80880901 | 
| <strong>CAPICOM_E_CANCELLED</strong> | El usuario ha cancelado la operación. <br /> Esto sucede cuando se solicita al usuario permiso para llevar a cabo una determinada operación, como el acceso a la clave privada, y el usuario cancela la operación.<br /> | 0x80880902 | 
| <strong>CAPICOM_E_NOT_ALLOWED</strong> | No se permite la operación intentada.<br /> Por ejemplo, no se permite cambiar la <a href="extendedproperty-propid.md"><strong>propiedad PropID</strong></a> de un <a href="extendedproperty.md"><strong>objeto ExtendedProperty</strong></a> si el objeto está asociado a un certificado.<br /> | 0x80880903 // v2.0 | 
| <strong>CAPICOM_E_OUT_OF_RESOURCE</strong> | CAPICOM se ha quedo sin un recurso.<br /> | 0x80880904 // v2.0 | 
| <strong>CAPICOM_E_INTERNAL</strong> | Se ha producido un error interno. <br /> Póngase en contacto con el soporte técnico de Microsoft para obtener ayuda.<br /> | 0x80880911 | 
| <strong>CAPICOM_E_UNKNOWN</strong> | Se ha producido un error desconocido. <br /> Recopile toda la información posible y póngase en contacto con su proveedor.<br /> | 0x80880999 | 




## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




