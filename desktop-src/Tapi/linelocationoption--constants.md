---
description: Las \_ constantes LINELOCATIONOPTION definen los valores que se usan en el miembro dwOptions de la estructura LINELOCATIONENTRY devuelta como parte de la estructura LINETRANSLATECAPS devuelta por lineGetTranslateCaps.
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: Constantes de LINELOCATIONOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f60398953d2f809e29a78323e3b1dedfcac7a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680771"
---
# <a name="linelocationoption_-constants"></a><span data-ttu-id="28f22-103">Constantes de LINELOCATIONOPTION \_</span><span class="sxs-lookup"><span data-stu-id="28f22-103">LINELOCATIONOPTION\_ Constants</span></span>

<span data-ttu-id="28f22-104">Las **constantes \_ LINELOCATIONOPTION** definen los valores que se usan en el miembro **DwOptions** de la estructura [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) devuelta como parte de la estructura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) devuelta por [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span><span class="sxs-lookup"><span data-stu-id="28f22-104">The **LINELOCATIONOPTION\_** constants define values used in the **dwOptions** member of the [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) structure returned as part of the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure returned by [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span></span>

<dl> <dt>

<span data-ttu-id="28f22-105"><span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION \_ PULSEDIAL**</span><span class="sxs-lookup"><span data-stu-id="28f22-105"><span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION\_PULSEDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="28f22-106">El modo de marcado predeterminado en esta ubicación es el marcado por pulsos.</span><span class="sxs-lookup"><span data-stu-id="28f22-106">The default dialing mode at this location is pulse dialing.</span></span> <span data-ttu-id="28f22-107">Si se establece este bit, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) insertará un modificador de marcado "P" al principio de la cadena de marcado devuelta cuando se seleccione esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="28f22-107">If this bit is set, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) will insert a "P" dial modifier at the beginning of the dialable string returned when this location is selected.</span></span> <span data-ttu-id="28f22-108">Si no se establece este bit, **lineTranslateAddress** insertará un modificador de marcado "T" al principio de la cadena de marcado.</span><span class="sxs-lookup"><span data-stu-id="28f22-108">If this bit is not set, **lineTranslateAddress** will insert a "T" dial modifier at the beginning of the dialable string.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28f22-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28f22-109">Remarks</span></span>

<span data-ttu-id="28f22-110">No extensible.</span><span class="sxs-lookup"><span data-stu-id="28f22-110">Not extensible.</span></span> <span data-ttu-id="28f22-111">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="28f22-111">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="28f22-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28f22-112">Requirements</span></span>



| <span data-ttu-id="28f22-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="28f22-113">Requirement</span></span> | <span data-ttu-id="28f22-114">Value</span><span class="sxs-lookup"><span data-stu-id="28f22-114">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="28f22-115">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="28f22-115">TAPI version</span></span><br/> | <span data-ttu-id="28f22-116">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="28f22-116">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="28f22-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28f22-117">Header</span></span><br/>       | <dl> <span data-ttu-id="28f22-118"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="28f22-118"><dt>Tapi.h</dt></span></span> </dl> |



 

 




