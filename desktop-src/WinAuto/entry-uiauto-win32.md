---
title: Automatización de la interfaz de usuario
description: Microsoft Automatización de la interfaz de usuario es un marco de accesibilidad que permite a las Windows proporcionar y consumir información mediante programación sobre interfaces de usuario (URI).
ms.assetid: 700ca38d-ff40-472b-a95a-11fa94c3bc1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55951bf103906aace627a03ab84557d6a555aa793f1e0cec7ff2c81598e71558
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071835"
---
# <a name="ui-automation"></a>Automatización de la interfaz de usuario

Microsoft Automatización de la interfaz de usuario es un marco de accesibilidad que permite a las Windows proporcionar y consumir información mediante programación sobre interfaces de usuario (URI). Proporciona acceso mediante programación a la mayoría de los elementos de la interfaz de usuario en el escritorio. Permite que los productos de tecnología de asistencia, como los lectores de pantalla, proporcionen información sobre la interfaz de usuario a los usuarios finales y manipulen la interfaz de usuario por medios distintos de la entrada estándar. Automatización de la interfaz de usuario también permite que los scripts de prueba automatizados interactúen con la interfaz de usuario.

-   [Cuando proceda](#where-applicable)
-   [Audiencia para desarrolladores](#developer-audience)
-   [Requisitos en tiempo de ejecución](#run-time-requirements)
-   [Compatibilidad con sistemas operativos de nivel inferior](#support-for-down-level-operating-systems)

## <a name="where-applicable"></a>Dónde se puede aplicar

Mediante el Automatización de la interfaz de usuario y los procedimientos de diseño accesibles, los desarrolladores pueden hacer que las aplicaciones que se ejecutan en Windows sea más accesible para muchas personas con discapacidades de visión, de oído o de movimiento. Además, Automatización de la interfaz de usuario está diseñado específicamente para proporcionar una funcionalidad sólida para escenarios de pruebas automatizadas.

## <a name="developer-audience"></a>Audiencia de los desarrolladores

Automatización de la interfaz de usuario está diseñado para desarrolladores experimentados de C/C++. En general, los desarrolladores necesitan un nivel moderado de comprensión sobre los objetos e interfaces del Modelo de objetos componentes (COM), Unicode y Windows API.

Para obtener información sobre Automatización de la interfaz de usuario código administrado, consulte [Accesibilidad](/dotnet/framework/ui-automation/) en la .NET Framework guía del desarrollador de MSDN.

## <a name="run-time-requirements"></a>Requisitos del tiempo de ejecución

Automatización de la interfaz de usuario se admite en los siguientes sistemas operativos: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016 y Windows Server 2019.

> [!Note]  
> Windows XP y Windows Server 2003 también requieren Microsoft .NET Framework 3.0.

 

## <a name="support-for-down-level-operating-systems"></a>Compatibilidad con sistemas operativos de nivel inferior

La actualización de plataforma para Windows Vista es un conjunto de bibliotecas en tiempo de ejecución que permite a los desarrolladores dirigir las aplicaciones a sistemas operativos de Windows 7 y de nivel inferior. La actualización de plataforma para Windows Server 2008 es un conjunto de bibliotecas en tiempo de ejecución que permite a los desarrolladores dirigir aplicaciones a Windows Server 2008 R2 y versiones anteriores de Windows Server. La actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008 estarán disponibles para todos los clientes de Windows Vista y Windows Server 2008 a través de Windows Update. Las aplicaciones de terceros que requieren Actualización de plataforma para Windows Vista o Actualización de plataforma para Windows Server 2008 pueden hacer que Windows Update detecte si está instalada; Si no es así, Windows Update la descargará e instalará en segundo plano.

La actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008 admiten toda la característica de Windows Automation API 3.0 establecida en los siguientes sistemas operativos.

-   Windows XP (inglés) <dl> Windows XP Home SP3 x86  
    Windows XP Professional SP3 x86  
    </dl>
-   Windows Server 2003 (English) <dl> Windows Server 2003 SP2 (x86 y x64)  
    </dl>
-   Windows Vista (inglés) <dl> Starter SP2 (x86 y x64)  
    Inicio Premium SP2 (x86 y x64)  
    Business SP2 (x86 y x64)  
    Enterprise SP2 (x86 y x64)  
    Ultimate SP2 (x86 y x64)  
    </dl>
-   Windows Server 2008 (inglés) <dl> Windows Server 2008 SP2 (x86 y x64)  
    </dl>

Para obtener más información sobre ambas actualizaciones, vea [Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).

## <a name="in-this-section"></a>En esta sección

-   [Fundamentos de UI Automation](entry-uiautocore-overview.md)
-   [Automatización de la interfaz de usuario del programador del proveedor de servicios](uiauto-providerportal.md)
-   [Automatización de la interfaz de usuario guía del programador de cliente](uiauto-clientportal.md)
-   [Referencia](entry-uiautocore-ref.md)
-   [Ejemplos](samples-entry.md)
-   [Apéndices](appendix-entry.md)

 

 