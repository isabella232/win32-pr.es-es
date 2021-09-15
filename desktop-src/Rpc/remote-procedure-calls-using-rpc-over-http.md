---
title: Llamadas de procedimiento remoto con RPC sobre HTTP
description: Los programas de explorador de Internet normalmente emplean el Protocolo de transporte de hipertexto (HTTP) como medio principal para examinar el World Wide Web.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- Llamada a procedimiento remoto RPC , tareas, mediante RPC/http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c84551500af712b1126d8f9a65cb3d02eba8c9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473619"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a>Llamadas de procedimiento remoto con RPC sobre HTTP

Los programas de explorador de Internet normalmente emplean el Protocolo de transporte de hipertexto (HTTP) como medio principal para examinar el World Wide Web. Http, por lo tanto, ve un uso amplio en la mayoría de los equipos en la actualidad. Microsoft ha ampliado las funcionalidades de Su Servidor de Internet Information Server (IIS) para proporcionar servicios de llamada a procedimiento remoto mediante HTTP.

La implementación de RPC sobre HTTP de Microsoft (RPC a través de HTTP) permite a los clientes rpc conectarse de forma segura y eficaz a través de Internet a programas de servidor RPC y ejecutar llamadas a procedimiento remoto. Esto se logra con la ayuda de un intermediario conocido como el proxy RPC sobre HTTP o simplemente el proxy RPC.

El proxy RPC se ejecuta en un equipo IIS. Acepta solicitudes RPC procedentes de Internet, realiza comprobaciones de autenticación, validación y acceso en esas solicitudes y, si la solicitud supera todas las pruebas, el proxy RPC reenvía la solicitud al servidor RPC que realiza el procesamiento real. Con RPC a través de HTTP, el cliente y el servidor RPC no se comunican directamente; en su lugar, usan el proxy RPC como intermediario. Este modelo se eligió por muchas razones. Para obtener más información, vea [RPC sobre seguridad HTTP.](rpc-over-http-security.md)

En esta sección se proporciona información general sobre RPC a través de HTTP en los temas siguientes:

-   [Uso de HTTP como transporte RPC](using-http-as-an-rpc-transport.md)
-   [Seguridad de RPC a través de HTTP](rpc-over-http-security.md)
-   [Requisitos del sistema e interoperabilidad para RPC a través de HTTP](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [Configuración de equipos para RPC a través de HTTP](configuring-computers-for-rpc-over-http.md)
-   [Rpc a través de la implementación de HTTP Recomendaciones](rpc-over-http-deployment-recommendations.md)

Para obtener información sobre escenarios de RPC a través de HTTP de gran volumen, consulte [Equilibrio de carga de RPC de Microsoft.](rpc-load-balancing.md)

 

 




