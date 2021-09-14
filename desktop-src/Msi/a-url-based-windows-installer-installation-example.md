---
description: En este ejemplo se muestra cómo crear una instalación basada en url de un paquete Windows Installer.
ms.assetid: a38a1132-43b4-449d-b134-f351ce370223
title: Ejemplo de instalación de Windows Installer basado en URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a210eb1b93202930309223b49c737aa85b1812
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159270"
---
# <a name="a-url-based-windows-installer-installation-example"></a>Ejemplo de instalación de Windows Installer basado en URL

En este ejemplo se muestra cómo crear una instalación basada en url de un paquete Windows Installer. Para obtener más información sobre cómo proteger las instalaciones y el uso de certificados digitales, vea [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and Digital Signatures (Directrices para crear instalaciones seguras y firmas [digitales) y Windows Installer](digital-signatures-and-windows-installer.md).

Para reproducir este ejemplo, necesita la [utilidad SignTool.](../seccrypto/signtool.md) Para más información, consulte [la Referencia de las herramientas de CryptoAPI](../seccrypto/cryptoapi-tools-reference.md) en el Kit de desarrollo de software (SDK) de Microsoft Windows. También necesita utilidades [Msistuff.exe](msistuff-exe.md) y Setup.exe del SDK de Windows para desarrolladores [Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Para obtener más información, vea [Internet Download Bootstrapping](internet-download-bootstrapping.md).

El ejemplo tiene las especificaciones siguientes:

-   Cuando los usuarios visitan su sitio web y hacen clic en el vínculo "Instalación de MySetup", se les presenta la opción de guardar o ejecutar desde esa ubicación. Si el usuario selecciona ejecutar desde esa ubicación, el Setup.exe actualiza la versión de Windows Installer en su equipo, si es necesario, comprueba la firma digital en el paquete del instalador e instala el paquete en su equipo.
-   Hay un certificado digital, Mycert.cer, que se proporciona con una clave privada, Mycert.pvk.
-   La dirección URL del sitio web hipotético que un cliente visitaría para instalar el paquete es https: \/ /www.blueyonderairlines.com/Products/MySetup/mysetup.html.
-   El diseño del servidor web es el siguiente. 

    | URL                                                               | Archivo        | Descripción                                    |
    |-------------------------------------------------------------------|-------------|------------------------------------------------|
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | Setup.exe   | Setup.exe previo.                        |
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | MySetup.msi | Paquete de instalación                           |
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | Cab1.cab    | Archivador de archivos de \# origen 1                        |
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | Cab2.cab    | Archivador de archivos de \# origen 2                        |
    | https: \/ /www.blueyonderairlines.com/Products/Common/InstMsi/Ansi    | Instmsi.exe | Ansi Windows Installer 2.0 redistribuible.    |
    | https: \/ /www.blueyonderairlines.com/Products/Common/InstMsi/Unicode | Instmsi.exe | Unicode Windows Installer 2.0 redistribuible. |

    

     

[Continuar](configuring-the-setup-exe-resources.md)

 

 
