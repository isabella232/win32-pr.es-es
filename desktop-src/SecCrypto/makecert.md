---
description: Crea un certificado X.509, firmado por la clave raíz de prueba u otra clave especificada, que enlaza el nombre a la parte pública del par de claves. El certificado se guarda en un archivo, en un almacén de certificados del sistema o en ambos.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd9f15f942fb6dd7c4c831cb33552b6f59ec2cd6cf9cac9654386d6adc27649
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425745"
---
# <a name="makecert"></a>MakeCert

> [!Note]  
> Makecert está en desuso. Para crear certificados autofirmados, use el cmdlet [New-SelfSignedCertificate de](/powershell/module/pki/new-selfsignedcertificate)PowerShell.

 

La herramienta MakeCert crea un certificado [*X.509,*](../secgloss/x-gly.md) firmado por la clave raíz de prueba u otra clave especificada, que enlaza el nombre a la parte pública del par de claves. El certificado se guarda en un archivo, en un almacén de certificados del sistema o en ambos. La herramienta se instala en la carpeta Bin de la ruta de instalación de \\ Microsoft Windows Software Development Kit (SDK).

La herramienta MakeCert usa la siguiente sintaxis de comandos:

**MakeCert** \[ *BasicOptions* \| *ExtendedOptions* \] *OutputFile*

*OutputFile* es el nombre del archivo donde se escribirá el certificado. Puede omitir *OutputFile si* el certificado no se va a escribir en un archivo.

## <a name="options"></a>Opciones

MakeCert incluye opciones básicas y extendidas. Las opciones básicas son las que más se utilizan para crear un certificado. Las opciones ampliadas proporcionan más flexibilidad.

Las opciones de MakeCert también se dividen en tres grupos funcionales:

-   Opciones básicas específicas de la tecnología de almacén de certificados.
-   Opciones extendidas específicas de la tecnología de clave privada y archivo SPC.
-   Opciones extendidas aplicables a la tecnología de archivo SPC, clave privada y almacén de certificados.

