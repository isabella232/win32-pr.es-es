---
title: Llamadas de procedimiento remoto con RPC sobre HTTP
description: Los programas del explorador de Internet suelen emplear el protocolo de transporte de hipertexto (HTTP) como medio principal de examinar el World Wide Web.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- RPC llamada a procedimiento remoto, tareas, uso de RPC/http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c84551500af712b1126d8f9a65cb3d02eba8c9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993823"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a>Llamadas de procedimiento remoto con RPC sobre HTTP

Los programas del explorador de Internet suelen emplear el protocolo de transporte de hipertexto (HTTP) como medio principal de examinar el World Wide Web. HTTP, por lo tanto, ve un uso extensivo en la mayoría de los equipos de hoy en día. Microsoft ha extendido las capacidades de su servidor de Internet Information Server (IIS) para proporcionar servicios de llamada a procedimiento remoto mediante HTTP.

La implementación de RPC a través de HTTP (RPC a través de HTTP) de Microsoft permite a los clientes RPC conectarse de forma segura y eficaz a través de Internet a programas de servidor RPC y ejecutar llamadas a procedimientos remotos. Esto se consigue con la ayuda de un intermediario conocido como el proxy RPC a través de HTTP o simplemente el proxy RPC.

El proxy RPC se ejecuta en un equipo de IIS. Acepta solicitudes RPC procedentes de Internet, realiza comprobaciones de autenticación, validación y acceso en esas solicitudes, y si la solicitud supera todas las pruebas, el proxy RPC reenvía la solicitud al servidor RPC que realiza el procesamiento real. Con RPC a través de HTTP, el cliente RPC y el servidor no se comunican directamente; en su lugar, usan el proxy RPC como intermediario. Este modelo se eligió por muchas razones. Para obtener más información, vea [seguridad de RPC a través de http](rpc-over-http-security.md).

En esta sección se proporciona información general sobre RPC a través de HTTP en los temas siguientes:

-   [Usar HTTP como transporte RPC](using-http-as-an-rpc-transport.md)
-   [Seguridad de RPC a través de HTTP](rpc-over-http-security.md)
-   [Requisitos del sistema e interoperabilidad de RPC a través de HTTP](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [Configuración de equipos para RPC a través de HTTP](configuring-computers-for-rpc-over-http.md)
-   [Recomendaciones de implementación de RPC sobre HTTP](rpc-over-http-deployment-recommendations.md)

Para obtener información sobre escenarios de RPC a través de HTTP de gran volumen, consulte [equilibrio de carga de Microsoft RPC](rpc-load-balancing.md).

 

 




