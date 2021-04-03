---
title: Usar canales autenticados seguros
description: Usar canales autenticados seguros
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows Media Administrador de dispositivos, autenticación
- Administrador de dispositivos, autenticación
- aplicaciones de escritorio, autenticación
- proveedores de servicios, autenticación
- Guía de programación, autenticación
- autenticación
- Windows Media Administrador de dispositivos, comunicación segura
- Administrador de dispositivos, protección de la comunicación
- aplicaciones de escritorio, comunicación segura
- proveedores de servicios, comunicación segura
- Guía de programación, comunicación segura
- comunicación segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88c271cecc2e9252a3f7af0540beef3dc57d2b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075351"
---
# <a name="using-secure-authenticated-channels"></a>Usar canales autenticados seguros

Windows Media Administrador de dispositivos habilita la autenticación y la comunicación segura entre los componentes proporcionando dos clases auxiliares, [CSecureChannelClient](csecurechannelclient-class.md) (para aplicaciones) y [CSecureChannelServer](csecurechannelserver-class.md) (para proveedores de servicios), y una interfaz, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (para ambos). Juntas, componen una API para el uso de canales autenticados seguros (SAC). SAC controla las tres tareas siguientes para proveedores de servicios o aplicaciones que usan Windows Media Administrador de dispositivos:

-   [Autenticación de componentes](component-authentication.md)
-   [Cifrado y descifrado](encryption-and-decryption.md)
-   [Autenticación de mensajes](message-authentication.md)

Una aplicación o proveedor de servicios debe administrar la autenticación de componentes, el cifrado y el descifrado. la autenticación de mensajes es opcional.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tareas comunes a las aplicaciones y proveedores de servicios**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




