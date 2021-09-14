---
title: Extensiones del servidor de directivas de red
description: NpS Extensions API permite a los desarrolladores de software escribir archivos DLL de extensión que se pueden usar para la autenticación, autorización y contabilidad. NPS Extensions API admite el protocolo Servicio de autenticación remota telefónica de usuario (RADIUS).
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd6f9bd0be7479726110b41d6060a7e5c836bb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071518"
---
# <a name="network-policy-server-extensions"></a>Extensiones del servidor de directivas de red

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS) a partir Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.

 

NpS Extensions API permite a los desarrolladores de software escribir archivos DLL de extensión que se pueden usar para la autenticación, autorización y contabilidad. NPS Extensions API admite el protocolo Servicio de autenticación remota telefónica de usuario (RADIUS).

Los archivos DLL de extensión implementados mediante la API de extensiones de NPS pueden proporcionar control de sesión y contabilidad mejorados. Estos archivos DLL se pueden usar para escenarios como el control del número de sesiones de red del usuario final, el uso de un servidor de estado y la conexión a bases de datos de autenticación de dominio Active Directory servicios. Los archivos DLL de extensión pueden expandir las autorizaciones de acceso remoto proporcionadas por NPS agregando sus propias autorizaciones al enviar una respuesta Accept de vuelta a un cliente de autenticación.

NPS Extensions API es aplicable en cualquier entorno informático donde mejoraría la eficacia para autenticar a los usuarios de acceso telefónico a través de un servidor remoto. Esta tecnología es especialmente útil para los proveedores de servicios de Internet (ISP).

## <a name="in-this-section"></a>En esta sección

[Información general](/windows/desktop/Nps/ias-about-internet-authentication-service)

Información general sobre RADIUS y la API de extensiones nps.

[Usando](/windows/desktop/Nps/ias-using-internet-authentication-service)

Código de ejemplo que muestra cómo usar la API de extensiones de NPS.

[Referencia](/windows/desktop/Nps/ias-internet-authentication-service-reference)

Documentación de tipos enumerados, funciones y estructuras que componen la API de extensiones nps.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servidor de directivas de red (Servicio de autenticación de Internet)](portal.md)
</dt> <dt>

[Protocolo de autenticación extensible (EAP)](../eap/eap-start-page.md)
</dt> </dl>

 

 