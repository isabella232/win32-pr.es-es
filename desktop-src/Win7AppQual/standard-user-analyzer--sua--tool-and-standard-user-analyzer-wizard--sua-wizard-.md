---
description: Aprenda a usar la herramienta Analizador de usuarios estándar (SUA) y el Asistente de SUA para probar las aplicaciones y detectar posibles problemas de compatibilidad.
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: Herramienta Analizador de usuario estándar (SUA) y Asistente para Analizador de usuario estándar (Asistente para SUA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fa9329f2f42dd8fc3b948388ef44948deca052a919ca50704cbccedc83fca84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994684"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a>Herramienta Analizador de usuario estándar (SUA) y Asistente para Analizador de usuario estándar (Asistente para SUA)

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows XP, Windows Vista, Windows 7  
**Servidores:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  

## <a name="description"></a>Descripción

La compatibilidad de Toolkit incluye la herramienta Analizador de usuarios estándar (SUA) y el Asistente para analizadores de usuarios estándar (Asistente para SUA). Estas herramientas le permiten probar las aplicaciones y supervisar las llamadas API con el fin de detectar posibles problemas de compatibilidad debido a la característica control de cuentas de usuario (UAC) en el sistema operativo Windows 7.

UAC, anteriormente conocido como Cuenta de usuario limitada (LUA), requiere que todos los usuarios (incluidos los miembros del grupo Administrador) se ejecuten como usuarios estándar mediante el cuadro de diálogo del símbolo del sistema de seguridad hasta que la aplicación se eleva deliberadamente. Sin embargo, las aplicaciones que requieren acceso y privilegios para las ubicaciones que no están disponibles para un usuario estándar no se pueden ejecutar correctamente con el rol Usuario estándar.

## <a name="usage"></a>Uso

En las secciones siguientes se proporciona información detallada sobre cómo usar las herramientas del Asistente para SUA y SUA.

**Herramienta SUA**

La herramienta SUA permite analizar una aplicación, revisar un informe detallado sobre los problemas relacionados con UAC y, a continuación, aplicar las mitigaciones de aplicaciones sugeridas y seleccionadas, como se muestra en el diagrama de flujo siguiente.

![Diagrama que muestra el flujo de la herramienta S U A.](images/act-suaflowchart-appcookbook.gif)

*Herramienta SUA y virtualización*

Solo la herramienta SUA le permite activar y desactivar la característica de virtualización. Al desactivar la característica de virtualización, la aplicación probada se comportará más como cuando funciona en el Windows operativo XP.

*Herramienta SUA y privilegios elevados*

Solo la herramienta SUA le permite activar y desactivar la característica **Iniciar con privilegios** elevados. La característica Iniciar con privilegios elevados permite que la aplicación seleccionada se ejecute como administrador o como usuario estándar. En función de la selección, encontrará diferentes tipos de problemas relacionados con UAC. Si activa la casilla **Iniciar** con privilegios elevados, la aplicación se ejecutará con privilegios de administrador completos, lo que permite a SUA predecir los problemas que pueden producirse para un usuario estándar. Si selecciona la casilla Iniciar con privilegios elevados, verá los errores resultantes de la aplicación que se está ejecutando y generando errores.

**Asistente de SUA**

El Asistente para SUA le permite seguir un proceso guiado y paso a paso por el que puede analizar una aplicación y, a continuación, aplicar las mitigaciones de aplicaciones sugeridas y seleccionadas, como se muestra en el siguiente diagrama de flujo. A diferencia de la herramienta SUA, el asistente no permite revisar los problemas detallados relacionados con UAC.

![Diagrama que muestra el flujo del Asistente de S U A.](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Compatibilidad de aplicaciones Toolkit descarga](/windows-hardware/get-started/adk-install)
-   [Descripción de las herramientas del analizador de usuarios estándar](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))
-   [Referencia técnica del Analizador de usuarios estándar](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))
-   [Prueba y mitigación de problemas mediante las herramientas de desarrollo](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))
-   [Compatibilidad de aplicaciones y control de cuentas de usuario](/previous-versions/windows/)

> [!Note]  
> Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.

 

 

 
