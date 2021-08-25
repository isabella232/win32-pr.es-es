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
ms.openlocfilehash: 4bdcda4e5ff70c0f576816830d788480763945e7a3940a8d87707cb251595c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879325"
---
# <a name="capicom_error_code-enumeration"></a>CAPICOM \_ ERROR \_ CODE (enumeración)

El **tipo de enumeración \_ CAPICOM ERROR \_ CODE** define códigos de error devueltos por CAPICOM.

> [!Note]  
> Visual Basic Los errores de Scripting Edition devuelven **un valor Err.number** mayor que cero. Para esos errores, **los valores de Err.Description** proporcionan información sobre la causa del error. Además de los Visual Basic de Scripting Edition, los errores de CAPICOM devuelven los códigos definidos por **CAPICOM \_ ERROR \_ CODE**.

 

## <a name="members"></a>Miembros



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Miembro</th>
<th>Descripción</th>
<th>Value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></td>
<td>Se usó un tipo de codificación que no es válido.<br/> En la lista siguiente se muestran los tipos de codificación válidos:
<ul>
<li>CAPICOM_ENCODE_ANY</li>
<li>CAPICOM_ENCODE_BASE64</li>
<li>CAPICOM_ENCODE_BINARY</li>
</ul>
<br/></td>
<td>0x80880100</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_EKU_INVALID_OID</strong></td>
<td>No se puede establecer la propiedad <a href="eku-oid.md"><strong>OID</strong></a> del <a href="eku.md"><strong>objeto EKU</strong></a> porque la <a href="eku-name.md"><strong>propiedad Name</strong></a> no está establecida en CAPICOM_EKU_OTHER.<br/> Establezca la <a href="eku-name.md"><strong>propiedad Name</strong></a> en CAPICOM_EKU_OTHER antes de establecer la <a href="eku-oid.md"><strong>propiedad OID.</strong></a><br/></td>
<td>0x80880200</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></td>
<td>La <a href="eku-oid.md"><strong>propiedad OID</strong></a> del <a href="eku.md"><strong>objeto EKU</strong></a> no se ha inicializado. <br/> Establezca la <a href="eku-name.md"><strong>propiedad Name</strong></a> en algo distinto de CAPICOM_EKU_OTHER o establezca la propiedad <strong>Name</strong> en CAPICOM_EKU_OTHER y la propiedad <a href="eku-oid.md"><strong>OID</strong></a> en un valor.<br/></td>
<td>0x80880201</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></td>
<td>El <a href="certificate.md"><strong>objeto Certificate</strong></a> no se ha inicializado.<br/> Normalmente, este código de error se devuelve cuando se crea una instancia de un <a href="certificate.md"><strong>objeto Certificate</strong></a> pero no se asocia a un certificado digital. Para asociar el objeto a un certificado digital, asígnelo a un objeto <strong>Certificate</strong> existente o llame al <a href="certificate-import.md"><strong>método Import.</strong></a><br/></td>
<td>0x80880210</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></td>
<td>El <a href="certificate.md"><strong>objeto</strong></a> Certificate no tiene una clave privada asociada.<br/> Este código de error se devuelve cuando se intenta firmar datos mediante <a href="certificate.md"><strong></strong></a> la clave privada del firmante, pero el objeto Certificate asociado al objeto <a href="signer.md"><strong>Signer</strong></a> no se puede usar para la operación de firma.<br/></td>
<td>0x80880211</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></td>
<td>El <a href="chain.md"><strong>objeto Chain</strong></a> no se ha inicializado. <br/> Para inicializar el <a href="chain.md"><strong>objeto Chain,</strong></a> llame al <a href="chain-build.md"><strong>método Build.</strong></a><br/></td>
<td>0x80880220</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_STORE_NOT_OPENED</strong></td>
<td>El <a href="store.md"><strong>objeto Store</strong></a> no se ha inicializado. <br/> Para inicializar <a href="store.md"><strong>el objeto Store,</strong></a> llame al <a href="store-open.md"><strong>método</strong></a> Open.<br/></td>
<td>0x80880230</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_STORE_EMPTY</strong></td>
<td>El <a href="store.md"><strong>objeto Store</strong></a> no contiene ningún objeto <a href="certificate.md"><strong>Certificate.</strong></a><br/></td>
<td>0x80880231</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></td>
<td>El <em>parámetro OpenMode</em> del <a href="store-open.md"><strong>método Store.Open</strong></a> no contiene un valor válido de CAPICOM_STORE_OPEN_MODE.<br/> En la lista siguiente se muestran los valores válidos de CAPICOM_STORE_OPEN_MODE:
<ul>
<li>CAPICOM_STORE_OPEN_READ_ONLY</li>
<li>CAPICOM_STORE_OPEN_READ_WRITE</li>
<li>CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</li>
<li>CAPICOM_STORE_OPEN_EXISTING_ONLY</li>
<li>CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</li>
</ul>
<br/></td>
<td>0x80880232</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></td>
<td>El <em>valor SaveAs</em> pasado al <a href="store-export.md"><strong>método Export</strong></a> del objeto <a href="store.md"><strong>Store</strong></a> no era válido. <br/> En la lista siguiente se muestran los valores <em>válidos de SaveAs:</em>
<ul>
<li>CAPICOM_STORE_SAVE_AS_SERIALIZED</li>
<li>CAPICOM_STORE_SAVE_AS_PKCS7</li>
</ul>
<br/></td>
<td>0x80880233</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></td>
<td>La <a href="attribute-name.md"><strong>propiedad Name</strong></a> del objeto <a href="attribute.md"><strong>Attribute</strong></a> no se ha inicializado. <br/> Establezca la <a href="attribute-name.md"><strong>propiedad Name.</strong></a><br/></td>
<td>0x80880240</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></td>
<td>La <a href="attribute-value.md"><strong>propiedad Value</strong></a> del objeto <a href="attribute.md"><strong>Attribute</strong></a> no se ha inicializado. <br/> Establezca la <a href="attribute-value.md"><strong>propiedad</strong></a> Value.<br/></td>
<td>0x80880241</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></td>
<td>La <a href="attribute-name.md"><strong>propiedad Name</strong></a> del objeto <a href="attribute.md"><strong>Attribute</strong></a> no es válida. <br/> En la lista siguiente se muestran los nombres de atributo válidos:
<ul>
<li>CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</li>
<li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</li>
<li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</li>
</ul>
<br/></td>
<td>0x80880242</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></td>
<td>La <a href="attribute-value.md"><strong>propiedad Value</strong></a> del objeto <a href="attribute.md"><strong>Attribute</strong></a> no es válida porque el tipo de datos no coincide con el tipo de datos indicado por la <strong>propiedad Name.</strong> <br/> Por ejemplo, si la <a href="attribute-value.md"><strong>propiedad Name</strong></a> se establece en CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, el tipo de datos debe ser <strong>DATE</strong>.<br/></td>
<td>0x80880243</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></td>
<td>El <a href="signer.md"><strong>objeto Signer</strong></a> no se ha inicializado. <br/> Para inicializar el <a href="signer.md"><strong>objeto Signer,</strong></a> establezca la <a href="signer-certificate.md"><strong>propiedad Certificate.</strong></a><br/></td>
<td>0x80880250</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></td>
<td>El firmante no se encuentra en el <a href="signeddata.md"><strong>objeto SignedData.</strong></a> <br/> Normalmente, esto no sucede con un <a href="signeddata.md"><strong>objeto SignedData</strong></a> creado por CAPICOM; sin embargo, si un producto de terceros creó el objeto <strong>SignedData,</strong> es posible que el certificado del firmante no se incluya en la estructura PKCS #7 firmante.<br/></td>
<td>0x80880251</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></td>
<td>No <a href="chain.md"><strong>se encuentra</strong></a> un objeto Chain en el objeto <a href="signer.md"><strong>Signer.</strong></a><br/></td>
<td>0x80880252 // v2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></td>
<td>Se intenta usar el firmante de una manera que no es válida.<br/></td>
<td>0x80880253 //v2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></td>
<td>El <a href="signeddata.md"><strong>objeto SignedData</strong></a> no se ha inicializado. <br/> Para inicializar <a href="signeddata.md"><strong>el objeto SignedData,</strong></a> establezca la <a href="signeddata-content.md"><strong>propiedad Content</strong></a> o llame al <a href="signeddata-verify.md"><strong>método Verify.</strong></a><br/></td>
<td>0x80880260</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></td>
<td>El <a href="signeddata.md"><strong>objeto SignedData</strong></a> contiene un tipo que no es válido. <br/> Normalmente, esto sucede cuando se intenta comprobar un mensaje sobre con un <a href="signeddata.md"><strong>objeto SignedData</strong></a> o viceversa.<br/></td>
<td>0x80880261</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></td>
<td>El <a href="signeddata.md"><strong>objeto SignedData</strong></a> no se ha firmado. <br/> Para firmar el <a href="signeddata.md"><strong>objeto SignedData,</strong></a> llame al <a href="signeddata-sign.md"><strong>método Sign.</strong></a><br/></td>
<td>0x80880262</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INVALID_ALGORITHM</strong></td>
<td>El valor del algoritmo para <a href="algorithm-name.md"><strong>la propiedad Name</strong></a> del objeto <a href="algorithm.md"><strong>Algorithm</strong></a> no es válido. <br/> En la lista siguiente se muestran los valores de algoritmo válidos para la <a href="algorithm-name.md"><strong>propiedad Name:</strong></a>
<ul>
<li>CAPICOM_ENCRYPTION_ALGORITHM_RC2</li>
<li>CAPICOM_ENCRYPTION_ALGORITHM_RC4</li>
<li>CAPICOM_ENCRYPTION_ALGORITHM_DES</li>
<li>CAPICOM_ENCRYPTION_ALGORITHM_3DES</li>
</ul>
<br/></td>
<td>0x80880270</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></td>
<td>El valor de longitud de clave para <a href="algorithm-keylength.md"><strong>la propiedad KeyLength</strong></a> del <a href="algorithm.md"><strong>objeto Algorithm</strong></a> no es válido. <br/> En la lista siguiente se muestran los valores de longitud de clave válidos para <a href="algorithm-keylength.md"><strong>la propiedad KeyLength:</strong></a>
<ul>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</li>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</li>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</li>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</li>
</ul>
<br/></td>
<td>0x80880271</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></td>
<td>El <a href="envelopeddata.md"><strong>objeto EnvelopedData</strong></a> no se ha inicializado. <br/> Para inicializar <a href="envelopeddata.md"><strong>el objeto EnvelopedData,</strong></a> establezca la <a href="envelopeddata-content.md"><strong>propiedad Content</strong></a> o llame al <a href="envelopeddata-decrypt.md"><strong>método Decrypt.</strong></a><br/></td>
<td>0x80880280</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></td>
<td>El <a href="envelopeddata.md"><strong>objeto EnvelopedData</strong></a> contiene un tipo que no es válido. <br/> Normalmente, esto sucede cuando se intenta comprobar un mensaje firmado con un objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> o viceversa.<br/></td>
<td>0x80880281</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></td>
<td>No se especifica ningún destinatario en el objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> cuando se llama al método <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> de un objeto <strong>EnvelopedData.</strong> <br/> Para agregar un destinatario, llame al <a href="recipients-add.md"><strong>método Recipients.Add.</strong></a><br/></td>
<td>0x80880282</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></td>
<td>No se encuentra el destinatario en el <a href="envelopeddata.md"><strong>objeto EnvelopedData.</strong></a> <br/> Normalmente, esto no sucede con un objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> creado por CAPICOM; sin embargo, si el objeto <strong>EnvelopedData</strong> lo creó un producto de terceros, es posible que el certificado del destinatario no se incluya en la PKCS #7 cliente.<br/></td>
<td>0x80880283</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></td>
<td>El <a href="encrypteddata.md"><strong>objeto EncryptedData</strong></a> no se ha inicializado. <br/> Para inicializar <a href="encrypteddata.md"><strong>el objeto EncryptedData,</strong></a> establezca la <a href="encrypteddata-content.md"><strong>propiedad Content</strong></a> o llame al <a href="encrypteddata-decrypt.md"><strong>método Decrypt.</strong></a><br/></td>
<td>0x80880290</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></td>
<td>El <a href="encrypteddata.md"><strong>objeto EncryptedData</strong></a> no es un tipo válido. <br/> Normalmente, esto significa que los datos están dañados.<br/></td>
<td>0x80880291</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></td>
<td>No se ha inicializado el secreto de un objeto <a href="encrypteddata.md"><strong>EncryptedData.</strong></a> <br/> Para inicializar el secreto de un <a href="encrypteddata.md"><strong>objeto EncryptedData,</strong></a> llame al <a href="encrypteddata-setsecret.md"><strong>método SetSecret.</strong></a><br/></td>
<td>0x80880292</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></td>
<td>El <a href="privatekey.md"><strong>objeto PrivateKey</strong></a> no se ha inicializado.<br/></td>
<td>0x80880300 // v2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></td>
<td>No se puede exportar el objeto <a href="privatekey.md"><strong>PrivateKey.</strong></a><br/></td>
<td>0x80880301 // v2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></td>
<td>El <a href="encodeddata.md"><strong>objeto EncodedData</strong></a> no se ha inicializado.<br/></td>
<td>0x80880320 // v2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></td>
<td>El <a href="extension.md"><strong>objeto Extension</strong></a> no se ha inicializado.<br/></td>
<td>0x80880330 // v2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></td>
<td>No se ha inicializado la propiedad <a href="extendedproperty-propid.md"><strong>PropID</strong></a> del <a href="extendedproperty.md"><strong>objeto ExtendedProperty.</strong></a><br/></td>
<td>0x80880340 // v2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></td>
<td>El <em>parámetro FindType</em> del <a href="certificates-find.md"><strong>método Certificates.Find</strong></a> no es un valor de la <a href="capicom-certificate-find-type.md"><strong>enumeración CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> datos.<br/></td>
<td>0x80880350 // v2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></td>
<td>La directiva predefinida especificada para la operación de búsqueda no es válida.<br/></td>
<td>0x80880351 // v2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></td>
<td>El <a href="signedcode.md"><strong>objeto SignedCode</strong></a> no se ha inicializado.<br/></td>
<td>0x80880360 // v2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></td>
<td>El <a href="signedcode.md"><strong>objeto SignedCode</strong></a> no se ha firmado.<br/> Para firmar el <a href="signedcode.md"><strong>objeto SignedCode,</strong></a> llame al <a href="signedcode-sign.md"><strong>método Sign.</strong></a><br/></td>
<td>0x80880361 // v2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></td>
<td>La <a href="signedcode-description.md"><strong>propiedad Description</strong></a> del objeto <a href="signedcode.md"><strong>SignedCode</strong></a> no se ha inicializado.<br/></td>
<td>0x80880362 // v2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></td>
<td>La <a href="signedcode-descriptionurl.md"><strong>propiedad DescriptionURL</strong></a> del <a href="signedcode.md"><strong>objeto SignedCode</strong></a> no se ha inicializado.<br/></td>
<td>0x80880363 // v2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></td>
<td>El <em>parámetro URL</em> del método <a href="signedcode-timestamp.md"><strong>SignedCode.Timestamp</strong></a> no es válido.<br/></td>
<td>0x80880364 // v2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_HASH_NO_DATA</strong></td>
<td>El <a href="hasheddata.md"><strong>objeto HashedData</strong></a> no contiene ningún dato.<br/></td>
<td>0x80880370 // v2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></td>
<td>El tipo de conversión no es válido.<br/></td>
<td>0x80880380 // v2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_NOT_SUPPORTED</strong></td>
<td>La operación solicitada no se admite en la plataforma actual. <br/></td>
<td>0x80880900</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_UI_DISABLED</strong></td>
<td>Al firmar, no <a href="signer-certificate.md"><strong>se ha</strong></a> establecido la propiedad Certificate del objeto <a href="signer.md"><strong>Signer,</strong></a> pero se ha deshabilitado la solicitud del certificado de usuario. <br/> Habilite el símbolo del sistema estableciendo la propiedad <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> del objeto <a href="settings.md"><strong>Configuración</strong></a> o establezca la propiedad <a href="signer-certificate.md"><strong>Certificate</strong></a> del <a href="signer.md"><strong>objeto Signer.</strong></a><br/></td>
<td>0x80880901</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CANCELLED</strong></td>
<td>El usuario canceló la operación. <br/> Esto sucede cuando se solicita al usuario permiso para llevar a cabo una operación determinada, como el acceso a la clave privada, y el usuario cancela la operación.<br/></td>
<td>0x80880902</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_NOT_ALLOWED</strong></td>
<td>No se permite la operación intentada.<br/> Por ejemplo, no se permite cambiar <a href="extendedproperty-propid.md"><strong>la propiedad PropID</strong></a> de un <a href="extendedproperty.md"><strong>objeto ExtendedProperty</strong></a> si el objeto está asociado a un certificado.<br/></td>
<td>0x80880903 // v2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></td>
<td>CAPICOM se ha quedo sin un recurso.<br/></td>
<td>0x80880904 // v2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INTERNAL</strong></td>
<td>Se ha producido un error interno. <br/> Póngase en contacto con el soporte técnico de Microsoft para obtener ayuda.<br/></td>
<td>0x80880911</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_UNKNOWN</strong></td>
<td>Se ha producido un error desconocido. <br/> Recopile toda la información posible y póngase en contacto con su proveedor.<br/></td>
<td>0x80880999</td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




