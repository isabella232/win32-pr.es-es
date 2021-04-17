---
description: Las herramientas de criptografía proporcionan herramientas de línea de comandos para la firma de código, la comprobación de firmas y otras tareas de criptografía.
ms.assetid: 21adbcfb-fadd-4818-9dc5-23bfd526b525
title: Herramientas de criptografía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8003bb002bd8d203547779c96bc15491a5418169
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666407"
---
# <a name="cryptography-tools"></a>Herramientas de criptografía

Las herramientas de criptografía proporcionan herramientas de línea de comandos para la firma de código, la comprobación de firmas y otras tareas de criptografía.

## <a name="introduction-to-code-signing"></a>Introducción a la firma de código

El sector del software debe proporcionar a los usuarios los medios para confiar en el código, incluido el código publicado en Internet. Muchas páginas web contienen solo información estática que se puede descargar con poco riesgo. Sin embargo, algunas páginas contienen controles y aplicaciones que se van a descargar y ejecutar en el equipo de un usuario. Estos archivos ejecutables pueden ser arriesgados para descargarse y ejecutarse.

El software empaquetado utiliza marcas de ventas de personalización de marca y de confianza para garantizar la integridad de los usuarios, pero estas garantías no están disponibles cuando se transmite código en Internet. Además, el propio Internet no proporciona ninguna garantía sobre la identidad del creador del software. Ni puede garantizar que no se modifique ningún software descargado después de su creación. Los exploradores pueden mostrar un mensaje de advertencia que explica los posibles peligros de la descarga de datos de cualquier tipo, pero los exploradores no pueden comprobar que el código es lo que dice ser. Se debe adoptar un enfoque más activo para que Internet sea un medio confiable para distribuir software.

Un enfoque para proporcionar garantías de autenticidad e [*integridad*](../secgloss/i-gly.md) de los archivos es adjuntar [*firmas digitales*](../secgloss/d-gly.md) a esos archivos. Una firma digital adjunta a un archivo identifica el distribuidor de ese archivo y garantiza que el contenido del archivo no se modificó después de la creación de la firma.

Las firmas digitales se pueden crear y comprobar mediante las API de criptografía de Microsoft. Para obtener información general sobre la criptografía y las funciones de [*CryptoAPI*](../secgloss/c-gly.md) , consulte [Criptografía Essentials](cryptography-essentials.md).

Para obtener información detallada acerca de las [*firmas digitales*](../secgloss/d-gly.md), los [*certificados*](../secgloss/c-gly.md)y los [*almacenes de certificados*](../secgloss/c-gly.md), vea los temas siguientes:

-   [Hashes y firmas digitales](hashes-and-digital-signatures.md)
-   [Certificados digitales](digital-certificates.md)
-   [Administración de certificados con almacenes de certificados](managing-certificates-with-certificate-stores.md)
-   [Comprobación de certificados de confianza](certificate-trust-verification.md)

Actualmente, las herramientas de CryptoAPI admiten la tecnología Microsoft Authenticode al permitir a los proveedores de software firmar los siguientes tipos de archivos para la comprobación de Authenticode.



| Extensión de nombre de archivo                             | Contenido                                                                                                                                                                                                                              |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .appx<br/>                                | Archivos de instalador para una aplicación de dispositivo de la tienda Windows.<br/>                                                                                                                                                                            |
| .cab<br/>                                 | Archivos independientes usados para la instalación y configuración de la aplicación. En un archivo. cab, varios archivos se comprimen en un archivo. Normalmente se encuentran en discos de distribución de software de Microsoft.<br/>                        |
| .cat<br/>                                 | Archivos que contienen [*huellas*](../secgloss/t-gly.md) digitales digitales de varios archivos. Se puede usar un archivo. cat para garantizar la integridad de los archivos cuyas huellas digitales incluye.<br/> |
| .dll<br/>                                 | Archivos que contienen funciones ejecutables.<br/>                                                                                                                                                                                   |
| .exe<br/>                                 | Archivos que contienen programas ejecutables.<br/>                                                                                                                                                                                    |
| .js<br/> .vbs<br/> .wsf<br/>  | Archivos del shell de Windows para JScript o Microsoft Visual Basic Scripting Edition (VBScript).<br/>                                                                                                                                    |
| .msi<br/> .msp<br/> .mst<br/> | Archivos de Windows Installer.<br/>                                                                                                                                                                                                   |
| .ocx<br/>                                 | Archivos que contienen controles ActiveX de Microsoft.<br/>                                                                                                                                                                             |
| .ps1<br/>                                 | Archivos que contienen scripts de PowerShell.<br/>                                                                                                                                                                                     |
| . STL<br/>                                 | Archivos que contienen una [*lista de certificados de confianza*](../secgloss/c-gly.md) (CTL).<br/>                                                                           |
| .sys<br/>                                 | Archivos que contienen archivos binarios del controlador.<br/>                                                                                                                                                                                        |



 

Para obtener información acerca de la firma digital, consulte los siguientes documentos:

-   CCITt, recomendación X. 509, *el marco de trabajo de Directory-Authentication, el* Comité de consulta, el teléfono internacional y el telegráfico, la Unión Internacional de telecomunicaciones, ginebra, 1989.
-   RSA Laboratories, *PKCS \# 7: estándar de sintaxis de mensajes criptográficos*. Versión 1,5, noviembre y 1993.
-   Schneier, Bruce, *criptografía aplicada*, 2d ed. Nueva York: John Wiley & hijos, 1996.
-   [https://www.rsa.com](https://www.rsa.com/)

> [!Note]  
> Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.

 

## <a name="microsoft-cryptography-tools"></a>Herramientas de criptografía de Microsoft

Las herramientas de publicación y la DLL de firma se instalan en el \\ directorio bin de la instalación de Microsoft SDK. Incluyen los siguientes archivos.



| Nombre de archivo                    | Observaciones                                                                                                                                                                                             |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cert2SPC.exe](cert2spc.md) | Crea un [*certificado de editor de software*](../secgloss/s-gly.md) (SPC) solo con fines de prueba.<br/> |
| [CertMgr.exe](certmgr.md)   | Administra certificados, CTL y [*listas de revocación de certificados*](../secgloss/c-gly.md) (CRL).<br/>             |
| [MakeCat.exe](makecat.md)   | Crea un archivo de catálogo sin firmar que contiene los valores hash de un conjunto de archivos junto con los atributos asociados de cada archivo.<br/>                                                               |
| [MakeCert.exe](makecert.md) | Crea un certificado [*X. 509*](../secgloss/x-gly.md) solo con fines de prueba.<br/>                                                                      |
| Pvk2pfx.exe                  | Convierte un archivo de certificado de editor de software (. SPC) o un archivo de clave privada (. PVK) al formato de archivo de intercambio de información personal (PFX).<br/>                                                   |
| [SetReg.exe](setreg.md)     | Establece las claves del registro que controlan la comprobación de certificados.<br/>                                                                                                                                |
| [SignTool.exe](signtool.md) | Los signos y la hora marcan un archivo. Además, comprueba la firma de un archivo.<br/>                                                                                                              |



 

 

 
