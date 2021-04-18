---
description: Hay algunas consideraciones que son exclusivas de los sistemas administrados de forma remota.
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: Consideraciones sobre la administración remota de WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bb40776f6b727abb49d7e0685bb12b087ed2bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706853"
---
# <a name="wfp-remote-administration-considerations"></a><span data-ttu-id="87b01-103">Consideraciones sobre la administración remota de WFP</span><span class="sxs-lookup"><span data-stu-id="87b01-103">WFP Remote Administration Considerations</span></span>

<span data-ttu-id="87b01-104">Hay algunas consideraciones que son exclusivas de los sistemas administrados de forma remota.</span><span class="sxs-lookup"><span data-stu-id="87b01-104">There are some considerations that are unique to remotely administered systems.</span></span> <span data-ttu-id="87b01-105">En primer lugar, cuando la instalación de software se implementa de forma remota (mediante SMS o MSI), los cuadros de diálogo de error de WFP se muestran en la pantalla de un administrador con sesión iniciada localmente (si existe), no en el servicio de instalación.</span><span class="sxs-lookup"><span data-stu-id="87b01-105">First, when software installation is remotely deployed (using SMS or MSI), WFP error dialog boxes are displayed on the screen of a locally logged on administrator (if present), not to the installation service.</span></span> <span data-ttu-id="87b01-106">En segundo lugar, si un administrador inicia sesión en un servidor de Terminal Server de forma remota e instala una aplicación que reemplaza los archivos del sistema protegidos, los cuadros de diálogo de error de WFP solo se muestran en la consola principal, no en la ventana remota del administrador.</span><span class="sxs-lookup"><span data-stu-id="87b01-106">Second, if an administrator logs into a terminal server remotely and installs an application that replaces protected system files, the WFP error dialog boxes are displayed only in the main console, not the administrator's remote window.</span></span>

<span data-ttu-id="87b01-107">Por estos motivos, WFP suprime los cuadros de diálogo de error hasta que un administrador inicia sesión localmente.</span><span class="sxs-lookup"><span data-stu-id="87b01-107">For these reasons, WFP suppresses its error dialog boxes until an administrator logs on locally.</span></span> <span data-ttu-id="87b01-108">Los administradores remotos pueden encontrar errores de reemplazo de archivos en el registro de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="87b01-108">Remote administrators can find file replacement errors in the system event log.</span></span>

<span data-ttu-id="87b01-109">**Windows Vista y Windows Server 2008:** No se admite la administración remota de WFP.</span><span class="sxs-lookup"><span data-stu-id="87b01-109">**Windows Vista and Windows Server 2008:** WFP remote administration is not supported.</span></span>

 

 



