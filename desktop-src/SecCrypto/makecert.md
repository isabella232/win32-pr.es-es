---
description: Crea un certificado X. 509, firmado por la clave raíz de prueba u otra clave especificada, que enlaza su nombre a la parte pública del par de claves. El certificado se guarda en un archivo, un almacén de certificados del sistema o ambos.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980ba379688f2dc61c44b06d66ed5255e5b2e988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686873"
---
# <a name="makecert"></a>MakeCert

> [!Note]  
> Makecert está en desuso. Para crear certificados autofirmados, use el cmdlet [de PowerShell New-SelfSignedCertificate](/powershell/module/pkiclient/new-selfsignedcertificate).

 

La herramienta MakeCert crea un certificado [*X. 509*](../secgloss/x-gly.md) , firmado por la clave raíz de prueba u otra clave especificada, que enlaza su nombre a la parte pública del par de claves. El certificado se guarda en un archivo, un almacén de certificados del sistema o ambos. La herramienta se instala en la \\ carpeta bin de la ruta de instalación del kit de desarrollo de software (SDK) de Microsoft Windows.

La herramienta MakeCert usa la siguiente sintaxis de comando:

**Makecert** \[ *BasicOptions* \| *ExtendedOptions* \] *OutputFile*

*OutputFile* es el nombre del archivo donde se escribirá el certificado. Puede omitir *OutputFile* si el certificado no se va a escribir en un archivo.

## <a name="options"></a>Opciones

MakeCert incluye opciones básicas y extendidas. Las opciones básicas son las que más se utilizan para crear un certificado. Las opciones ampliadas proporcionan más flexibilidad.

Las opciones de MakeCert también se dividen en tres grupos funcionales:

-   Opciones básicas específicas de la tecnología de almacén de certificados únicamente.
-   Opciones extendidas específicas de la tecnología de clave privada y archivos SPC únicamente.
-   Opciones extendidas aplicables a la tecnología de archivos SPC, clave privada y almacén de certificados.

