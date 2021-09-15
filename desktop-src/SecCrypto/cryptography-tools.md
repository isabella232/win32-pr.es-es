---
description: Las herramientas de criptografía proporcionan herramientas de línea de comandos para la firma de código, la comprobación de firmas y otras tareas de criptografía.
ms.assetid: 21adbcfb-fadd-4818-9dc5-23bfd526b525
title: Herramientas de criptografía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8003bb002bd8d203547779c96bc15491a5418169
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271047"
---
# <a name="cryptography-tools"></a>Herramientas de criptografía

Las herramientas de criptografía proporcionan herramientas de línea de comandos para la firma de código, la comprobación de firmas y otras tareas de criptografía.

## <a name="introduction-to-code-signing"></a>Introducción a la firma de código

El sector del software debe proporcionar a los usuarios los medios para confiar en el código, incluido el código publicado en Internet. Muchas páginas web contienen solo información estática que se puede descargar con poco riesgo. Sin embargo, algunas páginas contienen controles y aplicaciones que se descargarán y ejecutarán en el equipo de un usuario. Estos archivos ejecutables pueden ser de riesgo para descargar y ejecutar.

El software empaquetado usa la personalidad de marca y los puntos de venta de confianza para garantizar a los usuarios su integridad, pero estas garantías no están disponibles cuando el código se transmite en Internet. Además, Internet no puede proporcionar ninguna garantía sobre la identidad del creador del software. Tampoco puede garantizar que ningún software descargado no se haya modificado después de su creación. Los exploradores pueden mostrar un mensaje de advertencia que explica los posibles riesgos de descargar datos de cualquier tipo, pero los exploradores no pueden comprobar que el código es lo que dice ser. Se debe adoptar un enfoque más activo para que Internet sea un medio confiable para distribuir software.

Un enfoque para proporcionar garantías de la autenticidad e [*integridad*](../secgloss/i-gly.md) de los archivos es adjuntar firmas [*digitales*](../secgloss/d-gly.md) a esos archivos. Una firma digital adjunta a un archivo identifica positivamente el distribuidor de ese archivo y garantiza que el contenido del archivo no se cambió después de crear la firma.

Las firmas digitales se pueden crear y comprobar mediante las API de criptografía de Microsoft. Para obtener información general sobre la criptografía y las [*funciones de CryptoAPI,*](../secgloss/c-gly.md) vea [Cryptography Essentials](cryptography-essentials.md).

Para obtener información detallada sobre [*las firmas digitales,*](../secgloss/d-gly.md) [*los certificados*](../secgloss/c-gly.md)y los almacenes de [*certificados*](../secgloss/c-gly.md), vea los temas siguientes:

-   [Hashes y firmas digitales](hashes-and-digital-signatures.md)
-   [Certificados digitales](digital-certificates.md)
-   [Administración de certificados con almacenes de certificados](managing-certificates-with-certificate-stores.md)
-   [Comprobación de confianza de certificados](certificate-trust-verification.md)

Actualmente, CryptoAPI Tools admite la tecnología De Microsoft Authenticode al permitir que los proveedores de software firmen los siguientes tipos de archivos para la comprobación de Authenticode.



| Extensión de nombre de archivo                             | Contenido                                                                                                                                                                                                                              |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .appx<br/>                                | Archivos del instalador para una aplicación Windows store.<br/>                                                                                                                                                                            |
| .cab<br/>                                 | Archivos independientes que se usan para la instalación y la instalación de aplicaciones. En un archivo archivador, varios archivos se comprimen en un archivo. Normalmente se encuentran en discos de distribución de software de Microsoft.<br/>                        |
| .cat<br/>                                 | Archivos que contienen huellas [*digitales*](../secgloss/t-gly.md) de varios archivos. Se puede usar un archivo .cat para garantizar la integridad de los archivos cuyas huellas digitales incluye.<br/> |
| .dll<br/>                                 | Archivos que contienen funciones ejecutables.<br/>                                                                                                                                                                                   |
| .exe<br/>                                 | Archivos que contienen programas ejecutables.<br/>                                                                                                                                                                                    |
| .js<br/> .vbs<br/> .wsf<br/>  | Windows shell para JScript o Microsoft Visual Basic Scripting Edition (VBScript).<br/>                                                                                                                                    |
| .msi<br/> .msp<br/> .mst<br/> | Windows archivos del instalador.<br/>                                                                                                                                                                                                   |
| .ocx<br/>                                 | Archivos que contienen controles ActiveX Microsoft.<br/>                                                                                                                                                                             |
| .ps1<br/>                                 | Archivos que contienen scripts de PowerShell.<br/>                                                                                                                                                                                     |
| .stl<br/>                                 | Archivos que contienen una [*lista de certificados de confianza*](../secgloss/c-gly.md) (CTL).<br/>                                                                           |
| .sys<br/>                                 | Archivos que contienen archivos binarios del controlador.<br/>                                                                                                                                                                                        |



 

Para obtener información sobre la firma digital, consulte los siguientes documentos:

-   CCITT, Recomendación X.509, The *Directory-Authentication Framework,* Comité de consulta, Teléfono internacional y telégrafo, Unión internacional de telecomunicaciones, Ginebra, 1989.
-   Rsa Rsa, *PKCS \# 7: estándar de* sintaxis de mensajes criptográficos . Versión 1.5, noviembre de 1993.
-   Schneier,Pliquen, *Applied Cryptography*, 2d ed. Nueva York: John Wiley & Sons, 1996.
-   [https://www.rsa.com](https://www.rsa.com/)

> [!Note]  
> Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.

 

## <a name="microsoft-cryptography-tools"></a>Herramientas de criptografía de Microsoft

Las herramientas de publicación y el archivo DLL de firma se instalan en el \\ directorio Bin de la instalación de Microsoft SDK. Incluyen los siguientes archivos.



| Nombre de archivo                    | Observaciones                                                                                                                                                                                             |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cert2SPC.exe](cert2spc.md) | Crea un [*certificado de Publisher software*](../secgloss/s-gly.md) (SPC) solo con fines de prueba.<br/> |
| [CertMgr.exe](certmgr.md)   | Administra certificados, CL y [*listas de revocación de certificados*](../secgloss/c-gly.md) (CRL).<br/>             |
| [MakeCat.exe](makecat.md)   | Crea un archivo de catálogo sin signo que contiene los hashes de un conjunto de archivos junto con los atributos asociados de cada archivo.<br/>                                                               |
| [MakeCert.exe](makecert.md) | Crea un [*certificado X.509*](../secgloss/x-gly.md) solo con fines de prueba.<br/>                                                                      |
| Pvk2pfx.exe                  | Convierte un archivo de certificado de publicador de software (.spc) o un archivo de clave privada (.pvk) al formato de archivo Exchange información personal (PFX).<br/>                                                   |
| [SetReg.exe](setreg.md)     | Establece las claves del Registro que controlan la comprobación del certificado.<br/>                                                                                                                                |
| [SignTool.exe](signtool.md) | Firma y marca de tiempo un archivo. Además, comprueba la firma de un archivo.<br/>                                                                                                              |



 

 

 
