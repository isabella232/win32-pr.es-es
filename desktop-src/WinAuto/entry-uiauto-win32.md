---
title: Automatización de la interfaz de usuario
description: La automatización de la interfaz de usuario de Microsoft es un marco de accesibilidad que permite que las aplicaciones Windows proporcionen y consuman información mediante programación sobre las interfaces de usuario (IUS).
ms.assetid: 700ca38d-ff40-472b-a95a-11fa94c3bc1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8006c79299cc1f736dc43555968443f634d4a51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904728"
---
# <a name="ui-automation"></a>Automatización de la interfaz de usuario

La automatización de la interfaz de usuario de Microsoft es un marco de accesibilidad que permite que las aplicaciones Windows proporcionen y consuman información mediante programación sobre las interfaces de usuario (IUS). Proporciona acceso mediante programación a la mayoría de los elementos de la interfaz de usuario en el escritorio. Permite productos de tecnología de asistencia, como lectores de pantalla, para proporcionar información sobre la interfaz de usuario a los usuarios finales y manipular la interfaz de usuario por medios distintos de la entrada estándar. UI Automation también permite que los scripts de pruebas automatizadas interactúen con la interfaz de usuario.

-   [Cuando proceda](#where-applicable)
-   [Audiencia para desarrolladores](#developer-audience)
-   [Requisitos de tiempo de ejecución](#run-time-requirements)
-   [Compatibilidad con sistemas operativos de nivel inferior](#support-for-down-level-operating-systems)

## <a name="where-applicable"></a>Dónde se puede aplicar

Mediante la automatización de la interfaz de usuario y las siguientes prácticas de diseño accesibles, los desarrolladores pueden hacer que las aplicaciones que se ejecutan en Windows sean más accesibles para muchas personas con discapacidades visuales, auditivas o de movimiento. Además, la automatización de la interfaz de usuario está diseñada específicamente para proporcionar una sólida funcionalidad para escenarios de pruebas automatizadas.

## <a name="developer-audience"></a>Audiencia de los desarrolladores

La automatización de la interfaz de usuario está diseñada para desarrolladores de C/C++ con experiencia. En general, los desarrolladores necesitan un nivel moderado de conocimiento sobre objetos e interfaces COM (modelo de objetos componentes), Unicode y programación de la API de Windows.

Para obtener información sobre la automatización de la interfaz de usuario para código administrado, vea [accesibilidad](/dotnet/framework/ui-automation/) en la sección Guía del desarrollador de .NET Framework de MSDN.

## <a name="run-time-requirements"></a>Requisitos del tiempo de ejecución

La automatización de la interfaz de usuario es compatible con los siguientes sistemas operativos: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016 y Windows Server 2019.

> [!Note]  
> Windows XP y Windows Server 2003 también requieren Microsoft .NET Framework 3,0.

 

## <a name="support-for-down-level-operating-systems"></a>Compatibilidad con sistemas operativos de nivel inferior

La actualización de la plataforma para Windows Vista es un conjunto de bibliotecas en tiempo de ejecución que permite a los desarrolladores destinar aplicaciones a Windows 7 y a sistemas operativos de nivel inferior. La actualización de la plataforma para Windows Server 2008 es un conjunto de bibliotecas en tiempo de ejecución que permite a los desarrolladores destinar aplicaciones a Windows Server 2008 R2 y versiones anteriores de Windows Server. La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 estarán disponibles para todos los clientes de Windows Vista y Windows Server 2008 a través de Windows Update. Las aplicaciones de terceros que requieren la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008 pueden detectar Windows Update detectar si está instalado; en caso contrario, Windows Update lo descargará e instalará en segundo plano.

La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 admiten todo el conjunto de características de Windows Automation API 3,0 en los sistemas operativos siguientes.

-   Windows XP (Inglés) <dl> Windows XP Home SP3 x86  
    Windows XP Professional SP3 x86  
    </dl>
-   Windows Server 2003 (English) <dl> Windows Server 2003 SP2 (x86 y x64)  
    </dl>
-   Windows Vista (Inglés) <dl> Starter SP2 (x86 y x64)  
    Home Premium SP2 (x86 y x64)  
    Service Pack 2 (x86 y x64)  
    Enterprise SP2 (x86 y x64)  
    Ultimate SP2 (x86 y x64)  
    </dl>
-   Windows Server 2008 (Inglés) <dl> Windows Server 2008 SP2 (x86 y x64)  
    </dl>

Para obtener más información acerca de ambas actualizaciones, consulte [actualización de la plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).

## <a name="in-this-section"></a>En esta sección

-   [Fundamentos de UI Automation](entry-uiautocore-overview.md)
-   [Guía del programador del proveedor de UI Automation](uiauto-providerportal.md)
-   [Guía del programador del cliente de UI Automation](uiauto-clientportal.md)
-   [Referencia](entry-uiautocore-ref.md)
-   [Ejemplos](samples-entry.md)
-   [Apéndices](appendix-entry.md)

 

 