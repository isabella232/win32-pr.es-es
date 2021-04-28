---
description: Control de versiones del sistema operativo
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Control de versiones del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2b8c60994eaee7a3becfa9acc03fe2c61fb12
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088043"
---
# <a name="operating-system-versioning"></a>Control de versiones del sistema operativo

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

**Gravedad:** alta  
**Frecuencia:** alta  









## <a name="description"></a>Descripción

El número de versión interno para Windows 7 y Windows Server 2008 R2 es 6.1. La función GetVersion devolverá ahora este número de versión a las aplicaciones cuando se consulta. Esto es especialmente importante para antivirus, copia de seguridad, aplicaciones de utilidad y protección de copia.

## <a name="manifestation-of-impact"></a>Demostración de impacto

La expresión de este cambio es específica de la aplicación. Esto significa que cualquier aplicación que comprueba específicamente la versión del sistema operativo recibirá un número de versión mayor, lo que puede dar lugar a una o varias de las situaciones siguientes:

-   Es posible que los instaladores de aplicaciones no puedan instalar la aplicación y que las aplicaciones no puedan iniciarse.
-   Las aplicaciones pueden volverse inestables o bloquearse
-   Las aplicaciones pueden generar mensajes de error, pero siguen funcionando correctamente

## <a name="mitigation"></a>Mitigación

La mayoría de las aplicaciones funcionarán correctamente en Windows 7 y Windows Server 2008 R2 porque la compatibilidad de aplicaciones en Windows 7 y Windows Server 2008 R2 es muy alta. Sin embargo, Windows 7 y Windows Server 2008 R2 incluyen un Vista de compatibilidad para instaladores y aplicaciones que comprueban la versión del sistema operativo.

Para habilitar la vista de compatibilidad, los usuarios pueden hacer clic con el botón derecho en el acceso directo o en el archivo ejecutable y, a continuación, aplicar el Vista de compatibilidad Windows XP SP2 o Windows Vista desde la pestaña Compatibilidad. En la mayoría de los casos, esto debería permitir que la aplicación funcione correctamente sin necesidad de realizar ningún cambio en la aplicación.

Los profesionales de TI también pueden aplicar cualquiera de las correcciones de compatibilidad de VersionLie aplicables, mediante la herramienta Administrador de compatibilidad, que se instala con Application Compatibility Toolkit (ACT). Por ejemplo, si una aplicación no funciona porque está comprobando, pero no buscando, la información de la versión de Windows XP® con Service Pack 2 (SP2), se puede aplicar WinXPSP2VersionLie para devolver la información de número de versión adecuada a la aplicación, independientemente de la versión real del sistema operativo que se ejecute en el equipo. Las correcciones de compatibilidad de VersionLie disponibles son:

-   Win95VersionLie
-   Win98VersionLie
-   WinNT4SP5VersionLie
-   Win2000VersionLie
-   Win2000SP1VersionLie
-   Win2000SP2VersionLie
-   Win2000SP3VersionLie
-   WinXPVersionLie
-   WinXPSP1VersionLie
-   WinXPSP2VersionLie
-   VistaRTMVersionLie
-   VistaSP1VersionLie
-   VistaSP2VersionLie
-   Win2K3RTMVersionLie
-   Win2K3SP1VersionLie

## <a name="solution"></a>Solución

Por lo general, las aplicaciones no deben realizar comprobaciones de versión del sistema operativo. Si una aplicación necesita una característica específica, es preferible intentar encontrarla y producir un error solo si falta la característica necesaria. Como mínimo, las aplicaciones siempre deben aceptar números de versión mayores o iguales que la versión más baja admitida del sistema operativo. Las excepciones solo deben producirse si hay un requisito legal, empresarial o de componente del sistema específico.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Descarga del kit de herramientas de compatibilidad de aplicaciones](/windows-hardware/get-started/adk-install)
-   [Correcciones de compatibilidad conocidas, modos de compatibilidad y mensajes de AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))

 

 