Las opciones que se muestran en las tablas siguientes solo se pueden usar Internet Explorer 4.0 o posterior.



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
<td><strong>-a</strong> <strong></strong> <em>Algoritmo</em></td>
<td><a href="/windows/desktop/SecGloss/h-gly"><em>Algoritmo hash.</em></a> Debe establecerse en <strong>SHA-1</strong> o <strong>MD5</strong> (valor predeterminado). Para obtener información sobre MD5, vea <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</td>
</tr>
<tr class="even">
<td><strong>-b</strong> <strong></strong> <em>DateStart</em></td>
<td>Fecha en que el certificado se convierte primero en válido. El valor predeterminado es cuando se crea el certificado. El formato de <em>DateStart</em> es mm/dd/yyyy.</td>
</tr>
<tr class="odd">
<td><strong>-cy</strong> <strong></strong> <em>CertificateTypes</em></td>
<td>Tipo de certificado. <em>CertificateTypes puede</em> ser <strong>end para</strong> la entidad final o entidad <strong>para</strong> la entidad <a href="/windows/desktop/SecGloss/c-gly"><em>de certificación</em></a>.</td>
</tr>
<tr class="even">
<td><strong>-e</strong> <strong></strong> <em>DateEnd</em></td>
<td>Fecha en que finaliza el período de validez. El valor predeterminado es el año 2039.</td>
</tr>
<tr class="odd">
<td><strong>-eku</strong> <strong></strong> <em>OID1,</em><strong></strong> <em>OID2</em> ...</td>
<td>Inserta una lista de uno o <a href="/windows/desktop/SecGloss/e-gly"><em></em></a> varios identificadores de objetos de uso mejorados de clave separados por <a href="/windows/desktop/SecGloss/o-gly"><em>comas</em></a> en el certificado. Por ejemplo, <strong>-eku 1.3.6.1.5.5.7.3.2</strong> inserta el OID de autenticación de cliente. Para obtener definiciones de ID permitidos, consulte el archivo Wincrypt.h en CryptoAPI 2.0.</td>
</tr>
<tr class="even">
<td><strong>-h</strong> <strong></strong> <em>NumChildren</em></td>
<td>Alto máximo del árbol debajo de este certificado.</td>
</tr>
<tr class="odd">
<td><strong>-l</strong> <strong></strong> <em>PolicyLink</em></td>
<td>Vínculo a la información de la directiva de la agencia SPC (por ejemplo, una dirección URL).</td>
</tr>
<tr class="even">
<td><strong>-m</strong> <strong></strong> <em>nMonths</em></td>
<td>Duración del período de validez.</td>
</tr>
<tr class="odd">
<td><strong>-n</strong> <strong>&quot;</strong> <em>Nombre</em><strong>&quot;</strong></td>
<td>Nombre del certificado del publicador. Este nombre debe cumplir el <a href="/windows/desktop/SecGloss/x-gly"><em>estándar X.500.</em></a> El método más sencillo consiste en usar el &quot; formato CN=<em>MyName.</em> &quot; Por ejemplo: <strong>-n &quot; CN=Test &quot; </strong>.</td>
</tr>
<tr class="even">
<td><strong>-nscp</strong></td>
<td>Se debe incluir la extensión de autenticación de cliente de Netscape.</td>
</tr>
<tr class="odd">
<td><strong>-pe</strong></td>
<td>Marca la clave privada como exportable.</td>
</tr>
<tr class="even">
<td><strong>-r</strong></td>
<td>Crea un certificado autofirmado.</td>
</tr>
<tr class="odd">
<td><strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em></td>
<td>Nombre de archivo de certificado con la clave pública de asunto existente que se va a usar.</td>
</tr>
<tr class="even">
<td><strong>-sk</strong> <strong></strong> <em>SubjectKey</em></td>
<td>Ubicación del contenedor de claves del sujeto que contiene la <a href="/windows/desktop/SecGloss/p-gly"><em>clave privada</em></a>. Si no existe un contenedor de claves, se creará uno. Si no se <strong>usa la opción -sk</strong> <strong>o -sv,</strong> se crea un contenedor de claves predeterminado y se usa de forma predeterminada.</td>
</tr>
<tr class="odd">
<td><strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em></td>
<td>Especificación de clave del sujeto. <em>SubjectKeySpec debe</em> ser uno de los tres valores posibles:<br/>
<ul>
<li><strong>Firma</strong> (especificación AT_SIGNATURE clave)</li>
<li><strong>Exchange</strong> (especificación AT_KEYEXCHANGE clave)</li>
<li>Entero, como <strong>3</strong></li>
</ul>
Para obtener más información, vea la nota que sigue a esta tabla.<br/></td>
</tr>
<tr class="even">
<td><strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em></td>
<td>Proveedor cryptoAPI para el asunto. El valor predeterminado es el proveedor del usuario. Para obtener información sobre los proveedores de CryptoAPI, consulte la CryptoAPI 2.0 de cifrado.</td>
</tr>
<tr class="odd">
<td><strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></td>
<td>Ubicación del Registro del almacén de certificados del sujeto. <em>SubjectCertStoreLocation</em> debe ser <strong>LocalMachine</strong> (clave del Registro HKEY_LOCAL_MACHINE) o <strong>CurrentUser</strong> (clave del Registro HKEY_CURRENT_USER). <strong>CurrentUser</strong> es el valor predeterminado.</td>
</tr>
<tr class="even">
<td><strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em></td>
<td>Nombre del almacén de certificados del sujeto donde se almacenará el certificado generado.</td>
</tr>
<tr class="odd">
<td><strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em></td>
<td>Nombre del archivo .pvk del sujeto. Si no se <strong>usa la opción -sk</strong> <strong>o -sv,</strong> se crea un contenedor de claves predeterminado y se usa de forma predeterminada.</td>
</tr>
<tr class="even">
<td><strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em></td>
<td>Tipo de proveedor cryptoAPI para el asunto. El valor predeterminado <a href="/windows/desktop/SecGloss/p-gly"><em>es PROV_RSA_FULL</em></a>. Para obtener información sobre los tipos de proveedor de CryptoAPI, consulte la CryptoAPI 2.0 web.</td>
</tr>
<tr class="odd">
<td><strong>-#</strong><strong></strong> <em>SerialNumber</em></td>
<td>Número de serie del certificado. El valor máximo es 2^31. El valor predeterminado es un valor generado por la herramienta que se garantiza que es único.</td>
</tr>
<tr class="even">
<td><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></td>
<td>Tipo de <a href="/windows/desktop/SecGloss/c-gly"><em>entidad de certificación</em></a>. <em>CertificateAuthority</em> debe establecerse en <strong>comercial</strong> (para que los publicadores de software comercial utilicen los certificados) o <strong>individual</strong> (para que los publicadores de software individuales los utilicen).</td>
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
> Si la **opción -sky** key specification se usa en Internet Explorer versión 4.0 o posterior, [](../secgloss/p-gly.md) la especificación debe coincidir con la especificación de clave indicada por el archivo de clave privada o el contenedor de claves [*privadas*](../secgloss/k-gly.md). Si no se usa la opción de especificación de clave, se usará la especificación de clave indicada por el archivo de clave privada o el contenedor de claves privadas. Si hay más de una especificación de clave en el contenedor de claves, MakeCert intentará primero usar la especificación de clave AT \_ SIGNATURE. Si se produce un error, MakeCert intentará usar AT \_ KEYEXCHANGE. Dado que la mayoría de los usuarios tienen una clave AT SIGNATURE o una clave AT KEYEXCHANGE, no es necesario usar esta opción en la mayoría \_ \_ de los casos.

 

