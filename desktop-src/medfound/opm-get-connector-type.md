---
description: Devuelve el tipo de conector físico de la salida de vídeo.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a95ca88b079aa93b4c2665fe7aa954eb58cfc1a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275833"
---
# <a name="opm_get_connector_type"></a><span data-ttu-id="ff99a-103">\_tipo de \_ conector de obtención de OPM \_</span><span class="sxs-lookup"><span data-stu-id="ff99a-103">OPM\_GET\_CONNECTOR\_TYPE</span></span>

<span data-ttu-id="ff99a-104">Devuelve el tipo de conector físico de la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ff99a-104">Returns the physical connector type of the video output.</span></span>



| <span data-ttu-id="ff99a-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff99a-105">Requirement</span></span> | <span data-ttu-id="ff99a-106">Value</span><span class="sxs-lookup"><span data-stu-id="ff99a-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="ff99a-107">GUID de solicitud</span><span class="sxs-lookup"><span data-stu-id="ff99a-107">Request GUID</span></span> | <span data-ttu-id="ff99a-108">\_tipo de \_ conector de obtención de OPM \_</span><span class="sxs-lookup"><span data-stu-id="ff99a-108">OPM\_GET\_CONNECTOR\_TYPE</span></span>                                                   |
| <span data-ttu-id="ff99a-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="ff99a-109">Input data</span></span>   | <span data-ttu-id="ff99a-110">None</span><span class="sxs-lookup"><span data-stu-id="ff99a-110">None</span></span>                                                                        |
| <span data-ttu-id="ff99a-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="ff99a-111">Return data</span></span>  | <span data-ttu-id="ff99a-112">Una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="ff99a-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ff99a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff99a-113">Remarks</span></span>

<span data-ttu-id="ff99a-114">El tipo de conector se devuelve en el miembro **ulInformation** de la estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="ff99a-114">The connector type is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="ff99a-115">El valor de **ulInformation** es igual a uno de los tipos de conectores que aparecen en las [**marcas de tipo de conector de OPM**](opm-connector-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ff99a-115">The value of **ulInformation** is equal to one of the connector types listed in [**OPM Connector Type Flags**](opm-connector-type-flags.md).</span></span>

<span data-ttu-id="ff99a-116">En el modo de emulación de COPP, el tipo de conector podría combinarse con la marca **\_ interna del \_ \_ \_ tipo \_ de conector compatible de COPP de OPM** .</span><span class="sxs-lookup"><span data-stu-id="ff99a-116">In COPP emulation mode, the connector type might be combined with the **OPM\_COPP\_COMPATIBLE\_CONNECTOR\_TYPE\_INTERNAL** flag.</span></span> <span data-ttu-id="ff99a-117">Use una operación and bit a bit para extraer el **tipo de conector** :</span><span class="sxs-lookup"><span data-stu-id="ff99a-117">Use a bitwise **AND** to extract the connector type:</span></span>

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

<span data-ttu-id="ff99a-118">Las aplicaciones deben omitir la marca **\_ interna del \_ \_ \_ tipo \_ de conector compatible de COPP de OPM** .</span><span class="sxs-lookup"><span data-stu-id="ff99a-118">Applications should ignore the **OPM\_COPP\_COMPATIBLE\_CONNECTOR\_TYPE\_INTERNAL** flag.</span></span> <span data-ttu-id="ff99a-119">Para obtener más información, consulte la sección Comentarios de las [**marcas de tipo de conector de OPM**](opm-connector-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ff99a-119">For more information, see the Remarks section of [**OPM Connector Type Flags**](opm-connector-type-flags.md).</span></span>

<span data-ttu-id="ff99a-120">Esta consulta es equivalente a la \_ consulta COPPQueryConnectorType de DXVA usada en el protocolo de protección de la salida certificada (COPP).</span><span class="sxs-lookup"><span data-stu-id="ff99a-120">This query is equivalent to the DXVA\_COPPQueryConnectorType query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff99a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff99a-121">Requirements</span></span>



| <span data-ttu-id="ff99a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff99a-122">Requirement</span></span> | <span data-ttu-id="ff99a-123">Value</span><span class="sxs-lookup"><span data-stu-id="ff99a-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ff99a-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff99a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ff99a-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ff99a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ff99a-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff99a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ff99a-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff99a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ff99a-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff99a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff99a-129"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff99a-129"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff99a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff99a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff99a-131">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="ff99a-131">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="ff99a-132">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="ff99a-132">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="ff99a-133">Solicitudes de estado de OPM</span><span class="sxs-lookup"><span data-stu-id="ff99a-133">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




