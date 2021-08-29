---
description: 'Internet Explorer 8: cadena del agente de usuario'
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: 'Internet Explorer 8: cadena del agente de usuario'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8222dc199d8023b34d092b5b68fca90a93d1a00a6e41618ee3c8ee3897ef535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995015"
---
# <a name="internet-explorer-8---user-agent-string"></a>Internet Explorer 8: cadena del agente de usuario

## <a name="affected-platforms"></a>Plataformas afectadas

 **Clientes:** Windows XP, Windows Vista, Windows 7  
**Servidores:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










## <a name="feature-impact"></a>Impacto en las características

**Gravedad:** media  
**Frecuencia:** alta  











## <a name="description"></a>Descripción

La cadena del agente de usuario es el Internet Explorer que proporciona datos sobre su versión y otros atributos a los servidores web. Muchas aplicaciones web se basan y se basan en la cadena del agente de usuario de IE. Los que lo hagan y dependan de un número de versión anterior se verán afectados. La cadena del Agente de usuario ahora incluye la cadena "Trident/4.0" para permitir la diferenciación entre la cadena del agente de usuario de Internet Explorer 7 y la cadena del Agente de usuario de Internet Explorer 8 cuando se ejecuta en Internet Explorer 7 Vista de compatibilidad. Consulte Understanding User Agent Strings (Descripción de las cadenas del agente de usuario) para obtener más información.

## <a name="manifestation-of-impact"></a>Consecuencia del impacto

Hay dos áreas afectadas:

-   Es posible que las páginas web que comprueban explícitamente la cadena del agente de usuario y no admiten la cadena del agente de Internet Explorer 8 no se ejecuten correctamente. En la mayoría de los casos, esto significa que las páginas bloquearán a los usuarios del contenido al que intentan acceder o mostrarán contenido incorrecto o incorrecto.
-   Las aplicaciones que hospedan Trident (consulte Hospedaje y reutilización) tendrán como valor predeterminado Internet Explorer 7 mediante el componente opcional web, pero no tendrán acceso a Internet Explorer 8 características.

## <a name="solution"></a>Solución

Asegúrese de que las aplicaciones controlan correctamente la nueva versión "MSIE 8.0" en la cadena del agente de usuario. También puede participar en la aplicación Internet Explorer 7 Vista de compatibilidad para esas aplicaciones basadas en Internet Explorer 7. Esto se puede hacer con metaetiquetas. Consulte la explicación en Descripción de las cadenas del agente de usuario para obtener más información.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

-   Ejecute sus aplicaciones y páginas web en un entorno de Internet Explorer 8 en Windows Vista o Windows XP para asegurarse de que se comportan de la manera deseada.
-   Como alternativa, puede ejecutar la herramienta de prueba de compatibilidad de Internet Explorer (IECTT) que se proporciona con el Toolkit de compatibilidad de aplicaciones (ACT) para localizar los posibles problemas debidos a las actualizaciones de características de seguridad.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Descripción de las cadenas del agente de usuario](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))
-   [Internet Explorer 8 User-Agent String](/archive/blogs/ie/)
-   [Cadena de agente de usuario y vector de versión](https://archive.msdn.microsoft.com/ie8whitepapers)
-   [Hospedaje y reutilización](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))
-   [Compatibilidad de aplicaciones Toolkit descarga](/windows-hardware/get-started/adk-install)
-   [Problemas conocidos Internet Explorer características de seguridad](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
