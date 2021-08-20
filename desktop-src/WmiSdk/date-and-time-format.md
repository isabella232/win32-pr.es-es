---
description: Describe el formato Modelo de información común (CIM) de fecha y hora usado por WMI. Este formato es independiente de la configuración regional, por lo que los scripts que usan DATETIME se pueden ejecutar en muchas zonas horarias.
ms.assetid: be239bf8-88a3-47bc-ae4f-49a5195e7a7d
ms.tgt_platform: multiple
title: Formato de fecha y hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb33f9c252a35fba35dcaa5c07d320033d043da1b148f6a6718ad8a3c637240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925491"
---
# <a name="date-and-time-format"></a>Formato de fecha y hora

WMI usa los formatos de fecha y hora definidos por la especificación distributed management task force ([DMTF.org](https://www.dmtf.org/)) Modelo de información común (CIM).

El **formato \_ CIM DATETIME** se implementa en microsoft [Managed Object Format (MOF)](managed-object-format--mof-.md) mediante el tipo de datos [MOF DATETIME.](datetime.md) Los formatos de fecha y hora también pueden expresar un intervalo de tiempo.

Para obtener más información sobre los formatos WMI, [vea CIM \_ DATETIME](cim-datetime.md) y [Interval Format](interval-format.md).

Para obtener más información sobre la conversión a y desde el formato DATETIME de WMI, vea [**SWbemDateTime**](swbemdatetime.md) y el artículo sobre TechNet ScriptCenter [It's About Time (Oh, and About Dates, too) (Acerca](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx)de las fechas, también).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WMI](about-wmi.md)
</dt> </dl>

 

 



