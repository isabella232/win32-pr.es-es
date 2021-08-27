---
description: Crea un certificado X.509, firmado por la clave raíz de prueba u otra clave especificada, que enlaza el nombre a la parte pública del par de claves. El certificado se guarda en un archivo, en un almacén de certificados del sistema o en ambos.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff9fb79b5db5a6a71eee981166742b4e1680184
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471931"
---
# <a name="makecert"></a>MakeCert

> [!Note]  
> Makecert está en desuso. Para crear certificados autofirmados, use el cmdlet [New-SelfSignedCertificate de](/powershell/module/pki/new-selfsignedcertificate)PowerShell.

 

La herramienta MakeCert crea un certificado [*X.509,*](../secgloss/x-gly.md) firmado por la clave raíz de prueba u otra clave especificada, que enlaza su nombre a la parte pública del par de claves. El certificado se guarda en un archivo, en un almacén de certificados del sistema o en ambos. La herramienta se instala en la carpeta Bin de la ruta de instalación de \\ Microsoft Windows Software Development Kit (SDK).

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




| Opción básica | Descripción | 
|--------------|-------------|
| <strong>-a</strong> <strong></strong> <em>Algoritmo</em> | <a href="/windows/desktop/SecGloss/h-gly"><em>Algoritmo hash.</em></a> Debe establecerse en <strong>SHA-1</strong> o <strong>MD5</strong> (valor predeterminado). Para obtener información sobre MD5, vea <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>. | 
| <strong>-b</strong> <strong></strong> <em>DateStart</em> | Fecha en que el certificado se convierte primero en válido. El valor predeterminado es cuando se crea el certificado. El formato de <em>DateStart</em> es mm/dd/yyyy. | 
| <strong>-cy</strong> <strong></strong> <em>CertificateTypes</em> | Tipo de certificado. <em>CertificateTypes puede</em> ser <strong>end para</strong> la entidad final o entidad <strong>para</strong> la entidad <a href="/windows/desktop/SecGloss/c-gly"><em>de certificación</em></a>. | 
| <strong>-e</strong> <strong></strong> <em>DateEnd</em> | Fecha en que finaliza el período de validez. El valor predeterminado es el año 2039. | 
| <strong>-eku</strong> <strong></strong> <em>OID1,</em><strong></strong><em>OID2</em> ... | Inserta una lista de uno o <a href="/windows/desktop/SecGloss/e-gly"><em></em></a>varios identificadores de objeto de uso mejorados de clave separados por<a href="/windows/desktop/SecGloss/o-gly"><em>comas</em></a> en el certificado. Por ejemplo, <strong>-eku 1.3.6.1.5.5.7.3.2</strong> inserta el OID de autenticación de cliente. Para obtener definiciones de ID permitidos, consulte el archivo Wincrypt.h en CryptoAPI 2.0. | 
| <strong>-h</strong> <strong></strong> <em>NumChildren</em> | Alto máximo del árbol debajo de este certificado. | 
| <strong>-l</strong> <strong></strong> <em>PolicyLink</em> | Vínculo a la información de la directiva de la agencia SPC (por ejemplo, una dirección URL). | 
| <strong>-m</strong> <strong></strong> <em>nMonths</em> | Duración del período de validez. | 
| <strong>-n</strong><strong>"</strong><em>Name</em><strong>"</strong> | Nombre del certificado del publicador. Este nombre debe cumplir el <a href="/windows/desktop/SecGloss/x-gly"><em>estándar X.500.</em></a> El método más sencillo es usar el formato "CN=<em>MyName".</em> Por ejemplo: <strong>-n "CN=Test".</strong> | 
| <strong>-nscp</strong> | Se debe incluir la extensión de autenticación de cliente de Netscape. | 
| <strong>-pe</strong> | Marca la clave privada como exportable. | 
| <strong>-r</strong> | Crea un certificado autofirmado. | 
| <strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em> | Nombre de archivo de certificado con la clave pública de asunto existente que se va a usar. | 
| <strong>-sk</strong> <strong></strong> <em>SubjectKey</em> | Ubicación del contenedor de claves del sujeto que contiene la <a href="/windows/desktop/SecGloss/p-gly"><em>clave privada</em></a>. Si no existe un contenedor de claves, se creará uno. Si no se <strong>usa la opción -sk</strong> <strong>o -sv,</strong> se crea un contenedor de claves predeterminado y se usa de forma predeterminada. | 
| <strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em> | Especificación de clave del sujeto. <em>SubjectKeySpec debe</em> ser uno de los tres valores posibles:<br /><ul><li><strong>Firma</strong> (especificación AT_SIGNATURE clave)</li><li><strong>Exchange</strong> (especificación AT_KEYEXCHANGE clave)</li><li>Un entero, como <strong>3</strong></li></ul>Para obtener más información, vea la nota que sigue a esta tabla.<br /> | 
| <strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em> | Proveedor cryptoAPI para el asunto. El valor predeterminado es el proveedor del usuario. Para obtener información sobre los proveedores de CryptoAPI, consulte la documentación CryptoAPI 2.0 cryptoapi. | 
| <strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em> | Ubicación del Registro del almacén de certificados del sujeto. <em>SubjectCertStoreLocation</em> debe ser <strong>LocalMachine</strong> (clave del Registro HKEY_LOCAL_MACHINE) o <strong>CurrentUser</strong> (clave del Registro HKEY_CURRENT_USER). <strong>CurrentUser</strong> es el valor predeterminado. | 
| <strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em> | Nombre del almacén de certificados del sujeto donde se almacenará el certificado generado. | 
| <strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em> | Nombre del archivo .pvk del sujeto. Si no se <strong>usa la opción -sk</strong> <strong>o -sv,</strong> se crea un contenedor de claves predeterminado y se usa de forma predeterminada. | 
| <strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em> | Tipo de proveedor cryptoAPI para el asunto. El valor predeterminado <a href="/windows/desktop/SecGloss/p-gly"><em>es PROV_RSA_FULL</em></a>. Para obtener información sobre los tipos de proveedor cryptoAPI, consulte la documentación CryptoAPI 2.0 cryptoapi. | 
| <strong>-#</strong><strong></strong><em>SerialNumber</em> | Número de serie del certificado. El valor máximo es 2^31. El valor predeterminado es un valor generado por la herramienta que se garantiza que es único. | 
| <strong>-$</strong><strong></strong><em>CertificateAuthority</em> | Tipo de <a href="/windows/desktop/SecGloss/c-gly"><em>entidad de certificación</em></a>. <em>CertificateAuthority</em> debe establecerse en <strong>comercial</strong> (para que los publicadores de software comercial utilicen los certificados) o <strong>individual</strong> (para que los publicadores de software individuales los utilicen). | 
| <strong>-?</strong> | Muestra las opciones básicas. | 
| <strong>-!</strong> | Muestra las opciones extendidas. | 




 

