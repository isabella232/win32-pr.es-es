---
title: Virtual Disk Service está transfiriendo a Windows Storage API de Administración
description: Virtual Disk Service está transfiriendo a Windows Storage API de Administración
ms.assetid: AB2A7D08-03B2-4595-A8EC-805D111A0E89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a45e25452ae0b6bb20e0ca04130b7fa2fd64f2a191d504380f973f663b7931ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852042"
---
# <a name="virtual-disk-service-is-transitioning-to-windows-storage-management-api"></a>Virtual Disk Service está transfiriendo a Windows Storage API de Administración

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8  
**Servidores:** Windows Server 2012  


## <a name="description"></a>Descripción

A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio virtual de disco se sustituye por el Storage API de Administración, una interfaz de programación basada en WMI. Para administrar subsistemas de almacenamiento, (Windows) discos, particiones y volúmenes, se recomienda encarecidamente usar el Storage API de Administración. Para obtener más información, [vea Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Para todos los usos excepto los volúmenes de arranque reflejados (con un volumen reflejado para hospedar el sistema operativo), los discos dinámicos están en desuso. Para los datos que requieren resistencia frente a errores de unidad, use Espacios de almacenamiento, una solución de virtualización de almacenamiento resistente. Para obtener más información, [vea Espacios de almacenamiento Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).

Puede seguir usando DiskPart, DiskRAID y Administración de discos durante el período de desuso, pero estas herramientas no funcionarán con Espacios de almacenamiento ni con otras nuevas API de administración de Windows Storage basadas en Windows Management Instrumentation (WMI) o con clientes o utilidades de administración de almacenamiento integradas.


| API existentes | Subsistemas de almacenamiento | Discos básicos | Discos dinámicos | Espacios de almacenamiento |
| --- | --- | --- | --- | --- |
| Vds | Sí | Sí | Sí | No |
| WMI | Sí | Sí | No | Sí |
| DiskPart | N/D | Sí | Sí | No |
| DiskRAID |  Sí | N/D | N/D | N/D |
| INTERFAZ GRÁFICA de usuario de Mgmt de disco | N/D | Sí | Sí | No |
| PowerShell | Sí | Sí | No | Sí |
| Espacios de almacenamiento Panel de control | N/D | No | No | Sí |


El resultado de esta transición será una mayor resistencia, disponibilidad y escalabilidad del almacenamiento. un lenguaje de programación y scripting unificado, menores costos de administración de almacenamiento y una administración más sencilla del almacenamiento remoto.

## <a name="manifestation"></a>Manifestación

Las utilidades DiskPart y DiskRAID usadas en el entorno VDS no admiten el nuevo Espacios de almacenamiento. Del mismo modo, la nueva Storage de PowerShell no admite los discos dinámicos en desuso.

## <a name="mitigation"></a>Mitigación

Microsoft recomienda encarecidamente que base las nuevas aplicaciones de administración de almacenamiento en el Windows Storage API de Administración y que planee la transición de las aplicaciones existentes basadas en la infraestructura vds. al Windows Storage API de Administración durante los ciclos de actualización estándar.

## <a name="resources"></a>Recursos

-   [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Cmdlets de almacenamiento en Windows PowerShell](/powershell/module/storage/?view=win10-ps)
-   [Instrumental de administración de Windows](../wmisdk/wmi-start-page.md)
-   [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=VS.85).aspx)

 

 