---
description: Esta \_ función TSPI lineSetCurrentLocation está obsoleta. TAPI llamó a esta función cuando el usuario (mediante el cuadro de diálogo Propiedades de marcado) o una aplicación (mediante la función lineSetCurrentLocation) cambió la ubicación de traducción de direcciones.
ms.assetid: acd9f05b-88ae-439a-95c0-d1e8779a32fe
title: TSPI_lineSetCurrentLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2361135770ac2d3900a902e0b7fa4fecad511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814363"
---
# <a name="tspi_linesetcurrentlocation"></a><span data-ttu-id="c6685-104">TSPI \_ lineSetCurrentLocation</span><span class="sxs-lookup"><span data-stu-id="c6685-104">TSPI\_lineSetCurrentLocation</span></span>

<span data-ttu-id="c6685-105">Esta \_ función TSPI lineSetCurrentLocation está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="c6685-105">This TSPI\_lineSetCurrentLocation function is obsolete.</span></span> <span data-ttu-id="c6685-106">TAPI llamó a esta función cuando el usuario (mediante el cuadro de diálogo **propiedades de marcado** ) o una aplicación (mediante la función [**lineSetCurrentLocation**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) ) cambió la ubicación de traducción de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c6685-106">TAPI called this function when the user (using the **Dialing Properties** dialog box) or an application (using the [**lineSetCurrentLocation**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) function) changed the address translation location.</span></span>

<span data-ttu-id="c6685-107">Actualmente, un cambio en la ubicación de traducción da como resultado un \_ mensaje line DEVSTATE con *dwParam1* establecido en LINEDEVSTATE \_ TRANSLATECHANGE.</span><span class="sxs-lookup"><span data-stu-id="c6685-107">Currently, a change in translation location results in a LINE\_DEVSTATE message with *dwParam1* set to LINEDEVSTATE\_TRANSLATECHANGE.</span></span>

 

 
