---
title: El servicio de disco virtual está cambiando a la API de administración de almacenamiento de Windows
description: El servicio de disco virtual está cambiando a la API de administración de almacenamiento de Windows
ms.assetid: AB2A7D08-03B2-4595-A8EC-805D111A0E89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceea3ffe82358737ca8f39e9ef6db0bdb1f116ef
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104421500"
---
# <a name="virtual-disk-service-is-transitioning-to-windows-storage-management-api"></a>El servicio de disco virtual está cambiando a la API de administración de almacenamiento de Windows

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


## <a name="description"></a>Descripción

A partir de Windows 8 y Windows Server 2012, la interfaz COM de servicio de disco virtual se sustituye por la API de administración de almacenamiento, una interfaz de programación basada en WMI. Para administrar los subsistemas de almacenamiento, los discos, las particiones y los volúmenes de (Windows), se recomienda encarecidamente usar la API de administración de almacenamiento. Para obtener más información, consulte [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

En el caso de todos los usos excepto los volúmenes de arranque reflejado (mediante un volumen reflejado para hospedar el sistema operativo), los discos dinámicos están desusados. En el caso de los datos que requieren resistencia frente a errores de unidad, use espacios de almacenamiento, una solución de virtualización de almacenamiento resistente. Para obtener más información, consulte la [vista previa técnica de espacios de almacenamiento](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).

Puede seguir usando DiskPart, Diskraid y administración de discos durante el período de desuso, pero estas herramientas no funcionarán con espacios de almacenamiento ni con ninguna otra API o utilidades de administración de almacenamiento de Windows (WMI) basadas en nuevas Instrumental de administración de Windows (WMI).


| API existentes | Subsistemas de almacenamiento | Discos básicos | Discos dinámicos | Espacios de almacenamiento |
| --- | --- | --- | --- | --- |
| VDS | Sí | Sí | Sí | No |
| WMI | Sí | Sí | No | Sí |
| DiskPart | N/D | Sí | Sí | No |
| DiskRAID |  Sí | N/D | N/D | N/D |
| GUI de administración de discos | N/D | Sí | Sí | No |
| PowerShell | Sí | Sí | No | Sí |
| Panel de control de espacios de almacenamiento | N/D | No | No | Sí |


El resultado de esta transición será una mayor resistencia de almacenamiento, disponibilidad y escalabilidad. un lenguaje de programación y scripting unificado, costos de administración de almacenamiento reducidos y administración de almacenamiento remoto más sencilla.

## <a name="manifestation"></a>Manifestación

Las utilidades DiskPart y Diskraid utilizadas en el entorno de VDS no admiten los nuevos espacios de almacenamiento. Del mismo modo, la nueva utilidad de PowerShell de almacenamiento no admite los discos dinámicos en desuso

## <a name="mitigation"></a>Mitigación

Microsoft recomienda encarecidamente que base las nuevas aplicaciones de administración de almacenamiento en la API de administración de almacenamiento de Windows y que planee la transición de las aplicaciones existentes basadas en la infraestructura de VDS a la API de administración de almacenamiento de Windows durante los ciclos de actualización estándar.

## <a name="resources"></a>Recursos

-   [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Cmdlets de almacenamiento en Windows PowerShell](/powershell/module/storage/?view=win10-ps)
-   [Instrumental de administración de Windows](../wmisdk/wmi-start-page.md)
-   [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=VS.85).aspx)

 

 