Las opciones que se proporcionan en las tablas siguientes solo se pueden usar con Internet Explorer 4,0 o posterior.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opción básica</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>-a</strong> <strong></strong> <em>Algoritmo</em> de</td>
<td>Algoritmo <a href="/windows/desktop/SecGloss/h-gly"><em>hash</em></a> . Debe establecerse en <strong>SHA-1</strong> o <strong>MD5</strong> (valor predeterminado). Para obtener información acerca de MD5, consulte <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</td>
</tr>
<tr class="even">
<td><strong>-b</strong> <strong></strong> <em>DateStart</em></td>
<td>Fecha en que el certificado pasa a ser válido por primera vez. El valor predeterminado es cuando se crea el certificado. El formato de <em>DateStart</em> es mm/dd/aaaa.</td>
</tr>
<tr class="odd">
<td><strong>-CY</strong> <strong></strong> <em>CertificateTypes</em></td>
<td>Tipo de certificado. <em>CertificateTypes</em> puede ser <strong>End</strong> para la entidad de certificación o <strong>autoridad</strong> para la <a href="/windows/desktop/SecGloss/c-gly"><em>entidad de certificación</em></a>.</td>
</tr>
<tr class="even">
<td><strong>-e</strong> <strong></strong> <em>DateEnd</em></td>
<td>Fecha en que finaliza el período de validez. El valor predeterminado es el año 2039.</td>
</tr>
<tr class="odd">
<td><strong>-EKU</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> ...</td>
<td>Inserta en el certificado una lista de uno o varios <a href="/windows/desktop/SecGloss/o-gly"><em>identificadores de objeto</em></a> (OID) de <a href="/windows/desktop/SecGloss/e-gly"><em>uso de clave mejorados</em></a> por comas. Por ejemplo, <strong>-EKU 1.3.6.1.5.5.7.3.2</strong> inserta el OID de autenticación del cliente. Para obtener definiciones de OID permitidos, vea el archivo Wincrypt. h en CryptoAPI 2.0.</td>
</tr>
<tr class="even">
<td><strong>-h</strong> <strong></strong> <em>NumChildren</em></td>
<td>Alto máximo del árbol por debajo de este certificado.</td>
</tr>
<tr class="odd">
<td><strong>-l</strong> <strong></strong> <em>PolicyLink</em></td>
<td>Vínculo a la información de la Directiva de la Agencia SPC (por ejemplo, una dirección URL).</td>
</tr>
<tr class="even">
<td><strong>-m</strong> <strong></strong> <em>nMonths</em></td>
<td>Duración del período de validez.</td>
</tr>
<tr class="odd">
<td><strong>-n</strong> <strong>&quot;</strong> <em>Nombre</em> de<strong>&quot;</strong></td>
<td>Nombre del certificado del publicador. Este nombre debe cumplir el estándar <a href="/windows/desktop/SecGloss/x-gly"><em>X. 500</em></a> . El método más sencillo es usar el &quot; formato CN =<em>nombre</em> &quot; . Por ejemplo: <strong>-n &quot; CN = test &quot; </strong>.</td>
</tr>
<tr class="even">
<td><strong>-nscp</strong></td>
<td>Se debe incluir la extensión de autenticación del cliente de Netscape.</td>
</tr>
<tr class="odd">
<td><strong>-PE</strong></td>
<td>Marca la clave privada como exportable.</td>
</tr>
<tr class="even">
<td><strong>-r</strong></td>
<td>Crea un certificado autofirmado.</td>
</tr>
<tr class="odd">
<td><strong>-SC</strong> <strong></strong> <em>SubjectCertFile</em></td>
<td>Nombre del archivo de certificado con la clave pública de asunto existente que se va a usar.</td>
</tr>
<tr class="even">
<td><strong>-SK</strong> <strong></strong> <em>SubjectKey</em></td>
<td>Ubicación del contenedor de claves del sujeto que contiene la <a href="/windows/desktop/SecGloss/p-gly"><em>clave privada</em></a>. Si no existe un contenedor de claves, se creará uno. Si no se usa la opción <strong>-SK</strong> o <strong>-SV</strong> , se crea un contenedor de claves predeterminado y se utiliza de forma predeterminada.</td>
</tr>
<tr class="odd">
<td><strong>-Sky</strong> <strong></strong> <em>SubjectKeySpec</em></td>
<td>Especificación de la clave del sujeto. <em>SubjectKeySpec</em> debe ser uno de los tres valores posibles:<br/>
<ul>
<li><strong>Signature</strong> (especificación de clave de AT_SIGNATURE)</li>
<li><strong>Exchange</strong> (especificación de clave de AT_KEYEXCHANGE)</li>
<li>Un entero, como <strong>3</strong></li>
</ul>
Para obtener más información, vea la nota que sigue a esta tabla.<br/></td>
</tr>
<tr class="even">
<td><strong>-SP</strong> <strong></strong> <em>SubjectProviderName</em></td>
<td>Proveedor de CryptoAPI para el sujeto. El valor predeterminado es el proveedor del usuario. Para obtener información acerca de los proveedores de CryptoAPI, consulte la documentación de CryptoAPI 2.0.</td>
</tr>
<tr class="odd">
<td><strong>-Sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></td>
<td>Ubicación del registro del almacén de certificados del sujeto. <em>SubjectCertStoreLocation</em> debe ser <strong>LocalMachine</strong> (clave del registro HKEY_LOCAL_MACHINE) o <strong>CurrentUser</strong> (clave del registro HKEY_CURRENT_USER). <strong>CurrentUser</strong> es el valor predeterminado.</td>
</tr>
<tr class="even">
<td><strong>-SS</strong> <strong></strong> <em>SubjectCertStoreName</em></td>
<td>Nombre del almacén de certificados del sujeto en el que se almacenará el certificado generado.</td>
</tr>
<tr class="odd">
<td><strong>-SV</strong> <strong></strong> <em>SubjectKeyFile</em></td>
<td>Nombre del archivo. PVK del sujeto. Si no se usa la opción <strong>-SK</strong> o <strong>-SV</strong> , se crea un contenedor de claves predeterminado y se utiliza de forma predeterminada.</td>
</tr>
<tr class="even">
<td><strong>-SY</strong> <strong></strong> <em>nSubjectProviderType</em></td>
<td>Tipo de proveedor de CryptoAPI para el asunto. El valor predeterminado es <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Para obtener información sobre los tipos de proveedor de CryptoAPI, vea la documentación de CryptoAPI 2.0.</td>
</tr>
<tr class="odd">
<td><strong>-#</strong><strong></strong> <em>SerialNumber</em></td>
<td>Número de serie del certificado. El valor máximo es 2 ^ 31. El valor predeterminado es un valor generado por la herramienta que se garantiza que es único.</td>
</tr>
<tr class="even">
<td><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></td>
<td>Tipo de <a href="/windows/desktop/SecGloss/c-gly"><em>entidad de certificación</em></a>. <em>CertificateAuthority</em> debe establecerse en <strong>Commercial</strong> (para los certificados que vayan a usar los publicadores de software comercial) o <strong>individual</strong> (para los certificados que vayan a usar los editores de software individuales).</td>
</tr>
<tr class="odd">
<td><strong>-?</strong></td>
<td>Muestra las opciones básicas.</td>
</tr>
<tr class="even">
<td><strong>-!</strong></td>
<td>Muestra las opciones extendidas.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Si se usa la opción **-Sky** Key Specification en la versión 4,0 o posterior de Internet Explorer, la especificación debe coincidir con la especificación de clave indicada por el archivo de [*clave privada*](../secgloss/p-gly.md) o el [*contenedor de claves*](../secgloss/k-gly.md)privadas. Si no se usa la opción de especificación de clave, se usará la especificación de clave indicada por el archivo de clave privada o el contenedor de claves privadas. Si hay más de una especificación de clave en el contenedor de claves, MakeCert primero intentará usar la especificación de la \_ clave at Signature. Si se produce un error, MakeCert intentará usar en \_ KEYEXCHANGE. Dado que la mayoría de los usuarios tienen una \_ clave at Signature o una \_ clave at KEYEXCHANGE, no es necesario usar esta opción en la mayoría de los casos.

 

