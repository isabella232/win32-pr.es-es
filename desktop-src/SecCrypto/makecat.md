---
description: Herramienta CryptoAPI que crea un archivo de catálogo.
ms.assetid: 233b3644-f2a5-4166-bac0-30bf2f54e957
title: MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6c2c3cb1d7df5a9f717143465d48d4c066466d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908087"
---
# <a name="makecat"></a>MakeCat

La herramienta MakeCat es una herramienta CryptoAPI que crea un archivo de catálogo. MakeCat está disponible como parte del kit de desarrollo de software (SDK) de Microsoft Windows para Windows 7 y .NET Framework 4,0 y está instalado, de forma predeterminada, en la \\ carpeta bin de la ruta de instalación de SDK.

La herramienta MakeCat usa la siguiente sintaxis de comando:

**MakeCat** \[ **-n** \| **-r** \| **-v** \] *Nombre de archivo*

## <a name="parameters"></a>Parámetros



| Parámetro             | Descripción                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-n**<br/>     | No se detiene en un error recuperable.<br/>                                                                                                                           |
| **-r**<br/>     | Fuerza a MakeCat a finalizar si encuentra errores recuperables. En concreto, terminará al procesar las entradas de la sección de archivos de catálogo de un archivo. CDF.<br/> |
| **-v**<br/>     | Detallado. Muestra todos los mensajes de progreso y de error.<br/>                                                                                                            |
| *FileName*<br/> | Nombre del archivo. CDF que se va a analizar. Para obtener la estructura y el contenido necesarios, vea la sección Comentarios.<br/>                                                                         |



 

## <a name="remarks"></a>Observaciones

El archivo. CDF debe compilarse con las siguientes especificaciones.

``` syntax
[CatalogHeader]
Name=Name              
ResultDir=ResultDir   
PublicVersion=[|1]
CatalogVersion = [|1|2]
HashAlgorithms=[|SHA1|SHA256]
PageHashes=[true|false]
EncodingType=Encodingtype 
CATATTR1={type}:{oid}:{value} (optional)
CATATTR2={type}:{oid}:{value} (optional)

[CatalogFiles]
{reference tag}=file path and name
{reference tag}ALTSIPID={guid} (optional)
{reference tag}ATTR1={type}:{oid}:{value} (optional)
{reference tag}ATTR2={type}:{oid}:{value} (optional)
<HASH>kernel32.dll=kernel32.dll
<HASH>ntdll.dll=ntdll.dll
```

> [!Note]  
> La última entrada del archivo. CDF siempre debe tener un carácter de nueva línea explícito al final de la línea.

 

La \[ \] sección CatalogHeader define información sobre todo el archivo de catálogo.



| Opción                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre<br/>           | Nombre del archivo de catálogo, incluida su extensión.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ResultDir<br/>      | Directorio donde se colocará el archivo. cat creado. Si no se indica, se usa el directorio actual predeterminado. Si el directorio no existe, se crea.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PublicVersion<br/>  | Esta opción no se admite. <br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Versión del catálogo. Si se deja en blanco, se usa el valor predeterminado, 1.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| CatalogVersion<br/> | Versión del catálogo. Si la versión no está presente o se establece en 1, "0x100" se pasa al parámetro *dwPublicVersion* de la función [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) y se crea un archivo de catálogo de la versión 1. La opción HashAlgorithms debe estar vacía o contener SHA1.<br/> Si la versión se establece en 2, se pasa "0x200" al parámetro *dwPublicVersion* de la función [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) y se crea un archivo de catálogo de la versión 2. La opción HashAlgorithms debe contener SHA256.<br/> Si esta opción está presente pero contiene cualquier valor distinto de 1 o 2, se producirá un error en la herramienta MakeCat.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta opción no se admite.<br/> <br/> |
| HashAlgorithms<br/> | Nombre del algoritmo hash usado. Para obtener más información, vea la opción CatalogVersion.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta opción no se admite.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| PageHashes<br/>     | Especifica si se van a aplicar algoritmos hash a los archivos enumerados en la <HASH> opción de la \[ \] sección CatalogFiles<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta opción no se admite.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| EncodingType<br/>   | Tipo de codificación de mensajes usada. Si se deja en blanco, el valor predeterminado de EncodingType es PKCS 7 codificación ASN de codificación de ASN \_ \_ \_ \| \_ \_ , 0x00010001. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

