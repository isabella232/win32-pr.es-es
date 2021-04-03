---
description: CryptXML permite a los desarrolladores ampliar los algoritmos criptográficos admitidos de forma nativa mediante el registro de un archivo DLL de extensión criptográfica en todo el sistema.
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: Extensiones criptográficas de firmas digitales XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8747521913ca1d551f1a2d4fd5b1c79d80065832
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "103913946"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a>Extensiones criptográficas de firmas digitales XML

CryptXML permite a los desarrolladores ampliar los algoritmos criptográficos admitidos de forma nativa mediante el registro de un archivo DLL de extensión criptográfica en todo el sistema. Los archivos dll de extensión amplían los algoritmos que admiten los elementos XML **SignatureMethod** y **DigestMethod** . Los archivos dll de extensión pueden admitir algoritmos que codifican parámetros adicionales en la firma digital XML.

Todas las dll de extensiones deben admitir la función [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) , que devuelve un puntero a una estructura de [**\_ \_ \_ interfaz criptográfica de XML de cifrado**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) . Esta estructura proporciona punteros de función a las funciones de extensión criptográfica implementadas. Las funciones admitidas dependen del tipo de algoritmo criptográfico compatible y de si el algoritmo debe codificar los parámetros en la firma digital XML.

Las funciones de extensiones criptográficas incluyen los siguientes punteros de función:

<dl> <dt>

<span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Funciones requeridas
</dt> <dd>

-   [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [**CryptXmlDllGetAlgorithmInfo**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Funciones de método de síntesis
</dt> <dd>

-   [**CryptXmlDllCloseDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [**CryptXmlDllCreateDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [**CryptXmlDllDigestData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [**CryptXmlDllFinalizeDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Funciones del método Signature
</dt> <dd>

-   [**CryptXmlDllSignData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [**CryptXmlDllVerifySignature**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [**CryptXmlDllCreateKey**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [**CryptXmlDllEncodeKeyValue**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>Para los algoritmos con parámetros codificados predeterminados
</dt> <dd>

-   [**CryptXmlDllEncodeAlgorithm**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

Los archivos dll de extensión criptográfica se registran en todo el sistema. Se requieren privilegios de administrador para registrar un archivo DLL de extensión criptográfica.

Todas las extensiones criptográficas de CryptXML se registran mediante el valor de URI establecido en el campo **SignatureMethod** o el atributo Algorithm del elemento **DigestMethod** .

Las rutas de acceso del registro para los archivos dll de extensión son las siguientes:

<dl> <dt>

<span id="32-bit"></span><span id="32-BIT"></span>32 bits
</dt> <dd>

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*

</dd> <dt>

<span id="64-bit"></span><span id="64-BIT"></span>64 bits
</dt> <dd>

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **WOW6432NODE** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*

</dd> </dl>

Cada clave contiene la siguiente configuración.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre</th>
<th>Tipo</th>
<th>Datos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Archivo DLL<br/></td>
<td>Cadena expansible<br/></td>
<td>Obligatorio.<br/>Ruta de acceso absoluta al archivo DLL del proveedor de servicios criptográficos XML.
<blockquote>
<p><b>Nota: </b> Se recomienda que los archivos dll de extensión criptográfica se encuentren en directorios en los que solo puedan escribir las aplicaciones con privilegios administrativos.</p>
<p><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> se usa para cargar el archivo dll de extensión criptográfica.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Nombre<br/></td>
<td><strong>String</strong></td>
<td>Opcional.<br/> El nombre para mostrar asociado con este URI.<br/></td>
</tr>
<tr class="odd">
<td>GroupId<br/></td>
<td><strong>DWORD</strong></td>
<td>Obligatorio.<br/> Identificador de grupo asociado a este algoritmo criptográfico. Entre los valores posibles se incluyen los siguientes:<strong>CRYPT_XML_GROUP_ID_HASH</strong> \ <strong></strong> = 1<br/><strong></strong> \ CRYPT_XML_GROUP_ID_SIGN <strong></strong> = 2<br/></td>
</tr>
<tr class="even">
<td>CNGAlgid<br/></td>
<td><strong>String</strong></td>
<td>Obligatorio.<br/> Nombre del algoritmo CNG que se va a pasar a las funciones BCrypt o NCrypt.<br/></td>
</tr>
<tr class="odd">
<td>CNGExtraAlgid<br/></td>
<td><strong>String</strong></td>
<td>Opcional.<br/> Una cadena de algoritmo adicional, que no sea la cadena en el miembro CNGAlgid, que se puede pasar a las funciones de CNG.<br/> Para los algoritmos de firma (CRYPT_XML_GROUP_ID_SIGN), este miembro es la cadena de algoritmo de clave pública que se va a pasar a las funciones de CNG.<br/> Para los demás valores de GroupId, establezca el miembro <strong>pwszCNGExtraAlgid</strong> en la cadena vacía, L &quot; &quot; . <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>


</dt> <dt>

[Algoritmos criptográficos de firma digital XML](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 
