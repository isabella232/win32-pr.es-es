---
description: Especifica el tipo de acción de una operación de prevención de pérdida de datos (DLP) de punto de conexión.
title: Enumeración DlpActionType (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpActionType
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 7900e79536cc9ac45037e205962a563bcde8878a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495955"
---
# <a name="dlpactiontype-enumeration"></a><span data-ttu-id="97c25-103">Enumeración DlpActionType</span><span class="sxs-lookup"><span data-stu-id="97c25-103">DlpActionType enumeration</span></span>

<span data-ttu-id="97c25-104">Especifica el tipo de acción de una operación de prevención de pérdida de datos (DLP) del punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="97c25-104">Specifies the action type of an endpoint Data Loss Prevention (DLP) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c25-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97c25-105">Syntax</span></span>


```C++
typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
```


## <a name="constants"></a><span data-ttu-id="97c25-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="97c25-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="97c25-107">*DlpActionTypeCopyToRemovableMedia*</span><span class="sxs-lookup"><span data-stu-id="97c25-107">*DlpActionTypeCopyToRemovableMedia*</span></span>
</dt> <dd>

<span data-ttu-id="97c25-108">Una operación de copia en un medio extraíble.</span><span class="sxs-lookup"><span data-stu-id="97c25-108">A copy operation to removable media.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="97c25-109">*DlpActionTypeCopyToNetworkShare*</span><span class="sxs-lookup"><span data-stu-id="97c25-109">*DlpActionTypeCopyToNetworkShare*</span></span>
</dt> <dd>

<span data-ttu-id="97c25-110">Una operación de copia en una carpeta de red compartida.</span><span class="sxs-lookup"><span data-stu-id="97c25-110">A copy operation to a shared network folder.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="97c25-111">*DlpActionTypeCopyToClipboard*</span><span class="sxs-lookup"><span data-stu-id="97c25-111">*DlpActionTypeCopyToClipboard*</span></span>
</dt> <dd>

<span data-ttu-id="97c25-112">Una operación de copia en el Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="97c25-112">A copy operation to the clipboard.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="97c25-113">*DlpActionTypePrint*</span><span class="sxs-lookup"><span data-stu-id="97c25-113">*DlpActionTypePrint*</span></span>
</dt> <dd>

<span data-ttu-id="97c25-114">Una operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="97c25-114">A print operation.</span></span>

</dd> </dl>


<dl> <dt>

<span data-ttu-id="97c25-115">*DlpActionTypeScreenClip*</span><span class="sxs-lookup"><span data-stu-id="97c25-115">*DlpActionTypeScreenClip*</span></span>
</dt> <dd>

<span data-ttu-id="97c25-116">Una operación de captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="97c25-116">A screen capture operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="97c25-117">*DlpActionTypeAccessByUnallowedApp*</span><span class="sxs-lookup"><span data-stu-id="97c25-117">*DlpActionTypeAccessByUnallowedApp*</span></span>
</dt> <dd>

<span data-ttu-id="97c25-118">Una operación realizada por una aplicación no permitido.</span><span class="sxs-lookup"><span data-stu-id="97c25-118">An operation performed by an unallowed app.</span></span>

</dd> </dl>


<dl> <dt>

<span data-ttu-id="97c25-119">*DlpActionTypeCloudAppEgress*</span><span class="sxs-lookup"><span data-stu-id="97c25-119">*DlpActionTypeCloudAppEgress*</span></span>
</dt> <dd>

<span data-ttu-id="97c25-120">Operación destinada a una ubicación en la nube.</span><span class="sxs-lookup"><span data-stu-id="97c25-120">An operation targeted to a cloud location.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="97c25-121">*DlpActionTypeAccessByBluetoothApp*</span><span class="sxs-lookup"><span data-stu-id="97c25-121">*DlpActionTypeAccessByBluetoothApp*</span></span>
</dt> <dd>

<span data-ttu-id="97c25-122">Una operación que incluye el acceso mediante una aplicación bluetooth.</span><span class="sxs-lookup"><span data-stu-id="97c25-122">An operation that includes access by a bluetooth app.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="97c25-123">*DlpActionTypeAccessByRDPApp*</span><span class="sxs-lookup"><span data-stu-id="97c25-123">*DlpActionTypeAccessByRDPApp*</span></span>
</dt> <dd>

<span data-ttu-id="97c25-124">Una operación que incluye el acceso mediante un escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="97c25-124">An operation that includes access by a remote desktop.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="97c25-125">*DlpActionTypeCount*</span><span class="sxs-lookup"><span data-stu-id="97c25-125">*DlpActionTypeCount*</span></span>
</dt> <dd>

<span data-ttu-id="97c25-126">Valor máximo de la enumeración .</span><span class="sxs-lookup"><span data-stu-id="97c25-126">The maximum value of the enumeration.</span></span>

</dd> </dl>
 

## <a name="remarks"></a><span data-ttu-id="97c25-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97c25-127">Remarks</span></span>

<span data-ttu-id="97c25-128">La estructura DLP_APP_OP_ENLIGHTENED_LEVEL utiliza [los valores de esta enumeración.](endpointdlp-dlp_app_op_enlightened_level.md)</span><span class="sxs-lookup"><span data-stu-id="97c25-128">Values from this enumeration are used by the [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="97c25-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97c25-129">Requirements</span></span>



| <span data-ttu-id="97c25-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="97c25-130">Requirement</span></span>          |    <span data-ttu-id="97c25-131">Value</span><span class="sxs-lookup"><span data-stu-id="97c25-131">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97c25-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97c25-132">Minimum supported client</span></span><br/> | <span data-ttu-id="97c25-133">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="97c25-133">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

