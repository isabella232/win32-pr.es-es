---
title: Extensiones de servidor de directivas de redes
description: La API de extensiones de NPS permite a los desarrolladores de software escribir archivos dll de extensión que se pueden usar para la autenticación, la autorización y las cuentas. La API de extensiones de NPS es compatible con el protocolo Servicio de autenticación remota telefónica de usuario (RADIUS).
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd6f9bd0be7479726110b41d6060a7e5c836bb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995482"
---
# <a name="network-policy-server-extensions"></a>Extensiones de servidor de directivas de redes

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.

 

La API de extensiones de NPS permite a los desarrolladores de software escribir archivos dll de extensión que se pueden usar para la autenticación, la autorización y las cuentas. La API de extensiones de NPS es compatible con el protocolo Servicio de autenticación remota telefónica de usuario (RADIUS).

Los archivos dll de extensión que se implementan mediante la API de extensiones de NPS pueden proporcionar control de sesión y contabilidad mejorados. Estos archivos DLL se pueden usar para escenarios como el control del número de sesiones de red de usuario final, el uso de un servidor de estado y la conexión a bases de datos de autenticación de dominio y servicios de Active Directory. Los archivos dll de extensión pueden expandir las autorizaciones de acceso remoto proporcionadas por NPS agregando sus propias autorizaciones al enviar una respuesta de aceptación de nuevo a un cliente de autenticación.

La API de extensiones de NPS es aplicable en cualquier entorno informático en el que pueda mejorar la eficacia para autenticar a los usuarios de acceso telefónico a través de un servidor remoto. Esta tecnología es especialmente útil para los proveedores de servicios de Internet (ISP).

## <a name="in-this-section"></a>En esta sección

[Información general](/windows/desktop/Nps/ias-about-internet-authentication-service)

Información general sobre RADIUS y la API de extensiones de NPS.

[Utilizan](/windows/desktop/Nps/ias-using-internet-authentication-service)

Código de ejemplo que muestra cómo usar la API de extensiones de NPS.

[Referencia](/windows/desktop/Nps/ias-internet-authentication-service-reference)

Documentación de tipos enumerados, funciones y estructuras que componen la API de extensiones de NPS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servidor de directivas de redes (servicio de autenticación de Internet)](portal.md)
</dt> <dt>

[Protocolo de autenticación extensible (EAP)](../eap/eap-start-page.md)
</dt> </dl>

 

 