\[En la \] sección CatalogFiles se define cada miembro del archivo de catálogo con archivos de varios tipos y atributos de varios tipos en grupos independientes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opción</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>etiqueta de referencia<br/></td>
<td>Referencia de texto al archivo. Puede incluir cualquier carácter de texto ASCII excepto el signo igual (=). El sistema debe poder reproducir esta etiqueta después de la instalación. <br/> Use <HASH> como prefijo del nombre de archivo. Esto da como resultado que la etiqueta sea el hash del archivo en forma de cadena ASCII. <br/></td>
</tr>
<tr class="even">
<td>Ruta de acceso y nombre de archivo<br/></td>
<td>El nombre de archivo, incluida la extensión que se va a analizar y la ruta de acceso relativa al archivo. Cualquier tipo de archivo que se pueda firmar con SignTool puede agregarse a un catálogo. Por ejemplo, los nombres de archivo con las siguientes extensiones, entre otros, se pueden agregar a un catálogo:. exe,. cab,. cat,. ocx,. dll y. STL.<br/></td>
</tr>
<tr class="odd">
<td>ALTSIPID<br/></td>
<td>GUID de SIP que se va a utilizar para el hash en lugar del SIP estándar basado en el tipo de archivo. Esta entrada es opcional. Si se omite esta entrada, se aplicará un algoritmo hash al miembro mediante el SIP predeterminado. Si no se encuentra ningún SIP instalado de forma predeterminada, se usará el SIP plano.<br/></td>
</tr>
<tr class="even">
<td>guid<br/></td>
<td>Representación de texto de un GUID.<br/></td>
</tr>
<tr class="odd">
<td>ATTRx<br/></td>
<td>Opcional. Atributo o instrucción sobre el archivo o el contenido. Puede haber cualquier número de atributos, incluido ninguno.<br/></td>
</tr>
<tr class="even">
<td>type<br/></td>
<td>Define el tipo de atributo que se va a agregar en el formato 0x00000000 (texto). Esta opción puede ser<strong>una combinación OR bit a bit</strong> de cero o más de los valores siguientes:<br/>
<ul>
<li>atributo autenticado de 0x10000000 (firmado, incluido en el hash).</li>
<li>0x20000000 atributo no autenticado (sin signo, no incluido en el hash, no comprobable).</li>
<li>el atributo 0x01000000 no se replicará en las entradas SHA1 de un catálogo CatalogVersion 2.</li>
<li>el atributo 0x00010000 se representa en texto sin formato. No se realizará ninguna conversión.</li>
<li>el atributo 0x00020000 se representa en la codificación de base 64. Se utiliza para representar datos binarios.</li>
<li>0x00000001 Attribute es un par nombre-valor. Use la opción OID como nombre. Este atributo es lento; por lo tanto, use esta opción con moderación.</li>
<li>un <a href="/windows/desktop/SecGloss/o-gly"><em>identificador de objeto</em></a> (OID) hace referencia a un atributo 0x00000002.</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>oid<br/></td>
<td>Representación de texto de la clave de referencia del atributo. Es un OID en forma de cadena de texto en notación cuádruple con puntos (por ejemplo, a.b.c. d) o un nombre de texto.<br/></td>
</tr>
<tr class="even">
<td>value<br/></td>
<td>Representación de texto del valor del atributo. El tipo de representación de texto utilizado depende del valor de la opción Type. Los caracteres EOL determinan la longitud.<br/></td>
</tr>
<tr class="odd">
<td><HASH><br/></td>
<td>Aplica un algoritmo hash al archivo especificado.<br/></td>
</tr>
</tbody>
</table>



 

El archivo de catálogo generado no tiene signo. Si se va a firmar antes de transmitir, se firma con [SignTool](signtool.md).

 

 
