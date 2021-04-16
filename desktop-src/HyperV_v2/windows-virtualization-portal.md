---
description: Microsoft Hyper-V Server proporciona un entorno de administración de máquinas virtuales escalable, confiable y de alta disponibilidad. El software de máquina virtual de Hyper-V consolida servidores y entornos de desarrollo y pruebas.
ms.assetid: 3359A33F-528B-4955-8B37-30523B8AD33A
title: Proveedor de WMI de Hyper-V (V2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555fd3cd1e8420c59bb5f1b8ef16480b3ddfcf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686732"
---
# <a name="hyper-v-wmi-provider-v2"></a>Proveedor de WMI de Hyper-V (V2)

## <a name="purpose"></a>Propósito

Hyper-V proporciona un entorno de computación de servidores virtualizado escalable, confiable y de alta disponibilidad. Permite que uno o más sistemas operativos invitados se ejecuten simultáneamente en un solo equipo físico. Entre los usos clave de la tecnología de máquina virtual se incluyen los siguientes:

-   Consolidación de servidores
-   Consolidación de entornos de desarrollo y pruebas
-   Recuperación ante desastres simplificada

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                 | Descripción                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca del proveedor WMI de Hyper-V](about-the-virtualization-wmi-provider.md)<br/>                | El proveedor WMI de Hyper-V permite a los desarrolladores y generadores de scripts crear rápidamente herramientas, utilidades y mejoras personalizadas para la plataforma de virtualización. Las interfaces WMI pueden administrar todos los aspectos de los servicios de Hyper-V.<br/> |
| [Usar el proveedor WMI de Hyper-V](using-the-virtualization-wmi-provider.md)<br/>                | En los temas siguientes se describe cómo usar el proveedor WMI de Hyper-V.<br/>                                                                                                                                                            |
| [Clases WMI de Hyper-V](hyper-v-wmi-classes.md)<br/>                                             | A continuación se muestran las clases WMI de Hyper-V.<br/>                                                                                                                                                                                    |
| [API de supervisión de estado de aplicaciones de Hyper-V](hyper-v-application-health-monitoring-api.md)<br/> | La API de supervisión de estado de aplicaciones de Hyper-V se usa para supervisar el estado de mantenimiento de las aplicaciones que se ejecutan en una máquina virtual.<br/>                                                                                               |
| [API de replicación de Hyper-V](hyper-v-replication-api.md)<br/>                                     | La API de replicación de Hyper-V se utiliza para controlar la replicación de máquinas virtuales y la recuperación de la conmutación por error.<br/>                                                                                                                             |
| [API de métricas de Hyper-V](hyper-v-metrics-api.md)<br/>                                             | La API de métricas de Hyper-V se usa para supervisar el estado de mantenimiento de las aplicaciones que se ejecutan en una máquina virtual.<br/>                                                                                                                     |
| [API de red de Hyper-V](hyper-v-networking-api.md)<br/>                                       | La API de red de Hyper-V se usa para controlar la red en Hyper-V.<br/>                                                                                                                                                          |
| [API de migración de Hyper-V](hyper-v-storage-migration-api.md)<br/>                                 | La API de migración de Hyper-V se usa para controlar el almacenamiento y la migración en vivo en Hyper-V.<br/>                                                                                                                                           |
| [API de Canal de fibra virtual de Hyper-V](hyper-v-virtual-fiber-channels-api.md)<br/>                | La API de Canal de fibra virtual de Hyper-V se usa para controlar los adaptadores de Canal de fibra virtual en Hyper-V.<br/>                                                                                                                           |
| [API de selección de ubicación de máquinas virtuales de Hyper-V](hyper-v-vm-placement-api.md)<br/>                                   | La API de selección de ubicación de máquina virtual (VM) de Hyper-V contiene la información de compatibilidad de las máquinas virtuales o el sistema del equipo host.<br/>                                                                                                        |
| [Clases de umbral](threshold-classes.md)<br/>                                                 | Contiene las clases introducidas en Windows 10.<br/>                                                                                                                                                                                |
| [Clases RS2](redstone-classes.md)<br/>                                                        | Contiene las nuevas clases para Windows 10, versión 1703.<br/>                                                                                                                                                                        |
| [Clases RS3](rs3-classes.md)<br/>                                                             | Contiene las nuevas clases para Windows 10, versión 1709.<br/>                                                                                                                                                                        |
| [Glosario de Hyper-V](virtualization-glossary.md)<br/>                                            | Glosario de términos usados en la documentación del SDK de virtualización de Windows.<br/>                                                                                                                                                       |



 

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Los servicios de Hyper-V requieren un sistema basado en x64 que admita la virtualización asistida por hardware que ejecuta Hyper-V. Sin embargo, los programas que interactúan con las interfaces WMI de Hyper-V se pueden ejecutar de forma remota en cualquier sistema compatible con WMI.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hyper-V (biblioteca técnica de Windows Server 2008 R2)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753637(v=ws.10))
</dt> <dt>

[Instrumental de administración de Windows](/windows/desktop/WmiSdk/wmi-start-page)
</dt> <dt>

[Virtualización de Windows Server](https://www.microsoft.com/windowsserver2008/virtualization/default.mspx)
</dt> </dl>

 

