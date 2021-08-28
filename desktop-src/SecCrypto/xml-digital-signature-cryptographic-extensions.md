---
description: CryptXML permite a los desarrolladores ampliar los algoritmos criptográficos admitidos de forma nativa mediante el registro de un archivo DLL de extensión criptográfica de todo el sistema.
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: Extensiones criptográficas de firma digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bf0f2d99b34d59e9817f8568b03be20e72dda1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474941"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a>Extensiones criptográficas de firma digital XML

CryptXML permite a los desarrolladores ampliar los algoritmos criptográficos admitidos de forma nativa mediante el registro de un archivo DLL de extensión criptográfica de todo el sistema. Los archivos DLL de extensión amplían los algoritmos admitidos por los elementos XML **SignatureMethod** **y DigestMethod.** Los archivos DLL de extensión pueden admitir algoritmos que codifican parámetros adicionales en la firma digital XML.

Todos los archivos DLL de extensiones deben admitir la función [**CryptXmlDllGetInterface,**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) que devuelve un puntero a una estructura [**CRYPT \_ XML CRYPTOGRAPHIC \_ \_ INTERFACE.**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) Esta estructura proporciona punteros de función a funciones de extensión criptográficas implementadas. Las funciones admitidas dependen del tipo de algoritmo criptográfico admitido y de si el algoritmo debe codificar parámetros en la firma digital XML.

Las funciones de extensiones criptográficas incluyen los siguientes punteros de función:

<dl> <dt>

<span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Funciones necesarias
</dt> <dd>

-   [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [**CryptXmlDllGetAlgorithmInfo**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Funciones del método digest
</dt> <dd>

-   [**CryptXmlDllCloseDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [**CryptXmlDllCreateDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [**CryptXmlDllDigestData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [**CryptXmlDllFinalizeDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Funciones del método signature
</dt> <dd>

-   [**CryptXmlDllSignData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [**CryptXmlDllVerifySignature**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [**CryptXmlDllCreateKey**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [**CryptXmlDllEncodeKeyValue**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>Para algoritmos con parámetros codificados predeterminados
</dt> <dd>

-   [**CryptXmlDllEncodeAlgorithm**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

Los archivos DLL de extensión criptográfica se registran en todo el sistema. Se requieren privilegios de administrador para registrar un archivo DLL de extensión criptográfica.

Todas las extensiones criptográficas CryptXML se registran mediante el valor uri establecido en **SignatureMethod** o el campo de atributo algorithm del **elemento DigestMethod.**

Las rutas de acceso del Registro para los archivos DLL de extensión son las siguientes:

<dl> <dt>

<span id="32-bit"></span><span id="32-BIT"></span>32 bits
</dt> <dd>

**HKEY \_ SOFTWARE \_ DE MÁQUINA LOCAL** \\  \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{uri}*

</dd> <dt>

<span id="64-bit"></span><span id="64-BIT"></span>64 bits
</dt> <dd>

**HKEY \_ SOFTWARE \_ DE MÁQUINA LOCAL** \\  \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{uri}*

**HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **WOW6432NODE** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{uri}*

</dd> </dl>

Cada clave contiene la siguiente configuración.




| Nombre | Tipo | Datos | 
|------|------|------|
| Archivo DLL<br /> | Cadena expandible<br /> | Necesario.<br />Ruta de acceso absoluta al archivo DLL del proveedor criptográfico XML.<blockquote><p><b>Nota: </b> Se recomienda que los archivos DLL de extensión criptográfica se encuentran en directorios en los que solo pueden escribirse las aplicaciones con privilegios administrativos.</p><p><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> se usa para cargar el archivo DLL de extensión criptográfica.<br /></p></blockquote><br /> | 
| Nombre<br /> | <strong>String</strong> | Opcional.<br /> Nombre para mostrar asociado a este URI.<br /> | 
| GroupId<br /> | <strong>DWORD</strong> | Necesario.<br /> Identificador de grupo asociado a este algoritmo criptográfico. Entre los valores posibles se incluyen los<strong>siguientes: CRYPT_XML_GROUP_ID_HASH</strong> \<strong> </strong> = 1<br /><strong></strong> \<strong> CRYPT_XML_GROUP_ID_SIGN </strong> = 2<br /> | 
| CNGAlgid<br /> | <strong>String</strong> | Necesario.<br /> Nombre del algoritmo CNG que se va a pasar a las funciones BCrypt o NCrypt.<br /> | 
| CNGExtraAlgid<br /> | <strong>String</strong> | Opcional.<br /> Una cadena de algoritmo adicional, que no sea la cadena del miembro CNGAlgid, que se puede pasar a las funciones de CNG.<br /> Para los algoritmos de firma (CRYPT_XML_GROUP_ID_SIGN), este miembro es la cadena de algoritmo de clave pública que se va a pasar a las funciones CNG.<br /> Para los demás valores de GroupId, establezca el miembro <strong>pwszCNGExtraAlgid</strong> en la cadena vacía, L"". <br /> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>


</dt> <dt>

[Algoritmos criptográficos de firma digital XML](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 
