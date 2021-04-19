---
description: .
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: 'Internet Explorer 8: protección de ejecución de datos/NX'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc73fcd70a244288aceaead426bf09f07656740d
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314778"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a>Internet Explorer 8: protección de ejecución de datos/NX

## <a name="affected-platforms"></a>Plataformas afectadas

 **Clientes** : Windows XP, Windows Vista, Windows 7  
**Servidores** : windows Server 2003, windows Server 2008, windows Server 2008 R2  










> [!Note]  
> Internet Explorer 8 habilitará la protección de DEP/NX cuando se ejecute en un sistema operativo con la Service Pack más reciente. Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1 y Windows Server 2008 tienen DEP/NX habilitado de forma predeterminada en Internet Explorer 8.

 

## <a name="feature-impact"></a>Impacto en las características

**Gravedad** : medio  
**Frecuencia** : baja  

> [!Note]  
> Normalmente, cualquier aplicación que se ejecute en Internet Explorer y que no sea compatible con DEP/NX se bloqueará al iniciarse y no funcionará. Es posible que Internet Explorer se bloquee al iniciar si se instalan complementos que no son compatibles con DEP/NX.

 

## <a name="description"></a>Descripción

DEP/NX es una característica de seguridad que ayuda a mitigar las vulnerabilidades relacionadas con la memoria. A partir de Internet Explorer 8, todos los procesos de Internet Explorer habilitan la característica DEP/NX de forma predeterminada.

## <a name="manifestation-of-impact"></a>Manifiesto de impacto

El kernel de Windows supervisa la ejecución de un programa. Si el kernel detecta un intento de ejecutar código desde una página de memoria que no está marcada como ejecutable, el kernel detiene la ejecución del programa, lo que produce un "bloqueo". Se trata de una medida de seguridad que ayuda a garantizar que las vulnerabilidades relacionadas con la memoria (por ejemplo, desbordamientos del búfer) en la aplicación no se puedan aprovechar para ejecutar código arbitrario.

## <a name="end-user-mitigation"></a>Mitigación de End-User

-   Instale una versión posterior del complemento o marco que sea compatible con DEP/NX.
-   Ejecute Internet Explorer con privilegios elevados como administrador y, a continuación, deshabilite DEP/NX mediante la casilla **Habilitar protección de memoria para ayudar a mitigar los ataques en línea** en la pestaña **Opciones**  /  **avanzadas** de Internet.

## <a name="developer-solution"></a>Solución para desarrolladores

Compile aplicaciones con las versiones más recientes de los marcos de trabajo compatibles con DEP.

## <a name="leveraging-feature-capabilities"></a>Aprovechar las capacidades de características

-   Use la opción del vinculador/NXCOMPAT para indicar la compatibilidad de DEP/NX
-   Opte por su código en otras defensas disponibles, como la defensa de pila (/GS), el control de excepciones seguro (/SafeSEH) y ASLR (/DynamicBase)

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

-   Pruebe el código con DEP/NX habilitado mediante la última versión de Internet Explorer Publicada en Windows Vista SP1 o posterior.
-   Pruebe con Internet Explorer 7 en Windows Vista después de habilitar la opción DEP/NX. Para habilitar DEP/NX para Internet Explorer 7, ejecute Internet Explorer como administrador y, después, active la casilla correspondiente en la pestaña Herramientas > opciones de Internet > avanzadas.
-   Ejecute la herramienta de prueba de compatibilidad de Internet Explorer (IECTT), que se proporciona con el kit de herramientas de compatibilidad de aplicaciones (ACT) para localizar cualquier posible problema debido a los cambios de DEP/NX.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Internet Explorer 8 Security Part I: protección de memoria de DEP/NX](/archive/blogs/ie/)
-   [Prevención de ejecución de datos](../memory/data-execution-prevention.md)
-   [Nuevas API de NX agregadas a Windows Vista SP1, Windows XP SP3 y Windows Server 2008 R2](/archive/blogs/michael_howard/)
-   [Descarga del kit de herramientas de compatibilidad de aplicaciones](/windows-hardware/get-started/adk-install)
-   [Problemas conocidos de la característica de seguridad de Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
