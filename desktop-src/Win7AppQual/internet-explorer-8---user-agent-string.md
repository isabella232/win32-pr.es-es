---
description: .
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8-cadena de agente de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aea44572f32e252a4e1d4dc2209e411834c12d4
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314798"
---
# <a name="internet-explorer-8---user-agent-string"></a>Internet Explorer 8-cadena de agente de usuario

## <a name="affected-platforms"></a>Plataformas afectadas

 **Clientes** : Windows XP, Windows Vista, Windows 7  
**Servidores** : windows Server 2003, windows Server 2008, windows Server 2008 R2  










## <a name="feature-impact"></a>Impacto en las características

**Gravedad** : medio  
**Frecuencia** : alta  











## <a name="description"></a>Descripción

La cadena de agente de usuario es el identificador de Internet Explorer que proporciona datos sobre su versión y otros atributos a los servidores Web. Muchas aplicaciones web se basan en la cadena de agente de usuario de IE y se superponer en ella. Los que lo hacen y dependen de un número de versión anterior se verán afectados. La cadena de agente de usuario ahora incluye la cadena ' Trident/4.0 ' para permitir la diferencia entre la cadena de agente de usuario de Internet Explorer 7 y la cadena de agente de usuario de Internet Explorer 8 cuando se ejecuta en la vista de compatibilidad de Internet Explorer 7. Consulte Descripción de las cadenas de agente de usuario para más información.

## <a name="manifestation-of-impact"></a>Manifiesto de impacto

Hay dos áreas afectadas:

-   Es posible que las páginas web que comprueben explícitamente la cadena de agente de usuario y no admitan la cadena de agente de usuario de Internet Explorer 8 no se ejecuten correctamente. En la mayoría de los casos, esto significa que las páginas bloquearán a los usuarios el contenido al que intentan acceder o que muestren contenido incorrecto o con formato incorrecto.
-   Las aplicaciones que hospedan Trident (consulte hospedaje y reutilización) tendrán como valor predeterminado Internet Explorer 7 mediante el componente opcional Web, pero no tendrán acceso a las características de Internet Explorer 8.

## <a name="solution"></a>Solución

Asegúrese de que las aplicaciones controlan correctamente la nueva versión de "MSIE 8,0" en la cadena de agente de usuario. También puede optar por la vista de compatibilidad de Internet Explorer 7 para esas aplicaciones basadas en Internet Explorer 7. Esto puede hacerse con etiquetas meta. Consulte la explicación de descripción de las cadenas de agente de usuario para más información.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

-   Ejecute las aplicaciones y las páginas web en un entorno de Internet Explorer 8 en Windows Vista o Windows XP para asegurarse de que se comportan de la manera deseada.
-   Como alternativa, puede ejecutar la herramienta de prueba de compatibilidad de Internet Explorer (IECTT) que se proporciona con el kit de herramientas de compatibilidad de aplicaciones (ACT) para localizar cualquier posible problema debido a las actualizaciones de las características de seguridad.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Descripción de las cadenas de agente de usuario](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))
-   [Cadena de User-Agent de Internet Explorer 8](/archive/blogs/ie/)
-   [Vector de versión y cadena de agente de usuario](https://archive.msdn.microsoft.com/ie8whitepapers)
-   [Hospedaje y reutilización](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))
-   [Descarga del kit de herramientas de compatibilidad de aplicaciones](/windows-hardware/get-started/adk-install)
-   [Problemas conocidos de la característica de seguridad de Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
