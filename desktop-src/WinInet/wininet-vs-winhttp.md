---
title: WinINet frente a WinHTTP
description: Con algunas excepciones, WinINet es un supraconjunto de WinHTTP. Al seleccionar entre los dos, debe usar WinINet, a menos que tenga previsto ejecutarlo en un servicio o un proceso similar a un servicio que requiera la suplantación y el aislamiento de la sesión.
ms.assetid: 77386b54-2c86-4a30-8c4c-88d5f15313d7
keywords:
- WinINet frente a WinHTTP
ms.topic: article
ms.date: 02/22/2019
ms.openlocfilehash: c4d161992c2202505e8c84c660ca1edc92cc7993
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704995"
---
# <a name="wininet-vs-winhttp"></a>WinINet frente a WinHTTP

Con algunas excepciones, [WinInet](portal.md) es un supraconjunto de [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page). Al seleccionar entre los dos, debe usar WinINet, a menos que tenga previsto ejecutarlo en un servicio o un proceso similar a un servicio que requiera la suplantación y el aislamiento de la sesión.

## <a name="comparison-of-features"></a>Comparación de características

| Característica | WinINet | WinHTTP |
|-|-|-|
| **Caché de credenciales** Permite que todas las aplicaciones integradas en Windows Internet Explorer obtengan las credenciales automáticamente. También permite que una aplicación que se ejecuta fuera de Internet Explorer solicite o especifique las credenciales del servidor una sola vez. Desde entonces, las solicitudes son automáticas. | sí | no |
| **Petición de credenciales** Proporciona una API que permite al código de llamada solicitar las credenciales al usuario. | sí | no |
| **FTP** | sí | no |
| **Compatibilidad con el marcado automático y el ras** Esta es la funcionalidad heredada. En su lugar, use [acceso remoto](/windows/desktop/RRAS/portal) . | sí | no |
| **Zonas** de Integración automática con zonas de seguridad de Internet Explorer. | sí | no |
| **Compatibilidad con IDNA** Compatibilidad integrada con el RFC/Punycode de IDNA. | sí | sí |
| **API jar de cookies** Se admiten las cookies persistentes y no persistentes. Cualquier aplicación o script puede usarse para ver las mismas cookies que el explorador. | sí | no |
| **Compatibilidad con IE en modo protegido** | sí | no |
| **Compatibilidad con la descompresión** Compatibilidad con el esquema de compresión gzip y DEFLATE. | sí | sí |
| **Compatibilidad con la carga fragmentada** El código de cliente debe realizar la fragmentación. | no | sí |
| **Compatibilidad con Socks V4** No incluye V4A o V5. | sí | no |
| **Envío y recepción bidireccionales** | no | no |
| **E/s superpuestas** | no | no |
| **Compatibilidad con esquemas de archivo** Útil para scripts de proxy con un esquema de archivo. | sí | no |
| **InternetOpenUrl** Código simplificado para abrir una dirección URL. | sí | no |
| **Compatibilidad con servicios** Se puede ejecutar desde un servicio o una cuenta de servicio. | no | sí |
| **Aislamiento de sesión** Las sesiones independientes no se ven afectadas entre sí. | no | sí |
| **Suplantación** Admite la llamada mientras el subproceso suplanta a otro usuario. | no | sí |

## <a name="related-topics"></a>Temas relacionados

* [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
* [WinINet](/windows/desktop/WinInet/about-wininet)