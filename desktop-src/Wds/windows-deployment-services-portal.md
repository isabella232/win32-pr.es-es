---
title: Servicios de implementación de Windows
description: Implementar sistemas operativos Windows. Configure nuevos clientes con una instalación basada en red sin necesidad de que los administradores visiten cada equipo o instalen directamente desde un CD o DVD.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Servicios de implementación de Windows servicios de implementación de Windows
- Servicios de implementación de Windows servicios de implementación de Windows, Página principal
- servicios de implementación servicios de implementación de Windows
- Servicios de implementación de Windows WDS véase servicios de implementación de Windows
- Servicios de instalación remota servicios de implementación de Windows ver servicios de implementación de Windows
- Servicios de implementación de Windows de RIS, vea servicios de implementación de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35bebb000b383552f12d259ca17552165e9247f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105705021"
---
# <a name="windows-deployment-services"></a>Servicios de implementación de Windows

## <a name="purpose"></a>Propósito

Servicios de implementación de Windows (WDS) es la versión revisada de los servicios de instalación remota (RIS). WDS permite la implementación de sistemas operativos Windows. Puede usar WDS para configurar nuevos clientes con una instalación basada en red sin necesidad de que los administradores visiten cada equipo o instalen directamente desde un CD o DVD.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La audiencia principal del desarrollador de la API de WDS es para los grupos que desarrollan herramientas y procesos personalizados para ti y otros grupos de administración de equipos. En entornos donde no se puede usar la solución estándar de servicios de implementación de Windows (WDS), la API de WDS permite el acceso mediante programación a algunos componentes de WDS.

Los fabricantes de equipos originales (OEM), los ensambladores de equipos y los profesionales de TI de la empresa que buscan información sobre cómo implementar Windows en equipos nuevos, deben ver la información acerca de la solución de servicios de implementación de Windows (WDS) estándar en la [Guía paso a paso de actualización](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) de los servicios de implementación de Windows y el [Kit de instalación automatizada de Windows (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

WDS está disponible como complemento para Windows Server 2003 con Service Pack 1 (SP1) y se incluye en el sistema operativo a partir de Windows Server 2003 con Service Pack 2 (SP2) y Windows Server 2008. La API del servidor PXE PXE requiere el rol de servidor de WDS en el servidor para implementar proveedores de PXE personalizados. La API de cliente de WDS requiere la fase de Microsoft Entorno de preinstalación de Windows (Windows PE 2,0) del proceso de instalación. Una imagen de arranque de RAMDISK de Windows PE 2,0 en. El formato WIM se debe descargar como parte del proceso de arranque de red para implementar clientes WDS personalizados.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                 | Descripción                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Acerca de la API de servicios de implementación de Windows](about-the-windows-deployment-services-api.md)<br/> | Información general sobre la API del servidor WDS y la API de cliente de WDS.<br/>    |
| [Referencia de servicios de implementación de Windows](windows-deployment-services-reference.md)<br/>         | Describe las funciones y estructuras de servicios de implementación de Windows.<br/> |



 

 

