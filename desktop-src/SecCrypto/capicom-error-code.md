---
description: Define los códigos de error devueltos por CAPICOM.
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: Enumeración CAPICOM_ERROR_CODE (CAPICOM. h)
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
ms.openlocfilehash: ccd4963c83f1ad7ce3bc686b7736ce47d699ce30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671044"
---
# <a name="capicom_error_code-enumeration"></a>\_Enumeración de códigos de error de CAPICOM \_

El tipo de enumeración del **\_ \_ código de error CAPICOM** define los códigos de error devueltos por CAPICOM.

> [!Note]  
> Los errores de Visual Basic Scripting Edition devuelven un valor de **Err. Number** mayor que cero. Para esos errores, los valores de **Err. Description** proporcionan información sobre la causa del error. Además de Visual Basic Scripting Edition errores, los errores de CAPICOM devuelven los códigos definidos por el **\_ \_ código de error de CAPICOM**.

 

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
<td>No se puede establecer la propiedad <a href="eku-oid.md"><strong>OID</strong></a> del objeto <a href="eku.md"><strong>EKU</strong></a> porque la propiedad <a href="eku-name.md"><strong>Name</strong></a> no está establecida en CAPICOM_EKU_OTHER.<br/> Establezca la propiedad <a href="eku-name.md"><strong>Name</strong></a> en CAPICOM_EKU_OTHER antes de establecer la propiedad <a href="eku-oid.md"><strong>OID</strong></a> .<br/></td>
<td>0x80880200</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></td>
<td>No se ha inicializado la propiedad <a href="eku-oid.md"><strong>OID</strong></a> del objeto <a href="eku.md"><strong>EKU</strong></a> . <br/> Establezca la propiedad <a href="eku-name.md"><strong>Name</strong></a> en algo distinto de CAPICOM_EKU_OTHER, o bien establezca la propiedad <strong>Name</strong> en CAPICOM_EKU_OTHER y la propiedad <a href="eku-oid.md"><strong>OID</strong></a> en un valor.<br/></td>
<td>0x80880201</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></td>
<td>No se ha inicializado el objeto de <a href="certificate.md"><strong>certificado</strong></a> .<br/> Normalmente, este código de error se devuelve cuando se crea una instancia de un objeto de <a href="certificate.md"><strong>certificado</strong></a> pero no se asocia a un certificado digital. Para asociar el objeto a un certificado digital, asígnelo a un objeto de <strong>certificado</strong> existente o llame al método de <a href="certificate-import.md"><strong>importación</strong></a> .<br/></td>
<td>0x80880210</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></td>
<td>El objeto de <a href="certificate.md"><strong>certificado</strong></a> no tiene una clave privada asociada.<br/> Este código de error se devuelve cuando se intenta firmar datos mediante la clave privada del firmante, pero el objeto de <a href="certificate.md"><strong>certificado</strong></a> asociado al objeto de <a href="signer.md"><strong>firmante</strong></a> no se puede usar para la operación de firma.<br/></td>
<td>0x80880211</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></td>
<td>No se ha inicializado el objeto de <a href="chain.md"><strong>cadena</strong></a> . <br/> Para inicializar el objeto de <a href="chain.md"><strong>cadena</strong></a> , llame al método de <a href="chain-build.md"><strong>compilación</strong></a> .<br/></td>
<td>0x80880220</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_STORE_NOT_OPENED</strong></td>
<td>No se ha inicializado el objeto de <a href="store.md"><strong>almacén</strong></a> . <br/> Para inicializar el objeto de <a href="store.md"><strong>almacenamiento</strong></a> , llame al método <a href="store-open.md"><strong>Open</strong></a> .<br/></td>
<td>0x80880230</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_STORE_EMPTY</strong></td>
<td>El objeto de <a href="store.md"><strong>almacén</strong></a> no contiene ningún objeto de <a href="certificate.md"><strong>certificado</strong></a> .<br/></td>
<td>0x80880231</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></td>
<td>El parámetro <em>OpenMode</em> del método <a href="store-open.md"><strong>Store. Open</strong></a> no contiene un valor válido de CAPICOM_STORE_OPEN_MODE.<br/> En la lista siguiente se muestran los valores válidos de CAPICOM_STORE_OPEN_MODE:
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
<td>El valor <em>SaveAs</em> pasado al método <a href="store-export.md"><strong>Export</strong></a> del objeto <a href="store.md"><strong>Store</strong></a> no era válido. <br/> En la lista siguiente se muestran los valores de <em>SaveAs</em> válidos:
<ul>
<li>CAPICOM_STORE_SAVE_AS_SERIALIZED</li>
<li>CAPICOM_STORE_SAVE_AS_PKCS7</li>
</ul>
<br/></td>
<td>0x80880233</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></td>
<td>No se ha inicializado la propiedad <a href="attribute-name.md"><strong>Name</strong></a> del objeto de <a href="attribute.md"><strong>atributo</strong></a> . <br/> Establezca la propiedad <a href="attribute-name.md"><strong>nombre</strong></a> .<br/></td>
<td>0x80880240</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></td>
<td>No se ha inicializado la propiedad <a href="attribute-value.md"><strong>Value</strong></a> del objeto de <a href="attribute.md"><strong>atributo</strong></a> . <br/> Establezca la propiedad <a href="attribute-value.md"><strong>Value</strong></a> .<br/></td>
<td>0x80880241</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></td>
<td>La propiedad de <a href="attribute-name.md"><strong>nombre</strong></a> del objeto de <a href="attribute.md"><strong>atributo</strong></a> no es válida. <br/> En la lista siguiente se muestran los nombres de atributo válidos:
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
<td>La propiedad <a href="attribute-value.md"><strong>Value</strong></a> del objeto de <a href="attribute.md"><strong>atributo</strong></a> no es válida porque el tipo de datos no coincide con el tipo de datos indicado por la propiedad <strong>Name</strong> . <br/> Por ejemplo, si la propiedad <a href="attribute-value.md"><strong>Name</strong></a> se establece en CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, el tipo de datos debe ser <strong>Date</strong>.<br/></td>
<td>0x80880243</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></td>
<td>No se ha inicializado el objeto de <a href="signer.md"><strong>firmante</strong></a> . <br/> Para inicializar el objeto de <a href="signer.md"><strong>firmante</strong></a> , establezca la propiedad de <a href="signer-certificate.md"><strong>certificado</strong></a> .<br/></td>
<td>0x80880250</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></td>
<td>No se encuentra el firmante en el objeto <a href="signeddata.md"><strong>SignedData</strong></a> . <br/> Normalmente, esto no ocurre con un objeto <a href="signeddata.md"><strong>SignedData</strong></a> creado por CAPICOM; sin embargo, si un producto de terceros creó el objeto <strong>SignedData</strong> , es posible que el certificado del firmante no se incluya en la estructura PKCS #7.<br/></td>
<td>0x80880251</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></td>
<td>No se encuentra un objeto de <a href="chain.md"><strong>cadena</strong></a> en el objeto de <a href="signer.md"><strong>firmante</strong></a> .<br/></td>
<td>0x80880252//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></td>
<td>Se ha intentado usar el firmante de una manera que no es válida.<br/></td>
<td>0x80880253//V2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></td>
<td>No se ha inicializado el objeto <a href="signeddata.md"><strong>SignedData</strong></a> . <br/> Para inicializar el objeto <a href="signeddata.md"><strong>SignedData</strong></a> , establezca la propiedad <a href="signeddata-content.md"><strong>Content</strong></a> o llame al método <a href="signeddata-verify.md"><strong>Verify</strong></a> .<br/></td>
<td>0x80880260</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></td>
<td>El objeto <a href="signeddata.md"><strong>SignedData</strong></a> contiene un tipo que no es válido. <br/> Normalmente, esto sucede cuando se realiza un intento de comprobar un mensaje con doble cifrado con un objeto <a href="signeddata.md"><strong>SignedData</strong></a> o viceversa.<br/></td>
<td>0x80880261</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></td>
<td>No se firmó el objeto <a href="signeddata.md"><strong>SignedData</strong></a> . <br/> Para firmar el objeto <a href="signeddata.md"><strong>SignedData</strong></a> , llame al método <a href="signeddata-sign.md"><strong>Sign</strong></a> .<br/></td>
<td>0x80880262</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INVALID_ALGORITHM</strong></td>
<td>El valor del algoritmo para la propiedad <a href="algorithm-name.md"><strong>Name</strong></a> del objeto <a href="algorithm.md"><strong>algorithm</strong></a> no es válido. <br/> En la lista siguiente se muestran los valores de algoritmo válidos para la propiedad <a href="algorithm-name.md"><strong>Name</strong></a> :
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
<td>El valor de longitud de clave para la propiedad <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> del objeto <a href="algorithm.md"><strong>algorithm</strong></a> no es válido. <br/> En la lista siguiente se muestran los valores de longitud de clave válidos para la propiedad <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> :
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
<td>No se ha inicializado el objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> . <br/> Para inicializar el objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> , establezca la propiedad <a href="envelopeddata-content.md"><strong>Content</strong></a> o llame al método <a href="envelopeddata-decrypt.md"><strong>Decrypt</strong></a> .<br/></td>
<td>0x80880280</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></td>
<td>El objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> contiene un tipo que no es válido. <br/> Normalmente, esto sucede cuando se realiza un intento de comprobar un mensaje firmado con un objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> o viceversa.<br/></td>
<td>0x80880281</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></td>
<td>No hay ningún destinatario especificado en el objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> cuando se llama al método <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> de un objeto <strong>EnvelopedData</strong> . <br/> Para agregar un destinatario, llame al método <a href="recipients-add.md"><strong>Recipients. Add</strong></a> .<br/></td>
<td>0x80880282</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></td>
<td>No se encuentra el destinatario en el objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> . <br/> Normalmente, esto no ocurre con un objeto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> creado por CAPICOM; sin embargo, si un producto de terceros creó el objeto <strong>EnvelopedData</strong> , es posible que el certificado del destinatario no se incluya en la estructura PKCS #7.<br/></td>
<td>0x80880283</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></td>
<td>El objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> no se ha inicializado. <br/> Para inicializar el objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , establezca la propiedad de <a href="encrypteddata-content.md"><strong>contenido</strong></a> o llame al método de <a href="encrypteddata-decrypt.md"><strong>descifrado</strong></a> .<br/></td>
<td>0x80880290</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></td>
<td>El objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> no es un tipo válido. <br/> Normalmente, esto significa que los datos están dañados.<br/></td>
<td>0x80880291</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></td>
<td>El secreto de un objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> no se ha inicializado. <br/> Para inicializar el secreto de un objeto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , llame al método <a href="encrypteddata-setsecret.md"><strong>SetSecret</strong></a> .<br/></td>
<td>0x80880292</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></td>
<td>No se ha inicializado el objeto <a href="privatekey.md"><strong>PrivateKey</strong></a> .<br/></td>
<td>0x80880300//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></td>
<td>No se puede exportar el objeto <a href="privatekey.md"><strong>PrivateKey</strong></a> .<br/></td>
<td>0x80880301//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></td>
<td>No se ha inicializado el objeto <a href="encodeddata.md"><strong>EncodedData</strong></a> .<br/></td>
<td>0x80880320//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></td>
<td>No se ha inicializado el objeto de <a href="extension.md"><strong>extensión</strong></a> .<br/></td>
<td>0x80880330//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></td>
<td>No se ha inicializado la propiedad <a href="extendedproperty-propid.md"><strong>PropID</strong></a> del objeto <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> .<br/></td>
<td>0x80880340//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></td>
<td>El parámetro <em>FindType</em> del método <a href="certificates-find.md"><strong>Certificates. Find</strong></a> no es un valor de la enumeración <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> .<br/></td>
<td>0x80880350//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></td>
<td>La Directiva predefinida especificada para la operación de búsqueda no es válida.<br/></td>
<td>0x80880351//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></td>
<td>No se ha inicializado el objeto <a href="signedcode.md"><strong>SignedCode</strong></a> .<br/></td>
<td>0x80880360//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></td>
<td>No se firmó el objeto <a href="signedcode.md"><strong>SignedCode</strong></a> .<br/> Para firmar el objeto <a href="signedcode.md"><strong>SignedCode</strong></a> , llame al método <a href="signedcode-sign.md"><strong>Sign</strong></a> .<br/></td>
<td>0x80880361//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></td>
<td>No se ha inicializado la propiedad <a href="signedcode-description.md"><strong>Description</strong></a> del objeto <a href="signedcode.md"><strong>SignedCode</strong></a> .<br/></td>
<td>0x80880362//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></td>
<td>No se ha inicializado la propiedad <a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a> del objeto <a href="signedcode.md"><strong>SignedCode</strong></a> .<br/></td>
<td>0x80880363//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></td>
<td>El parámetro de <em>dirección URL</em> del método <a href="signedcode-timestamp.md"><strong>SignedCode. timestamp</strong></a> no es válido.<br/></td>
<td>0x80880364//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_HASH_NO_DATA</strong></td>
<td>El objeto <a href="hasheddata.md"><strong>HashedData</strong></a> no contiene ningún dato.<br/></td>
<td>0x80880370//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></td>
<td>El tipo de conversión no es válido.<br/></td>
<td>0x80880380//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_NOT_SUPPORTED</strong></td>
<td>La operación solicitada no se admite en la plataforma actual. <br/></td>
<td>0x80880900</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_UI_DISABLED</strong></td>
<td>Al firmar, no se ha establecido la propiedad de <a href="signer-certificate.md"><strong>certificado</strong></a> del objeto de <a href="signer.md"><strong>firmante</strong></a> , pero se ha deshabilitado el símbolo del sistema para el certificado de usuario. <br/> Habilite el símbolo del sistema estableciendo la propiedad <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> del objeto de <a href="settings.md"><strong>configuración</strong></a> o establezca la propiedad de <a href="signer-certificate.md"><strong>certificado</strong></a> del objeto de <a href="signer.md"><strong>firmante</strong></a> .<br/></td>
<td>0x80880901</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CANCELLED</strong></td>
<td>El usuario ha cancelado la operación. <br/> Esto sucede cuando se solicita al usuario permiso para llevar a cabo una operación determinada, como tener acceso a la clave privada, y el usuario cancela la operación.<br/></td>
<td>0x80880902</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_NOT_ALLOWED</strong></td>
<td>La operación intentada no está permitida.<br/> Por ejemplo, no se permite cambiar la propiedad <a href="extendedproperty-propid.md"><strong>PropID</strong></a> de un objeto <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> si el objeto está asociado a un certificado.<br/></td>
<td>0x80880903//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></td>
<td>CAPICOM se ha quedado sin recursos.<br/></td>
<td>0x80880904//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INTERNAL</strong></td>
<td>Se ha producido un error interno. <br/> Póngase en contacto con el soporte técnico de Microsoft para obtener ayuda.<br/></td>
<td>0x80880911</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_UNKNOWN</strong></td>
<td>Se ha producido un error desconocido. <br/> Recopile tanta información como sea posible y póngase en contacto con su proveedor.<br/></td>
<td>0x80880999</td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




