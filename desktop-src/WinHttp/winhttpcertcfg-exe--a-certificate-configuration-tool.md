---
description: La herramienta de configuración de certificados de servicios HTTP de Microsoft Windows (WinHTTP), &\# 0034;WinHttpCertCfg.exe&0034;, permite a los administradores instalar y configurar certificados de cliente en cualquier almacén de certificados al que pueda acceder la cuenta de \# Internet Server Web Application Manager (IWAM). La herramienta también elimina la necesidad de hacer algo especial en cuentas como la cuenta de IWAM para obtener acceso a los certificados al usar Active Server Pages (ASP).
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe, una herramienta de configuración de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b8fbfadd6cf0282f63b26c8dd40d5ef96b5f54
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466432"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a>WinHttpCertCfg.exe, una herramienta de configuración de certificados

La herramienta de configuración de certificados de servicios [HTTP de Microsoft Windows (WinHTTP),](about-winhttp.md) "WinHttpCertCfg.exe", [](glossary.md) permite a los administradores instalar y configurar certificados de cliente en cualquier almacén de certificados al que pueda acceder la cuenta del Administrador de aplicaciones web de Internet Server (IWAM). La herramienta también elimina la necesidad de hacer algo especial en cuentas como la cuenta de IWAM para obtener acceso a los certificados al usar Active Server Pages (ASP).

El Microsoft Management Console (MMC) permite a los administradores importar certificados de cliente a un equipo local. Sin embargo, la importación de un certificado no concede automáticamente acceso a la clave privada para otras cuentas. Esta clave privada es necesaria para la autenticación de certificados de cliente. La herramienta de configuración de certificados de Microsoft Windows HTTP Services (WinHTTP) proporciona la capacidad de conceder acceso a cuentas adicionales, como la cuenta de IWAM, cuando sea necesario.

-   [Uso de la herramienta de configuración de certificados](#using-the-certificate-configuration-tool)
-   [Ejemplos](#examples)

## <a name="using-the-certificate-configuration-tool"></a>Uso de la herramienta de configuración de certificados

La herramienta de configuración de certificados WinHTTP, WinHttpCertCfg.exe, está disponible como descarga en el sitio web Windows Resource Kit Tools de [Windows Server 2003.](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) En el código de ejemplo siguiente se muestran los parámetros de línea de comandos válidos que se usarán con esta herramienta.

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

En la tabla siguiente se enumeran los parámetros de la herramienta de configuración.




| Parámetro | Descripción | 
|-----------|-------------|
| -? | Muestra los datos de sintaxis. | 
| -i | Especifica que el certificado se va a importar desde un archivo de Exchange personal (PFX). Este parámetro debe ir seguido del nombre del archivo. Cuando se especifica este parámetro, también se deben especificar "-a" y "-c". | 
| -g | Especifica que se concede acceso a una clave privada. Cuando se especifica este parámetro, también se deben especificar "-a", "-c" y "-s". | 
| -r | Especifica que se quita el acceso para una clave privada. Cuando se especifica este parámetro, también se deben especificar "-a", "-c" y "-s". | 
| -l | Especifica que se enumeran las cuentas con acceso a una clave privada. Cuando se especifica este parámetro, también se deben especificar "-c" y "-s". | 
| -a | Especifica la cuenta de usuario en la máquina que se está configurando. Podría ser una máquina local o una cuenta de dominio, como "IWAM_TESTMACHINE", "TESTUSER" o "TESTDOMAIN\DOMAINUSER". | 
| -c | Especifica la ubicación y el nombre del almacén <a href="glossary.md"><em>de certificados.</em></a> Use "LOCAL_MACHINE" o "CURRENT_USER" para designar qué rama del Registro se va a usar para la ubicación. El <em>almacén de</em> certificados puede ser cualquier instalado en la máquina. Los ejemplos de nombres típicos son "MY", "Root" y "TrustedPeople". La ubicación y el nombre del almacén <em>de certificados</em> se separan con una barra diagonal hacia atrás, por ejemplo, "LOCAL_MACHINE\Root".<blockquote>[!Note]<br />Aunque la rama "CURRENT_USER" del registro se puede especificar con este parámetro, la extensión del acceso a las claves <a href="glossary.md"><em></em></a> privadas está pensada principalmente para los certificados instalados en un almacén de certificados de equipo local al que pueden tener acceso varios usuarios.</blockquote><br /> | 
| -S | Especifica una cadena de búsqueda que no tiene en cuenta las mayúsculas y minúsculas para buscar el primer certificado enumerado con un nombre de sujeto que contiene esta subcadena. | 
| -p | Especifica una contraseña que se usa para importar el certificado y la clave privada. Esto solo se usa con la opción de importación. | 




 

> [!NOTE]
> El usuario debe tener privilegios suficientes para usar esta herramienta, que requiere que el usuario sea administrador y el mismo usuario que instaló el certificado de cliente, si está instalado.
>
> La herramienta "WinHttpCertCfg.exe" no es útil para configurar certificados almacenados en un sistema de archivos como FAT32, que no admite listas de control de acceso (ACL).

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestran algunas de las formas en que se puede usar la herramienta de configuración.

1.  Este comando enumera las cuentas que tienen acceso a la clave privada [](glossary.md) para el certificado "MyCertificate" en el almacén de certificados "Raíz" de la rama LOCAL \_ MACHINE del registro.

    **winhttpcertcfg -l -c RAÍZ DE MÁQUINA LOCAL \_ \\ -s MyCertificate**

2.  Este comando concede acceso a la clave privada del certificado [](glossary.md) "MyCertificate" en el almacén de certificados "My" para la cuenta TESTUSER.

    **winhttpcertcfg -g -c LOCAL \_ MACHINE \\ My -s MyCertificate -a TESTUSER**

3.  Este comando importa un certificado y una clave privada de un archivo PFX y extiende el acceso de clave privada a otra cuenta.

    **winhttpcertcfg -i PFXFile -c LOCAL \_ MACHINE \\ My -a IWAM \_ TESTMACHINE -p PFXPassword**

4.  Este comando deniega el acceso a la clave privada de la cuenta TESTMACHINE de IWAM \_ con el certificado especificado.

    **winhttpcertcfg -r -c LOCAL \_ MACHINE \\ Root -s MyCertificate -a IWAM \_ TESTMACHINE**

 

 




