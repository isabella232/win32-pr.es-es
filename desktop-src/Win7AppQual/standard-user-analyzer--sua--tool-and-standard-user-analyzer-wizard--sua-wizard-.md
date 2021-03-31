---
description: Aprenda a usar la herramienta de analizador de usuario estándar (SUA) y el Asistente de SUA para probar sus aplicaciones y detectar posibles problemas de compatibilidad.
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: Herramienta Analizador de usuario estándar (SUA) y Asistente para Analizador de usuario estándar (Asistente para SUA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc0e729c37ff1650f0dab7f3dd1c05ffb4b5f370
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104083528"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a>Herramienta Analizador de usuario estándar (SUA) y Asistente para Analizador de usuario estándar (Asistente para SUA)

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows XP Windows \| vista Windows \| 7  
**Servidores:** Windows Server 2003 \| Windows server 2008 \| windows Server 2008 R2  

## <a name="description"></a>Descripción

El kit de herramientas de compatibilidad de aplicaciones incluye la herramienta analizador de usuario estándar (SUA) y el Asistente para el analizador de usuarios estándar (Asistente para SUA). Estas herramientas le permiten probar sus aplicaciones y supervisar las llamadas de API para detectar posibles problemas de compatibilidad debido a la característica control de cuentas de usuario (UAC) en el sistema operativo Windows 7.

UAC, anteriormente conocido como cuenta de usuario limitada (LUA), requiere que todos los usuarios (incluidos los miembros del grupo de administradores) se ejecuten como usuarios estándar mediante el cuadro de diálogo de mensaje de seguridad hasta que la aplicación se haya elevado deliberadamente. Sin embargo, las aplicaciones que requieren acceso y privilegios para ubicaciones que no están disponibles para un usuario estándar no se pueden ejecutar correctamente con el rol de usuario estándar.

## <a name="usage"></a>Uso

En las secciones siguientes se proporciona información detallada sobre cómo usar las herramientas del asistente SUA y SUA.

**Herramienta SUA**

La herramienta SUA le permite analizar una aplicación, revisar un informe detallado sobre los problemas relacionados con UAC y, a continuación, aplicar las mitigaciones de la aplicación sugerida y seleccionada, tal como se muestra en el siguiente diagrama de flujo.

![Diagrama que muestra el flujo de la herramienta S U A.](images/act-suaflowchart-appcookbook.gif)

*Herramienta SUA y virtualización*

Solo la herramienta SUA permite activar y desactivar la característica de virtualización. Al desactivar la característica de virtualización, la aplicación comprobada se comportará de la misma manera que cuando funciona en el sistema operativo Windows XP.

*Herramienta SUA y privilegios elevados*

Solo la herramienta SUA permite activar y desactivar la característica de **Inicio elevado** . La característica de inicio elevado permite que la aplicación seleccionada se ejecute como administrador o como usuario estándar. En función de la selección, se localizarán diferentes tipos de problemas relacionados con UAC. Si desactiva la casilla **iniciar con privilegios elevados** , la aplicación se ejecutará con privilegios de administrador completos, lo que permite que sua prediga los problemas que pueden producirse para un usuario estándar. Si activa la casilla iniciar con privilegios elevados, verá los errores resultantes de la aplicación que se ejecuta realmente y que generan errores.

**Asistente para SUA**

El Asistente para SUA le permite seguir un proceso guiado paso a paso por el que puede analizar una aplicación y, a continuación, aplicar las mitigaciones de la aplicación sugerida y seleccionada, tal como se muestra en el siguiente diagrama de flujo. A diferencia de la herramienta SUA, el asistente no permite revisar los problemas detallados relacionados con UAC.

![Diagrama que muestra el flujo del asistente S U A.](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Descarga del kit de herramientas de compatibilidad de aplicaciones](/windows-hardware/get-started/adk-install)
-   [Descripción de las herramientas del analizador de usuario estándar](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))
-   [Referencia técnica del analizador de usuario estándar](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))
-   [Prueba y mitigación de problemas con las herramientas de desarrollo](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))
-   [Compatibilidad de aplicaciones y control de cuentas de usuario](/previous-versions/windows/)

> [!Note]  
> Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.

 

 

 
