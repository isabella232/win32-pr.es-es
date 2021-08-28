---
title: Uso de canales autenticados seguros
description: Uso de canales autenticados seguros
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows Media Administrador de dispositivos,authentication
- Administrador de dispositivos,autenticación
- aplicaciones de escritorio, autenticación
- proveedores de servicios, autenticación
- guía de programación, autenticación
- autenticación
- Windows Comunicación Administrador de dispositivos, segura
- Administrador de dispositivos comunicación segura
- aplicaciones de escritorio, comunicación segura
- proveedores de servicios, comunicación segura
- guía de programación, comunicación segura
- comunicación segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a86eb364baca933eea1c81e587f99c9381786c5c3f62f2cefcfe3ceaed6e51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124115"
---
# <a name="using-secure-authenticated-channels"></a>Uso de canales autenticados seguros

Windows Media Administrador de dispositivos permite la autenticación y la comunicación segura entre componentes al proporcionar dos clases auxiliares, [CSecureChannelClient](csecurechannelclient-class.md) (para aplicaciones) y [CSecureChannelServer](csecurechannelserver-class.md) (para proveedores de servicios) y una interfaz, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (para ambos). Juntos, son una API para el uso de canales autenticados seguros (SAC). SAC controla las tres tareas siguientes para proveedores de servicios o aplicaciones que usan Windows Media Administrador de dispositivos:

-   [Autenticación de componentes](component-authentication.md)
-   [Cifrado y descifrado](encryption-and-decryption.md)
-   [Autenticación de mensajes](message-authentication.md)

Una aplicación o proveedor de servicios debe controlar la autenticación, el cifrado y el descifrado de componentes. la autenticación de mensajes es opcional.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tareas comunes para aplicaciones y proveedores de servicios**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




