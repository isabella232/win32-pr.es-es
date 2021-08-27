---
title: Llamadas de procedimiento remoto con RPC sobre HTTP
description: Los programas de explorador de Internet normalmente emplean el Protocolo de transporte de hipertexto (HTTP) como medio principal para examinar el World Wide Web.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- Procedimiento remoto Llame a RPC , tareas, mediante RPC/http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fedeb1700d798a616d3441b356f6f31867eed0399f412ed1f82923bcc4ac5f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101665"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a>Llamadas de procedimiento remoto con RPC sobre HTTP

Los programas de explorador de Internet normalmente emplean el Protocolo de transporte de hipertexto (HTTP) como medio principal para examinar el World Wide Web. Por lo tanto, HTTP ve un uso amplio en la mayoría de los equipos en la actualidad. Microsoft ha ampliado las funcionalidades de Su Servidor de Internet Information Server (IIS) para proporcionar servicios de llamada a procedimientos remotos mediante HTTP.

La implementación de RPC sobre HTTP de Microsoft (RPC sobre HTTP) permite a los clientes RPC conectarse de forma segura y eficaz a través de Internet a programas de servidor RPC y ejecutar llamadas a procedimientos remotos. Esto se logra con la ayuda de un intermediario conocido como el proxy RPC sobre HTTP o simplemente el proxy RPC.

El proxy RPC se ejecuta en un equipo IIS. Acepta solicitudes RPC procedentes de Internet, realiza comprobaciones de autenticación, validación y acceso en esas solicitudes y, si la solicitud pasa todas las pruebas, el proxy RPC reenvía la solicitud al servidor RPC que realiza el procesamiento real. Con RPC a través de HTTP, el cliente y el servidor RPC no se comunican directamente; en su lugar, usan el proxy RPC como intermediario. Este modelo se eligió por muchas razones. Para obtener más información, vea [RPC sobre seguridad HTTP.](rpc-over-http-security.md)

En esta sección se proporciona información general sobre RPC a través de HTTP en los temas siguientes:

-   [Usar HTTP como transporte RPC](using-http-as-an-rpc-transport.md)
-   [RPC sobre seguridad HTTP](rpc-over-http-security.md)
-   [Requisitos del sistema e interoperabilidad para RPC a través de HTTP](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [Configuración de equipos para RPC a través de HTTP](configuring-computers-for-rpc-over-http.md)
-   [Rpc a través de http Deployment Recomendaciones](rpc-over-http-deployment-recommendations.md)

Para obtener información sobre los escenarios de RPC a través de HTTP de gran volumen, consulte Equilibrio de [carga de RPC de Microsoft](rpc-load-balancing.md).

 

 




