---
description: En este ejemplo se muestra cómo crear una instalación basada en una dirección URL de un paquete de Windows Installer.
ms.assetid: a38a1132-43b4-449d-b134-f351ce370223
title: Ejemplo de instalación de Windows Installer basado en URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a210eb1b93202930309223b49c737aa85b1812
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105653261"
---
# <a name="a-url-based-windows-installer-installation-example"></a>Ejemplo de instalación de Windows Installer basado en URL

En este ejemplo se muestra cómo crear una instalación basada en una dirección URL de un paquete de Windows Installer. Para obtener más información acerca de la protección de instalaciones y el uso de certificados digitales, consulte las [instrucciones para crear instalaciones seguras](guidelines-for-authoring-secure-installations.md) y [firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md).

Para reproducir este ejemplo, necesita la utilidad [SignTool](../seccrypto/signtool.md) . Para obtener más información, consulte la referencia de las [herramientas de CryptoAPI](../seccrypto/cryptoapi-tools-reference.md) en el kit de desarrollo de software (SDK) de Microsoft Windows. También necesita [Msistuff.exe](msistuff-exe.md) y Setup.exe utilidades de los [componentes Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Para obtener más información, consulte [arranque de descarga en Internet](internet-download-bootstrapping.md).

El ejemplo tiene las siguientes especificaciones:

-   Cuando los usuarios visiten su sitio web y hagan clic en el vínculo "instalar instalación", se les presentará la opción de guardar o ejecutar desde esa ubicación. Si el usuario selecciona ejecutar desde esa ubicación, el Setup.exe actualiza la versión de Windows Installer en su equipo, si es necesario, comprueba la firma digital en el paquete del instalador e instala el paquete en su equipo.
-   Hay un certificado digital, MyCert. cer, que se proporciona con una clave privada, MyCert. PVK.
-   La dirección URL del sitio web hipotético que visitará un cliente para instalar el paquete es https: \/ /www.blueyonderairlines.com/Products/MySetup/mysetup.html.
-   El diseño del servidor web es el siguiente. 

    | URL                                                               | Archivo        | Descripción                                    |
    |-------------------------------------------------------------------|-------------|------------------------------------------------|
    | https: \/ /www.blueyonderairlines.com/products/MySetup/               | Setup.exe   | Setup.exe arranque.                        |
    | https: \/ /www.blueyonderairlines.com/products/MySetup/               | MySetup.msi | Paquete de instalación                           |
    | https: \/ /www.blueyonderairlines.com/products/MySetup/               | Cab1.cab    | Archivo. cab de origen \# 1                        |
    | https: \/ /www.blueyonderairlines.com/products/MySetup/               | Cab2.cab    | Archivo de origen Cabinet \# 2                        |
    | https: \/ /www.blueyonderairlines.com/products/Common/InstMsi/ANSI    | Instmsi.exe | ANSI Windows Installer 2,0 Redistributable.    |
    | https: \/ /www.blueyonderairlines.com/products/Common/InstMsi/Unicode | Instmsi.exe | Unicode Windows Installer 2,0 Redistributable. |

    

     

[Continuar](configuring-the-setup-exe-resources.md)

 

 
