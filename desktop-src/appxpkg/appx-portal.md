---
title: Empaquetado, implementación y consulta de aplicaciones de Windows
description: Cree mediante programación paquetes de aplicaciones para aplicaciones Windows e instale, actualice, consulte y desinstale paquetes de aplicaciones.
ms.assetid: 4ea65e62-4878-41fd-9ad8-424b1546f02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bfd1792e0b7b18f0dee04bca6f352e055b20f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149189"
---
# <a name="packaging-deployment-and-query-of-windows-apps"></a>Empaquetado, implementación y consulta de aplicaciones de Windows

Puede implementar, administrar y dar servicio a aplicaciones de Windows (incluidas las aplicaciones de escritorio y UWPs) a través de paquetes de la aplicación. msix/. appx basados en el formato OPC. Cada paquete de aplicación contiene los archivos que constituyen la aplicación y un archivo de manifiesto que describe el software para Windows.

## <a name="introduction"></a>Introducción

Normalmente, los desarrolladores crean y firman paquetes de aplicación mediante Visual Studio. Para obtener más información, consulte [empaquetar una aplicación para UWP con Visual Studio](/windows/msix/package/packaging-uwp-apps).

El Microsoft Store facilita la compilación, el envío y la venta de sus aplicaciones a clientes de todo el mundo. Para obtener más información, consulte [envíos de aplicaciones](/windows/uwp/publish/app-submissions).

Los cmdlets de Windows PowerShell permiten instalar y administrar aplicaciones Windows de línea de negocio sin usar la tienda. Para obtener más información, consulte [cmdlets del módulo appx](/powershell/module/appx/index?view=win10-ps).

Con las API de empaquetado, implementación y consulta, puede realizar estas tareas mediante programación:

-   Crear un paquete de aplicación para una aplicación de Windows
-   Implementar una aplicación de Windows empaquetada
-   Enumerar los paquetes de la aplicación instalados en un sistema y obtener información sobre ellos desde su manifiesto
-   Usar el contenido de un paquete de la aplicación

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                    | Descripción                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cómo crear un paquete de aplicación (C++)](how-to-create-a-package.md)                                        | Obtenga información sobre cómo crear un paquete de la aplicación con la API de empaquetado.                                                                                                                           |
| [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md) (Cómo crear un certificado de firma del paquete de la aplicación)      | Obtenga información sobre cómo usar [**Makecert**](/windows-hardware/drivers/devtest/makecert) y [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) para crear un certificado de firma de código de prueba, de modo que pueda firmar los paquetes de la aplicación. |
| [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md) (Cómo firmar un paquete de la aplicación con SignTool)                    | Obtenga información sobre cómo usar [**SignTool**](/windows-hardware/drivers/devtest/signtool) para firmar los paquetes de la aplicación de forma que se puedan implementar.                                                                    |
| [Cómo solucionar errores de firma de paquete de aplicaciones](how-to-troubleshoot-app-package-signature-errors.md) | Un error de implementación de la aplicación puede deberse a un error al validar la firma digital del paquete de la aplicación. Obtenga información acerca de cómo reconocer estos errores y qué hacer con ellos.          |
| [Cómo firmar un paquete de aplicación mediante programación (C++)](how-to-programmatically-sign-a-package.md)          | Obtenga información sobre cómo firmar un paquete de aplicación mediante la función [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .                                                                                   |
| [Cómo desarrollar una aplicación de OEM que use un archivo personalizado](how-to-develop-oem-app-with-custom-file.md)         | Obtenga información sobre cómo desarrollar una aplicación que use un archivo personalizado para pasar información del OEM a la aplicación.                                                                                             |
| [Extraer el contenido del paquete de la aplicación (C++)](how-to-extract-content-from-a-package.md)                          | Obtenga información sobre cómo extraer archivos de un paquete de la aplicación mediante la API de empaquetado.                                                                                                               |
| [Información del manifiesto del paquete de la aplicación de consulta (C++)](how-to-query-package-identity-information.md)                   | Obtenga información sobre cómo obtener información de un manifiesto del paquete de aplicaciones mediante la API de empaquetado.                                                                                                            |
| [Solución de problemas](troubleshooting.md)                                                                   | Proporciona información para ayudarle a solucionar los problemas que experimente al empaquetar, implementar o consultar un paquete de la aplicación.                                                                 |
| [Referencia de la API de empaquetado](interfaces.md)                                                                | La API de empaquetado crea, Lee y escribe paquetes de aplicaciones.                                                                                                                            |
| [Referencia de la API de implementación](package-deployment-api.md)                                                   | La API de implementación instala, actualiza y desinstala paquetes de aplicaciones.                                                                                                                    |
| [Referencia de API de consulta](functions.md)                                                                     | La API de consulta obtiene información sobre los paquetes de aplicación instalados en el sistema.                                                                                                               |
| [Herramientas y cmdlets de PowerShell](appx-packaging-tools.md)                                                 | Use estas herramientas y cmdlets para crear, instalar y administrar paquetes de aplicaciones.                                                                                                              |
| [Muestras de SDK](appx-packaging-samples.md)                                                                | Descargue ejemplos de SDK que muestran las API de empaquetado, implementación y consulta de aplicaciones de Windows.                                                                               |
| [Glosario](appx-packaging-glossary.md)                                                                  | Obtenga información sobre los términos relacionados con el empaquetado, la implementación y la consulta de aplicaciones de Windows.                                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptos**
</dt> <dt>

[Implementación y paquetes de aplicaciones](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

**Otra referencia**
</dt> <dt>

[Esquema del manifiesto del paquete de la aplicación](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[**Windows. ApplicationModel. Package**](/uwp/api/Windows.ApplicationModel.Package)
</dt> <dt>

[**Windows. ApplicationModel. PackageId**](/uwp/api/Windows.ApplicationModel.PackageId)
</dt> <dt>

[**Windows.Management.Deployment.PackageManager**](/uwp/api/Windows.Management.Deployment.PackageManager)
</dt> <dt>

[**Windows.Management.Deployment.PackageUserInformation**](/uwp/api/Windows.Management.Deployment.PackageUserInformation)
</dt> </dl>

 

 