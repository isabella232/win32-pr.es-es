---
description: Internet Explorer 8- Protección de ejecución de datos/NX
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8- Protección de ejecución de datos/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb0208cc20e78c30f42b09af78460990be20b002
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253257"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a>Internet Explorer 8- Protección de ejecución de datos/NX

## <a name="affected-platforms"></a>Plataformas afectadas

 **Clientes:** Windows XP, Windows Vista, Windows 7  
**Servidores:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










> [!Note]  
> Internet Explorer 8 habilitará la protección DEP/NX cuando se ejecute en un sistema operativo con el Service Pack más reciente. Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1 y Windows Server 2008 tienen DEP/NX habilitado de forma predeterminada en Internet Explorer 8.

 

## <a name="feature-impact"></a>Impacto en las características

**Gravedad:** media  
**Frecuencia:** baja  

> [!Note]  
> Normalmente, cualquier aplicación que se ejecute en Internet Explorer y no sea compatible con DEP/NX se bloqueará durante el inicio y no funcionará. Internet Explorer pueden bloquearse al iniciarse si están instalados complementos que no son compatibles con DEP/NX.

 

## <a name="description"></a>Descripción

DEP/NX es una característica de seguridad que ayuda a mitigar las vulnerabilidades relacionadas con la memoria. A partir Internet Explorer 8, todos los procesos Internet Explorer habilitan la característica DEP/NX de forma predeterminada.

## <a name="manifestation-of-impact"></a>Demostración del impacto

El Windows kernel supervisa la ejecución de un programa. Si el kernel detecta un intento de ejecutar código desde una página de memoria que no está marcada como ejecutable, el kernel detiene la ejecución del programa, lo que produce un "bloqueo". Se trata de una medida de seguridad que ayuda a garantizar que las vulnerabilidades relacionadas con la memoria (por ejemplo, desbordamientos de búfer) de la aplicación no se puedan aprovechar para ejecutar código arbitrario.

## <a name="end-user-mitigation"></a>End-User mitigación

-   Instale una versión posterior del complemento o del marco que sea compatible con DEP/NX.
-   Ejecute Internet Explorer con privilegios elevados como administrador y,  a continuación, deshabilite DEP/NX mediante la casilla Habilitar la protección de memoria para ayudar a mitigar los ataques en línea en la pestaña Opciones avanzadas de **Internet.**  /  

## <a name="developer-solution"></a>Solución para desarrolladores

Compile aplicaciones mediante las versiones más recientes de los marcos compatibles con DEP.

## <a name="leveraging-feature-capabilities"></a>Aprovechamiento de las funcionalidades de características

-   Use la opción del vinculador /NXCOMPAT para indicar la compatibilidad de DEP/NX.
-   Opte por el código en otras defensas disponibles, como la defensa de pila (/GS), el control seguro de excepciones (/SafeSEH) y ASLR (/DynamicBase).

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

-   Pruebe el código con DEP/NX habilitado mediante la versión Internet Explorer más reciente en Windows Vista SP1 o posterior.
-   Pruebe con Internet Explorer 7 en Windows Vista después de habilitar la opción DEP/NX. Para habilitar DEP/NX para Internet Explorer 7, ejecute Internet Explorer como administrador y, a continuación, establezca la casilla adecuada en la pestaña Herramientas > Opciones de Internet > avanzadas.
-   Ejecute Internet Explorer Compatibility Test Tool (IECTT), que se proporciona con application Compatibility Toolkit (ACT) para localizar los posibles problemas debidos a los cambios de DEP/NX.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Internet Explorer 8 Security Part I: DEP/NX Memory Protection](/archive/blogs/ie/)
-   [Prevención de ejecución de datos](../memory/data-execution-prevention.md)
-   [Nuevas API nx agregadas a Windows Vista SP1, Windows XP SP3 y Windows Server 2008 R2](/archive/blogs/michael_howard/)
-   [Descarga de compatibilidad de Toolkit aplicaciones](/windows-hardware/get-started/adk-install)
-   [Problemas conocidos Internet Explorer características de seguridad de seguridad](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
