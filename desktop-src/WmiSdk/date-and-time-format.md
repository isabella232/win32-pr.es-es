---
description: Describe el formato de fecha y hora de Modelo de información común (CIM) utilizado por WMI. Este formato es independiente de la configuración regional, por lo que los scripts que usan DATETIME se pueden ejecutar en muchas zonas horarias.
ms.assetid: be239bf8-88a3-47bc-ae4f-49a5195e7a7d
ms.tgt_platform: multiple
title: Formato de fecha y hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e8f97930efa33942fe87b2109aa7cd7ba9d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156005"
---
# <a name="date-and-time-format"></a><span data-ttu-id="5327b-104">Formato de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="5327b-104">Date and Time Format</span></span>

<span data-ttu-id="5327b-105">WMI usa los formatos de fecha y hora definidos por la especificación de Modelo de información común (CIM) del equipo de administración distribuida ([DMTF.org](https://www.dmtf.org/)).</span><span class="sxs-lookup"><span data-stu-id="5327b-105">WMI uses the date and time formats defined by the Distributed Management Task Force ([DMTF.org](https://www.dmtf.org/)) Common Information Model (CIM) specification.</span></span>

<span data-ttu-id="5327b-106">El formato de **\_ fecha y hora de CIM** se implementa en Microsoft [Managed Object Format (MOF)](managed-object-format--mof-.md) mediante el tipo de [valor de fecha y hora](datetime.md) MOF.</span><span class="sxs-lookup"><span data-stu-id="5327b-106">The **CIM\_DATETIME** format is implemented in the Microsoft [Managed Object Format (MOF)](managed-object-format--mof-.md) by the [DATETIME](datetime.md) MOF datatype.</span></span> <span data-ttu-id="5327b-107">Los formatos de fecha y hora también pueden expresar un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="5327b-107">The date and time formats can also express an interval of time.</span></span>

<span data-ttu-id="5327b-108">Para obtener más información sobre los formatos de WMI, consulte [formato de intervalo](interval-format.md)y [fecha y \_ hora de CIM](cim-datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="5327b-108">For more information about WMI formats, see [CIM\_DATETIME](cim-datetime.md) and [Interval Format](interval-format.md).</span></span>

<span data-ttu-id="5327b-109">Para obtener más información sobre la conversión a y desde el formato de fecha y hora de WMI, consulte [**SWbemDateTime**](swbemdatetime.md) y el artículo en TechNet ScriptCenter [sobre la hora (oh y las fechas)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="5327b-109">For more information about converting to and from the WMI DATETIME format, see [**SWbemDateTime**](swbemdatetime.md) and the article on TechNet ScriptCenter [It's About Time (Oh, and About Dates, too)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5327b-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5327b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5327b-111">Acerca de WMI</span><span class="sxs-lookup"><span data-stu-id="5327b-111">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 



