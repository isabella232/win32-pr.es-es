---
description: La herramienta de configuración de certificados de los servicios HTTP de Microsoft Windows (WinHTTP), &\# 0034; WinHttpCertCfg.exe&\# 0034;, permite a los administradores instalar y configurar certificados de cliente en cualquier almacén de certificados al que pueda tener acceso la cuenta del administrador de aplicaciones web (IWAM) del servidor de Internet. La herramienta también elimina la necesidad de hacer nada especial en cuentas como la cuenta IWAM para obtener acceso a los certificados cuando se utiliza Active Server páginas (ASP).
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe, una herramienta de configuración de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4250cd717b9f611f4f23f17c93069760c283c97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154313"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a>WinHttpCertCfg.exe, una herramienta de configuración de certificados

La herramienta de configuración de certificados de los [servicios http de Microsoft Windows (WinHTTP)](about-winhttp.md) , "WinHttpCertCfg.exe", permite a los administradores instalar y configurar certificados de cliente en cualquier [*almacén de certificados*](glossary.md) al que pueda tener acceso la cuenta del administrador de aplicaciones web (IWAM) del servidor de Internet. La herramienta también elimina la necesidad de hacer nada especial en cuentas como la cuenta IWAM para obtener acceso a los certificados cuando se utiliza Active Server páginas (ASP).

Microsoft Management Console (MMC) permite a los administradores importar certificados de cliente en un equipo local. Sin embargo, la importación de un certificado no concede automáticamente acceso a la clave privada para otras cuentas. Esta clave privada es necesaria para la autenticación de certificados de cliente. La herramienta de configuración de certificados de los servicios HTTP de Microsoft Windows (WinHTTP) proporciona la capacidad de conceder acceso a cuentas adicionales, como la cuenta IWAM, cuando sea necesario.

-   [Uso de la herramienta de configuración de certificados](#using-the-certificate-configuration-tool)
-   [Ejemplos](#examples)

## <a name="using-the-certificate-configuration-tool"></a>Uso de la herramienta de configuración de certificados

La herramienta de configuración de certificados WinHTTP, WinHttpCertCfg.exe, está disponible como descarga en el sitio web de [herramientas del kit de recursos de Windows Server 2003](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) . En el ejemplo de código siguiente se muestran los parámetros de línea de comandos válidos para usar con esta herramienta.

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

En la tabla siguiente se enumeran los parámetros de la herramienta de configuración de.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parámetro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-?</td>
<td>Muestra datos de sintaxis.</td>
</tr>
<tr class="even">
<td>-i</td>
<td>Especifica que el certificado se va a importar desde un archivo de intercambio de información personal (PFX). Este parámetro debe ir seguido del nombre del archivo. Cuando se especifica este parámetro, &quot; &quot; &quot; &quot; también se deben especificar-a y-c.</td>
</tr>
<tr class="odd">
<td>-g</td>
<td>Especifica que se concede acceso a una clave privada. Cuando se especifica este parámetro, &quot; &quot; &quot; también se deben especificar-a,-c &quot; y &quot; -s &quot; .</td>
</tr>
<tr class="even">
<td>-r</td>
<td>Especifica que se quita el acceso para una clave privada. Cuando se especifica este parámetro, &quot; &quot; &quot; también se deben especificar-a,-c &quot; y &quot; -s &quot; .</td>
</tr>
<tr class="odd">
<td>-l</td>
<td>Especifica que se enumeran las cuentas con acceso a una clave privada. Cuando se especifica este parámetro, &quot; &quot; &quot; &quot; también se deben especificar-c y-s.</td>
</tr>
<tr class="even">
<td>-a</td>
<td>Especifica la cuenta de usuario en la máquina que se está configurando. Puede ser una cuenta de dominio o de equipo local, como &quot; IWAM_TESTMACHINE &quot; , &quot; TESTUSER &quot; o &quot; TESTDOMAIN\DOMAINUSER &quot; .</td>
</tr>
<tr class="odd">
<td>-c</td>
<td>Especifica la ubicación y el nombre del <a href="glossary.md"><em>almacén de certificados</em></a>. Utilice &quot; LOCAL_MACHINE &quot; o &quot; CURRENT_USER &quot; para designar qué rama del registro se va a usar para la ubicación. El <em>almacén de certificados</em> puede estar instalado en la máquina. Los ejemplos de nombre típicos son &quot; My &quot; , &quot; root &quot; y &quot; TrustedPeople &quot; . La ubicación y el nombre del <em>almacén de certificados</em> se separan con una barra diagonal inversa, por ejemplo, &quot; LOCAL_MACHINE \root &quot; .
<blockquote>
[!Note]<br />
Aunque se &quot; &quot; puede especificar la rama CURRENT_USER del registro con este parámetro, la extensión del acceso a las claves privadas está pensada principalmente para los certificados instalados en un <a href="glossary.md"><em>almacén de certificados</em></a> del equipo local al que pueden tener acceso varios usuarios.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>-S</td>
<td>Especifica una cadena de búsqueda que no distingue entre mayúsculas y minúsculas para buscar el primer certificado enumerado con un nombre de sujeto que contiene esta subcadena.</td>
</tr>
<tr class="odd">
<td>-p</td>
<td>Especifica una contraseña que se usa para importar el certificado y la clave privada. Solo se usa con la opción de importación.</td>
</tr>
</tbody>
</table>



 

> [!NOTE]
> El usuario debe tener privilegios suficientes para usar esta herramienta, que requiere que el usuario sea un administrador y el mismo usuario que instaló el certificado de cliente, si está instalado.
>
> La herramienta "WinHttpCertCfg.exe" no es útil para configurar certificados almacenados en un sistema de archivos como FAT32, que no admite listas de control de acceso (ACL).

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestran algunas de las formas en que se puede usar la herramienta de configuración.

1.  Este comando muestra las cuentas que tienen acceso a la clave privada para el certificado "percertificate" en el [*almacén de certificados*](glossary.md) "raíz" de la \_ rama del equipo local del registro.

    **winhttpcertcfg-l-c raíz de la \_ máquina local \\ -s-certificado**

2.  Este comando concede acceso a la clave privada del certificado "mi certificado" en el [*almacén de certificados*](glossary.md) "mi" para la cuenta usuarioDePrueba.

    **winhttpcertcfg-g-c \_ equipo local \\ My-s mi certificado-a TESTUSER**

3.  Este comando importa un certificado y una clave privada de un archivo PFX y extiende el acceso a la clave privada a otra cuenta.

    **winhttpcertcfg-i PFXFile-c \_ equipo local \\ My-a IWAM \_ TESTMACHINE-p PFXPassword**

4.  Este comando deniega el acceso a la clave privada de la \_ cuenta de IWAM TESTMACHINE con el certificado especificado.

    **winhttpcertcfg-r-c \_ raíz del equipo local \\ -s-certificado-a IWAM \_ TESTMACHINE**

 

 




