---
description: Las \_ constantes LINECARDOPTION definen los valores que se usan en el miembro dwOptions de la estructura LINECARDENTRY devuelta como parte de la estructura LINETRANSLATECAPS devuelta por lineGetTranslateCaps.
ms.assetid: 36c67fbf-e5ca-4ec4-a03a-0b828667abcc
title: Constantes de LINECARDOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9948d4a8963e8a9c860f68f0067c601f602c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681233"
---
# <a name="linecardoption_-constants"></a><span data-ttu-id="ded28-103">Constantes de LINECARDOPTION \_</span><span class="sxs-lookup"><span data-stu-id="ded28-103">LINECARDOPTION\_ Constants</span></span>

<span data-ttu-id="ded28-104">Las **\_ constantes LINECARDOPTION** definen los valores que se usan en el miembro **DwOptions** de la estructura [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) devuelta como parte de la estructura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) devuelta por [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span><span class="sxs-lookup"><span data-stu-id="ded28-104">The **LINECARDOPTION\_constants** define values used in the **dwOptions** member of the [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) structure returned as part of the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure returned by [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span></span> <span data-ttu-id="ded28-105">Las **\_ constantes de LINECARDOPTION** t tienen los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="ded28-105">The **LINECARDOPTION\_constants** t has the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ded28-106"><span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION \_ oculto**</span><span class="sxs-lookup"><span data-stu-id="ded28-106"><span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION\_HIDDEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ded28-107">El usuario ha ocultado esta tarjeta de llamada.</span><span class="sxs-lookup"><span data-stu-id="ded28-107">This calling card has been hidden by the user.</span></span> <span data-ttu-id="ded28-108">No se muestra en la aplicación auxiliar de marcado en la lista principal de tarjetas de llamada disponibles, pero se mostrará en la lista de tarjetas de las que se pueden copiar reglas de marcado.</span><span class="sxs-lookup"><span data-stu-id="ded28-108">It is not shown by Dial Helper in the main listing of available calling cards, but will be shown in the list of cards from which dialing rules can be copied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ded28-109"><span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION \_ PREdefinido**</span><span class="sxs-lookup"><span data-stu-id="ded28-109"><span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION\_PREDEFINED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ded28-110">Esta tarjeta de llamada es una de las definiciones de tarjeta de llamada predefinidas incluidas con telefonía por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ded28-110">This calling card is one of the predefined calling card definitions included with Telephony by Microsoft.</span></span> <span data-ttu-id="ded28-111">No se puede quitar completamente mediante la aplicación auxiliar de marcado; Si el usuario intenta quitarlo, se quedará oculto.</span><span class="sxs-lookup"><span data-stu-id="ded28-111">It cannot be removed entirely using Dial Helper; if the user attempts to remove it, it will become HIDDEN.</span></span> <span data-ttu-id="ded28-112">Por lo tanto, sigue siendo accesible para copiar reglas de marcado.</span><span class="sxs-lookup"><span data-stu-id="ded28-112">It thus continues to be accessible for copying of dialing rules.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ded28-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ded28-113">Remarks</span></span>

<span data-ttu-id="ded28-114">No extensible.</span><span class="sxs-lookup"><span data-stu-id="ded28-114">Not extensible.</span></span> <span data-ttu-id="ded28-115">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="ded28-115">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="ded28-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ded28-116">Requirements</span></span>



| <span data-ttu-id="ded28-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ded28-117">Requirement</span></span> | <span data-ttu-id="ded28-118">Value</span><span class="sxs-lookup"><span data-stu-id="ded28-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ded28-119">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="ded28-119">TAPI version</span></span><br/> | <span data-ttu-id="ded28-120">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="ded28-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ded28-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ded28-121">Header</span></span><br/>       | <dl> <span data-ttu-id="ded28-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ded28-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




