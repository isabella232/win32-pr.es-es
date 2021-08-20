---
description: Microsoft Hyper-V servidor proporciona un entorno de administración de máquinas virtuales escalable, confiable y de alta disponibilidad. El software de máquina virtual de Hyper-V consolida servidores y entornos de desarrollo y pruebas.
ms.assetid: 3359A33F-528B-4955-8B37-30523B8AD33A
title: Proveedor WMI de Hyper-V (V2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b82156754f085196eaece86bb4996c1b4a0bb8348e1566894ee78d4921676f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014253"
---
# <a name="hyper-v-wmi-provider-v2"></a>Proveedor WMI de Hyper-V (V2)

## <a name="purpose"></a>Propósito

Hyper-V proporciona un entorno informático de servidor virtualizado escalable, confiable y de alta disponibilidad. Permite que uno o varios sistemas operativos invitados se ejecuten simultáneamente en un único equipo físico. Entre los usos clave de la tecnología de máquina virtual se incluyen los siguientes:

-   Consolidación de servidores
-   Consolidación de entornos de desarrollo y pruebas
-   Recuperación ante desastres simplificada

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                 | Descripción                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca del proveedor WMI de Hyper-V](about-the-virtualization-wmi-provider.md)<br/>                | El proveedor WMI para Hyper-V permite a los desarrolladores y los desarrolladores crear rápidamente herramientas, utilidades y mejoras personalizadas para la plataforma de virtualización. Las interfaces WMI pueden administrar todos los aspectos de los servicios de Hyper-V.<br/> |
| [Uso del proveedor WMI de Hyper-V](using-the-virtualization-wmi-provider.md)<br/>                | En los temas siguientes se describe cómo usar el proveedor WMI de Hyper-V.<br/>                                                                                                                                                            |
| [Clases WMI de Hyper-V](hyper-v-wmi-classes.md)<br/>                                             | Las siguientes son las clases WMI de Hyper-V.<br/>                                                                                                                                                                                    |
| [API de supervisión de estado de aplicaciones de Hyper-V](hyper-v-application-health-monitoring-api.md)<br/> | La API de supervisión de estado de aplicaciones de Hyper-V se usa para supervisar el estado de mantenimiento de las aplicaciones que se ejecutan en una máquina virtual.<br/>                                                                                               |
| [API de replicación de Hyper-V](hyper-v-replication-api.md)<br/>                                     | La API de replicación de Hyper-V se usa para controlar la replicación de máquinas virtuales y la recuperación de conmutación por error.<br/>                                                                                                                             |
| [API de métricas de Hyper-V](hyper-v-metrics-api.md)<br/>                                             | La API de métricas de Hyper-V se usa para supervisar el estado de mantenimiento de las aplicaciones que se ejecutan en una máquina virtual.<br/>                                                                                                                     |
| [API de red de Hyper-V](hyper-v-networking-api.md)<br/>                                       | La API de red de Hyper-V se usa para controlar las redes en Hyper-V.<br/>                                                                                                                                                          |
| [API de migración de Hyper-V](hyper-v-storage-migration-api.md)<br/>                                 | La API de migración de Hyper-V se usa para controlar el almacenamiento y la migración en vivo en Hyper-V.<br/>                                                                                                                                           |
| [API virtual de Hyper-V Canal de fibra API](hyper-v-virtual-fiber-channels-api.md)<br/>                | La API de Canal de fibra virtual de Hyper-V se usa para controlar los adaptadores de Canal de fibra virtuales en Hyper-V.<br/>                                                                                                                           |
| [API de selección de ubicación de máquinas virtuales de Hyper-V](hyper-v-vm-placement-api.md)<br/>                                   | La API de selección de ubicación de máquinas virtuales (VM) de Hyper-V contiene la información de compatibilidad de las máquinas virtuales o del sistema de hospedaje del equipo.<br/>                                                                                                        |
| [Clases de umbral](threshold-classes.md)<br/>                                                 | Contiene las clases introducidas en Windows 10.<br/>                                                                                                                                                                                |
| [Clases RS2](redstone-classes.md)<br/>                                                        | Contiene las nuevas clases para Windows 10, versión 1703.<br/>                                                                                                                                                                        |
| [Clases RS3](rs3-classes.md)<br/>                                                             | Contiene las nuevas clases para Windows 10, versión 1709.<br/>                                                                                                                                                                        |
| [Glosario de Hyper-V](virtualization-glossary.md)<br/>                                            | Glosario de términos usados en la documentación del SDK Windows Virtualization.<br/>                                                                                                                                                       |



 

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Los servicios de Hyper-V requieren un sistema basado en x64 que admita la virtualización asistida por hardware que ejecuta Hyper-V. Sin embargo, los programas que interactúan con las interfaces WMI de Hyper-V se pueden ejecutar de forma remota en cualquier sistema que admita WMI.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hyper-V (biblioteca Windows Server 2008 R2)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753637(v=ws.10))
</dt> <dt>

[Instrumental de administración de Windows](/windows/desktop/WmiSdk/wmi-start-page)
</dt> <dt>

[Windows Virtualización de servidor](https://www.microsoft.com/windowsserver2008/virtualization/default.mspx)
</dt> </dl>

 

