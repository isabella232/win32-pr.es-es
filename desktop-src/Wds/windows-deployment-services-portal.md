---
title: Servicios de implementación de Windows
description: Implemente Windows sistemas operativos. Configure nuevos clientes con una instalación basada en red sin necesidad de que los administradores visiten cada equipo o instalen directamente desde medios de CD o DVD.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Windows Deployment Services Windows Deployment Services
- Windows Deployment Services Windows Deployment Services , página principal
- servicios de implementación Windows Deployment Services
- WDS Windows Deployment Services consulte Windows Deployment Services
- Servicios de instalación remota Windows Deployment Services consulte Windows Deployment Services
- RIS Windows Deployment Services Consulte Windows Deployment Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35bebb000b383552f12d259ca17552165e9247f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359119"
---
# <a name="windows-deployment-services"></a>Servicios de implementación de Windows

## <a name="purpose"></a>Propósito

Windows Deployment Services (WDS) es la versión revisada de Servicios de instalación remota (RIS). WDS permite la implementación de Windows sistemas operativos. Puede usar WDS para configurar nuevos clientes con una instalación basada en red sin necesidad de que los administradores visiten cada equipo o se instalen directamente desde medios de CD o DVD.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La audiencia principal para desarrolladores de la API de WDS es para los grupos que desarrollan herramientas y procesos personalizados para TI y otros grupos de administración de equipos. En entornos en los que no se puede usar Windows de servicios de implementación de implementación (WDS) estándar, la API de WDS permite el acceso mediante programación a algunos componentes de WDS.

Los fabricantes de equipos originales (OEM), los generadores de sistemas y los profesionales de TI corporativos que buscan información sobre cómo implementar Windows en equipos nuevos deben ver la información sobre la solución estándar de Windows Deployment Services (WDS) en la Guía paso a paso de actualización de [Windows Deployment Services](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) y el Kit de instalación automatizada [(UUK)](https://www.microsoft.com/download/details.aspx?id=10333)de Windows.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

WDS está disponible como complemento para Windows Server 2003 con Service Pack 1 (SP1) y se incluye en el sistema operativo a partir de Windows Server 2003 con Service Pack 2 (SP2) y Windows Server 2008. La API del servidor PXE de WDS requiere el rol de servidor WDS en el servidor para implementar proveedores PXE personalizados. La API de cliente de WDS requiere la fase Windows entorno de preinstalación de Microsoft (Windows PE 2.0) del procesamiento de la instalación. Imagen de arranque RAMDISK de Windows PE 2.0 en . El formato WIM debe descargarse como parte del proceso de arranque de red para implementar clientes WDS personalizados.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                 | Descripción                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Acerca de la API Windows Deployment Services](about-the-windows-deployment-services-api.md)<br/> | Información general sobre la API del servidor WDS y la API de cliente de WDS.<br/>    |
| [Windows Referencia de servicios de implementación](windows-deployment-services-reference.md)<br/>         | Describe las Windows y estructuras de Deployment Services.<br/> |



 

 