> [!Note]  
> Si la **opción -sky** key specification se usa en Internet Explorer versión 4.0 o posterior, [](../secgloss/p-gly.md) la especificación debe coincidir con la especificación de clave indicada por el archivo de clave privada o el contenedor de claves [*privadas*](../secgloss/k-gly.md). Si no se usa la opción de especificación de clave, se usará la especificación de clave indicada por el archivo de clave privada o el contenedor de claves privadas. Si hay más de una especificación de clave en el contenedor de claves, MakeCert intentará usar primero la especificación de clave AT \_ SIGNATURE. Si se produce un error, MakeCert intentará usar AT \_ KEYEXCHANGE. Dado que la mayoría de los usuarios tienen una clave AT SIGNATURE o una clave AT KEYEXCHANGE, no es necesario usar esta opción en la mayoría \_ \_ de los casos.

 

Las siguientes opciones son solo para los [*archivos de certificado Publisher software*](../secgloss/s-gly.md) (SPC) y la tecnología de clave privada.




| Opción de clave privada y SPC | Descripción | 
|----------------------------|-------------|
| <strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em> | Ubicación del certificado del emisor. | 
| <strong>-ik</strong> <strong></strong> <em>IssuerKey</em> | Ubicación del contenedor de claves del emisor. El valor predeterminado es la clave raíz de prueba. | 
| <strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em> | Especificación de clave del emisor, que debe ser uno de los tres valores posibles:<br /><ul><li><strong>Firma</strong> (especificación AT_SIGNATURE clave)</li><li><strong>Exchange</strong> (especificación AT_KEYEXCHANGE clave)</li><li>Entero, como <strong>3</strong></li></ul>Para obtener más información, vea la nota que sigue a esta tabla.<br /> | 
| <strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em> | Proveedor cryptoAPI para el emisor. El valor predeterminado es el proveedor del usuario. Para obtener información sobre los proveedores de CryptoAPI, consulte la documentación CryptoAPI 2.0 cryptoAPI. | 
| <strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em> | Archivo de clave privada del emisor. El valor predeterminado es la raíz de prueba. | 
| <strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em> | Tipo de proveedor CryptoAPI para el emisor. El valor predeterminado <a href="/windows/desktop/SecGloss/p-gly"><em>es PROV_RSA_FULL</em></a>. Para obtener información sobre los tipos de proveedor cryptoAPI, consulte la documentación CryptoAPI 2.0 datos. | 




 

> [!Note]  
> Si la **opción -iky** key specification se usa en Internet Explorer 4.0 o posterior, [](../secgloss/p-gly.md) la especificación debe coincidir con la especificación de clave indicada por el archivo de clave privada o el contenedor de [*claves privadas*](../secgloss/k-gly.md). Si no se usa la opción de especificación de clave, se usará la especificación de clave indicada por el archivo de clave privada o el contenedor de claves privadas. Si hay más de una especificación de clave en el contenedor de claves, MakeCert intentará usar primero la especificación de clave AT \_ SIGNATURE. Si se produce un error, MakeCert intentará usar AT \_ KEYEXCHANGE. Dado que la mayoría de los usuarios tienen una clave AT SIGNATURE o una clave AT KEYEXCHANGE, no es necesario usar esta opción en la mayoría \_ \_ de los casos.

 

Las siguientes opciones son solo para [*la tecnología de almacén de*](../secgloss/c-gly.md) certificados.



| Opción almacén de certificados          | Descripción                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-ic** *IssuerCertFile*          | Archivo que contiene el certificado del emisor. MakeCert buscará en el almacén de certificados un certificado con una coincidencia exacta.                                                                                                                                                                                                        |
| **-in** *IssuerNameString*        | Nombre común del certificado del emisor. MakeCert buscará en el almacén de certificados un certificado cuyo nombre común incluya *IssuerNameString.*                                                                                                                                                                                  |
| **-ir** *IssuerCertStoreLocation* | Ubicación del Registro del almacén de certificados del emisor. *IssuerCertStoreLocation* debe ser **LocalMachine** (clave del Registro HKEY LOCAL MACHINE) o \_ \_ **CurrentUser** (clave del Registro HKEY \_ CURRENT \_ USER). **CurrentUser** es el valor predeterminado.                                                                                                |
| **-is** *IssuerCertStoreName*     | Almacén de certificados del emisor que incluye el certificado del emisor y su información de clave privada asociada. Si hay más de un certificado en el almacén, el usuario debe identificarlo de forma única mediante la **opción -ic** **o -in.** Si el certificado del almacén de certificados no se identifica de forma única, se producirá un error en MakeCert. |



 

 

 
