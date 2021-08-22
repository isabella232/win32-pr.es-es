---
title: Empaquetado, implementación y consulta de Windows aplicaciones
description: Cree paquetes de aplicación para aplicaciones Windows, e instale, actualice, consulte y desinstale paquetes de aplicaciones mediante programación.
ms.assetid: 4ea65e62-4878-41fd-9ad8-424b1546f02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca79d235aa8d0d69c887eb67704d30137cf36a7583471f28269ac939a26b2a85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814278"
---
# <a name="packaging-deployment-and-query-of-windows-apps"></a>Empaquetado, implementación y consulta de Windows aplicaciones

Implemente, administre y administre aplicaciones de Windows (incluidos los UWP y las aplicaciones de escritorio) a través de paquetes de aplicaciones .msix/.appx basados en el formato OPC. Cada paquete de aplicación contiene los archivos que constituyen la aplicación y un archivo de manifiesto que describe el software que se va a Windows.

## <a name="introduction"></a>Introducción

Normalmente, los desarrolladores crean y firman paquetes de aplicaciones Visual Studio. Para obtener más información, [consulta Empaquetado de una aplicación para UWP Visual Studio](/windows/msix/package/packaging-uwp-apps).

La Microsoft Store facilita la compilación, el envío y la venta de las aplicaciones a clientes de todo el mundo. Para más información, consulte [Envíos de aplicaciones.](/windows/uwp/publish/app-submissions)

Windows PowerShell cmdlets permiten instalar y administrar aplicaciones de línea de Windows sin usar store. Para obtener más información, [vea Cmdlets de módulo Appx.](/powershell/module/appx/index?view=win10-ps)

Con las API de empaquetado, implementación y consulta, puede realizar estas tareas mediante programación:

-   Creación de un paquete de aplicación para una Windows aplicación
-   Implementación de una aplicación Windows empaquetado
-   Enumerar los paquetes de aplicación instalados en un sistema y obtener información sobre ellos desde su manifiesto
-   Consumo del contenido de un paquete de aplicación

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                    | Descripción                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cómo crear un paquete de aplicación (C++)](how-to-create-a-package.md)                                        | Aprenda a crear un paquete de aplicación mediante la API de empaquetado.                                                                                                                           |
| [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md) (Cómo crear un certificado de firma del paquete de la aplicación)      | Aprenda a usar [**MakeCert**](/windows-hardware/drivers/devtest/makecert) y [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) para crear un certificado de firma de código de prueba para que pueda firmar los paquetes de la aplicación. |
| [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md) (Cómo firmar un paquete de la aplicación con SignTool)                    | Aprenda a usar [**SignTool para**](/windows-hardware/drivers/devtest/signtool) firmar los paquetes de aplicación para que se puedan implementar.                                                                    |
| [Solución de errores de firma de paquetes de aplicaciones](how-to-troubleshoot-app-package-signature-errors.md) | Un error de implementación de la aplicación puede deberse a un error al validar la firma digital del paquete de la aplicación. Obtenga información sobre cómo reconocer estos errores y qué hacer con ellos.          |
| [Cómo firmar mediante programación un paquete de aplicación (C++)](how-to-programmatically-sign-a-package.md)          | Aprenda a firmar un paquete de aplicación mediante la [**función SignerSignEx2.**](/windows/desktop/SecCrypto/signersignex2)                                                                                   |
| [Desarrollo de una aplicación OEM que usa un archivo personalizado](how-to-develop-oem-app-with-custom-file.md)         | Obtenga información sobre cómo desarrollar una aplicación que usa un archivo personalizado para pasar información del OEM a la aplicación.                                                                                             |
| [Extracción del contenido del paquete de aplicación (C++)](how-to-extract-content-from-a-package.md)                          | Obtenga información sobre cómo extraer archivos de un paquete de aplicación mediante la API de empaquetado.                                                                                                               |
| [Consulta de la información del manifiesto del paquete de aplicación (C++)](how-to-query-package-identity-information.md)                   | Obtenga información de un manifiesto de paquete de aplicación mediante la API de empaquetado.                                                                                                            |
| [Solución de problemas](troubleshooting.md)                                                                   | Proporciona información para ayudarle a solucionar los problemas que experimenta al empaquetar, implementar o consultar un paquete de aplicación.                                                                 |
| [Referencia de API de empaquetado](interfaces.md)                                                                | La API de empaquetado crea, lee y escribe paquetes de aplicación.                                                                                                                            |
| [Referencia de api de implementación](package-deployment-api.md)                                                   | La API de implementación instala, actualiza y desinstala paquetes de aplicaciones.                                                                                                                    |
| [Referencia de la API de consulta](functions.md)                                                                     | La API de consulta obtiene información sobre los paquetes de aplicación instalados en el sistema.                                                                                                               |
| [Herramientas y cmdlets de PowerShell](appx-packaging-tools.md)                                                 | Use estas herramientas y cmdlets para crear, instalar y administrar paquetes de aplicaciones.                                                                                                              |
| [Muestras de SDK](appx-packaging-samples.md)                                                                | Descargue ejemplos del SDK que muestran las API de empaquetado, implementación y consulta para Windows aplicaciones.                                                                               |
| [Glosario](appx-packaging-glossary.md)                                                                  | Obtenga información sobre los términos relacionados con el empaquetado, la implementación y la consulta de Windows aplicaciones.                                                                                              |



 

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

[**Windows. ApplicationModel.Package**](/uwp/api/Windows.ApplicationModel.Package)
</dt> <dt>

[**Windows. ApplicationModel.PackageId**](/uwp/api/Windows.ApplicationModel.PackageId)
</dt> <dt>

[**Windows.Management.Deployment.PackageManager**](/uwp/api/Windows.Management.Deployment.PackageManager)
</dt> <dt>

[**Windows.Management.Deployment.PackageUserInformation**](/uwp/api/Windows.Management.Deployment.PackageUserInformation)
</dt> </dl>

 

 