Las siguientes opciones son solo para los [*archivos de Publisher de*](../secgloss/s-gly.md) software (SPC) y la tecnología de clave privada.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>SPC y opción de clave privada</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em></td>
<td>Ubicación del certificado del emisor.</td>
</tr>
<tr class="even">
<td><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></td>
<td>Ubicación del contenedor de claves del emisor. El valor predeterminado es la clave raíz de prueba.</td>
</tr>
<tr class="odd">
<td><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></td>
<td>Especificación de clave del emisor, que debe ser uno de los tres valores posibles:<br/>
<ul>
<li><strong>Firma</strong> (AT_SIGNATURE especificación de clave)</li>
<li><strong>Exchange</strong> (especificación AT_KEYEXCHANGE clave)</li>
<li>Entero, como <strong>3</strong></li>
</ul>
Para obtener más información, vea la nota que sigue a esta tabla.<br/></td>
</tr>
<tr class="even">
<td><strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em></td>
<td>Proveedor cryptoAPI para el emisor. El valor predeterminado es el proveedor del usuario. Para obtener información sobre los proveedores de CryptoAPI, consulte la documentación CryptoAPI 2.0 cifrado.</td>
</tr>
<tr class="odd">
<td><strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em></td>
<td>Archivo de clave privada del emisor. El valor predeterminado es la raíz de la prueba.</td>
</tr>
<tr class="even">
<td><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></td>
<td>Tipo de proveedor cryptoAPI para el emisor. El valor predeterminado <a href="/windows/desktop/SecGloss/p-gly"><em>es PROV_RSA_FULL</em></a>. Para obtener información sobre los tipos de proveedor de CryptoAPI, consulte la CryptoAPI 2.0 web.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Si la **opción -iky** key specification se usa en Internet Explorer 4.0 o posterior, la [](../secgloss/p-gly.md) especificación debe coincidir con la especificación de clave indicada por el archivo de clave privada o el contenedor de claves [*privadas*](../secgloss/k-gly.md). Si no se usa la opción de especificación de clave, se usará la especificación de clave indicada por el archivo de clave privada o el contenedor de claves privadas. Si hay más de una especificación de clave en el contenedor de claves, MakeCert intentará primero usar la especificación de clave AT \_ SIGNATURE. Si se produce un error, MakeCert intentará usar AT \_ KEYEXCHANGE. Dado que la mayoría de los usuarios tienen una clave AT SIGNATURE o una clave AT KEYEXCHANGE, no es necesario usar esta opción en la mayoría \_ \_ de los casos.

 

Las siguientes opciones son solo para [*la tecnología de almacén de*](../secgloss/c-gly.md) certificados.



| Opción almacén de certificados          | Descripción                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-ic** *IssuerCertFile*          | Archivo que contiene el certificado del emisor. MakeCert buscará en el almacén de certificados un certificado con una coincidencia exacta.                                                                                                                                                                                                        |
| **-in** *IssuerNameString*        | Nombre común del certificado del emisor. MakeCert buscará en el almacén de certificados un certificado cuyo nombre común incluya *IssuerNameString.*                                                                                                                                                                                  |
| **-ir** *IssuerCertStoreLocation* | Ubicación del Registro del almacén de certificados del emisor. *IssuerCertStoreLocation* debe ser **LocalMachine** (clave del Registro HKEY LOCAL MACHINE) o \_ \_ **CurrentUser** (clave del Registro HKEY \_ CURRENT \_ USER). **CurrentUser** es el valor predeterminado.                                                                                                |
| **-is** *IssuerCertStoreName*     | Almacén de certificados del emisor que incluye el certificado del emisor y su información de clave privada asociada. Si hay más de un certificado en el almacén, el usuario debe identificarlo de forma única mediante la **opción -ic** **o -in.** Si el certificado del almacén de certificados no se identifica de forma única, se producirá un error en MakeCert. |



 

 

 
