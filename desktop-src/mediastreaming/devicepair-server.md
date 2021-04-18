---
title: Propiedad del servidor DevicePair (Asptlb. h)
description: Obtiene el servidor para el par de dispositivo básico activo.
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- Propiedad de servidor API de streaming de multimedia
- Propiedad de servidor API de streaming de multimedia, interfaz DevicePair
- Interfaz DevicePair API de streaming de multimedia, propiedad de servidor
topic_type:
- apiref
api_name:
- DevicePair.Server
- DevicePair.get_Server
api_location:
- asptlb.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec2c28e8118f6cf11e89c7ab4a5ba04abd8b8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718600"
---
# <a name="devicepairserver-property"></a><span data-ttu-id="fd785-106">DevicePair:: Server (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fd785-106">DevicePair::Server property</span></span>

<span data-ttu-id="fd785-107">Obtiene el servidor para el par de dispositivo básico activo.</span><span class="sxs-lookup"><span data-stu-id="fd785-107">Gets the server for the active basic device pair.</span></span>

<span data-ttu-id="fd785-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fd785-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd785-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd785-109">Syntax</span></span>


```C++
HRESULT get_Server(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a><span data-ttu-id="fd785-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fd785-110">Property value</span></span>

<span data-ttu-id="fd785-111">Recibe un objeto [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) que representa el dispositivo de servidor.</span><span class="sxs-lookup"><span data-stu-id="fd785-111">Receives a [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) object that represents the server device.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd785-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd785-112">Requirements</span></span>



| <span data-ttu-id="fd785-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd785-113">Requirement</span></span> | <span data-ttu-id="fd785-114">Value</span><span class="sxs-lookup"><span data-stu-id="fd785-114">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fd785-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd785-115">Header</span></span><br/> | <dl> <span data-ttu-id="fd785-116"><dt>Asptlb. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd785-116"><dt>Asptlb.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd785-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd785-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd785-118">[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fd785-118">[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span></span>
</dt> </dl>

 

