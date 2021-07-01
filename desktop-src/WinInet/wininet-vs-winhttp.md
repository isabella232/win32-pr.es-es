---
title: WinINet frente a WinHTTP
description: Aprenda a elegir entre WinInet y WinHTTP. Lea una comparación de características y revise los temas relacionados.
ms.assetid: 77386b54-2c86-4a30-8c4c-88d5f15313d7
keywords:
- WinINet frente a WinHTTP
ms.topic: article
ms.date: 02/22/2019
ms.openlocfilehash: 8ced80dd048559fee483e8cf121918eed75fc462
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118800"
---
# <a name="wininet-vs-winhttp"></a>WinINet frente a WinHTTP

Con algunas excepciones, [WinINet](portal.md) es un superconjunto de [WinHTTP.](/windows/desktop/WinHttp/winhttp-start-page) Al seleccionar entre los dos, debes usar WinINet, a menos que planees ejecutar dentro de un proceso de servicio o servicio que requiera suplantación y aislamiento de sesión.

## <a name="comparison-of-features"></a>Comparación de características

| Característica | Wininet | WinHTTP |
|-|-|-|
| **Caché de credenciales** Permite que todas las aplicaciones integradas de Windows Internet Explorer obtengan credenciales automáticamente. También permite que una aplicación que se ejecuta fuera de Internet Explorer solicitar o especificar las credenciales para el servidor solo una vez. A partir de ese momento, las solicitudes son automáticas. | Sí | No |
| **Credential Prompting** Proporciona una API que permite que el código de llamada solicite al usuario las credenciales. | Sí | No |
| **FTP** | Sí | No |
| **Compatibilidad con Autodial/RAS** Se trata de una funcionalidad heredada. En [su lugar, use acceso](/windows/desktop/RRAS/portal) remoto. | Sí | No |
| **Zonas** Integración automática con Internet Explorer de seguridad. | Sí | No |
| **Compatibilidad con IDNA** Compatibilidad integrada con RFC/Punycode de IDNA. | Sí | Sí |
| **API jar de cookies** Se admiten cookies persistentes y no persistentes. Cualquier aplicación o script puede usarlo para ver las mismas cookies que el explorador. | Sí | No |
| **Compatibilidad con IE en modo protegido** | Sí | No |
| **Compatibilidad con la descompresión** Compatibilidad con el esquema de compresión gzip y deflate. | Sí | Sí |
| **Compatibilidad con la carga fragmentada** El código de cliente debe realizar la fragmentación. | No | sí |
| **Compatibilidad con SOCKS v4** No incluye v4a o v5. | Sí | No |
| **Envío y recepción bidireccionales** | No | No |
| **E/S superpuesta** | No | No |
| **Compatibilidad con esquemas de archivo** Útil para scripts de proxy con un esquema de archivo. | Sí | No |
| **InternetOpenUrl** Código simplificado para abrir una dirección URL. | Sí | No |
| **Soporte técnico de servicios** Se puede ejecutar desde un servicio o una cuenta de servicio. | No | sí |
| **Aislamiento de sesión** Las sesiones independientes no se afectan entre sí. | No | sí |
| **Suplantación** Admite la llamada mientras el subproceso suplanta a un usuario diferente. | No | sí |

## <a name="related-topics"></a>Temas relacionados

* [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
* [Wininet](/windows/desktop/WinInet/about-wininet)