Las siguientes opciones son solo para los archivos de [*certificado de editor de software*](../secgloss/s-gly.md) (SPC) y la tecnología de clave privada.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>SPC y la opción de clave privada</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>-IC</strong> <strong></strong> <em>IssuerCertFile</em></td>
<td>Ubicación del certificado del emisor.</td>
</tr>
<tr class="even">
<td><strong>-IK</strong> <strong></strong> <em>IssuerKey</em></td>
<td>Ubicación del contenedor de claves del emisor. El valor predeterminado es la clave raíz de prueba.</td>
</tr>
<tr class="odd">
<td><strong>-IKY</strong> <strong></strong> <em>IssuerKeySpec</em></td>
<td>Especificación de clave del emisor, que debe ser uno de los tres valores posibles:<br/>
<ul>
<li><strong>Signature</strong> (especificación de clave de AT_SIGNATURE)</li>
<li><strong>Exchange</strong> (especificación de clave de AT_KEYEXCHANGE)</li>
<li>Un entero, como <strong>3</strong></li>
</ul>
Para obtener más información, vea la nota que sigue a esta tabla.<br/></td>
</tr>
<tr class="even">
<td><strong>-IP</strong> <strong></strong> <em>IssuerProviderName</em></td>
<td>Proveedor de CryptoAPI para el emisor. El valor predeterminado es el proveedor del usuario. Para obtener información acerca de los proveedores de CryptoAPI, consulte la documentación de CryptoAPI 2.0.</td>
</tr>
<tr class="odd">
<td><strong>-IV</strong> <strong></strong> <em>IssuerKeyFile</em></td>
<td>Archivo de clave privada del emisor. El valor predeterminado es la raíz de prueba.</td>
</tr>
<tr class="even">
<td><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></td>
<td>Tipo de proveedor de CryptoAPI para el emisor. El valor predeterminado es <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Para obtener información sobre los tipos de proveedor de CryptoAPI, vea la documentación de CryptoAPI 2.0.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Si se usa la opción **de especificación de clave-IKY** en Internet Explorer 4,0 o posterior, la especificación debe coincidir con la especificación de clave indicada por el archivo de [*clave privada*](../secgloss/p-gly.md) o el [*contenedor de claves*](../secgloss/k-gly.md)privadas. Si no se usa la opción de especificación de clave, se usará la especificación de clave indicada por el archivo de clave privada o el contenedor de claves privadas. Si hay más de una especificación de clave en el contenedor de claves, MakeCert primero intentará usar la especificación de la \_ clave at Signature. Si se produce un error, MakeCert intentará usar en \_ KEYEXCHANGE. Dado que la mayoría de los usuarios tienen una \_ clave at Signature o una \_ clave at KEYEXCHANGE, no es necesario usar esta opción en la mayoría de los casos.

 

Las siguientes opciones son solo para la tecnología de [*almacén de certificados*](../secgloss/c-gly.md) .



| Opción de almacén de certificados          | Descripción                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-** *IssuerCertFile* IC          | Archivo que contiene el certificado del emisor. MakeCert buscará un certificado con una coincidencia exacta en el almacén de certificados.                                                                                                                                                                                                        |
| **-en** *IssuerNameString*        | Nombre común del certificado del emisor. MakeCert buscará en el almacén de certificados un certificado cuyo nombre común incluya *IssuerNameString*.                                                                                                                                                                                  |
| **-IssuerCertStoreLocation de infrarrojos**  | Ubicación del registro del almacén de certificados del emisor. *IssuerCertStoreLocation* debe ser **LocalMachine** (clave del registro HKEY \_ local \_ Machine) o **CurrentUser** (clave del registro HKEY \_ Current \_ User). **CurrentUser** es el valor predeterminado.                                                                                                |
| **-es** *IssuerCertStoreName*     | Almacén de certificados del emisor que incluye el certificado del emisor y su información de clave privada asociada. Si hay más de un certificado en el almacén, el usuario debe identificarlo de forma exclusiva mediante la opción **-IC** o **-in** . Si el certificado del almacén de certificados no se identifica de forma única, se producirá un error en MakeCert. |



 

 

 
