---
description: No se admite.
ms.assetid: 1e4c3bd4-2540-428f-9ca6-dd4c65c53434
title: 'IRenderEngine:: SetInterestRange (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetInterestRange
api_type:
- COM
api_location: ''
ms.openlocfilehash: 81ccd8c1266710e7e38fe9b79e86319e8fef7314
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494597"
---
# <a name="irenderenginesetinterestrange-method"></a><span data-ttu-id="242a6-103">IRenderEngine:: SetInterestRange (método)</span><span class="sxs-lookup"><span data-stu-id="242a6-103">IRenderEngine::SetInterestRange method</span></span>

> [!Note]  
> <span data-ttu-id="242a6-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="242a6-104">\[Deprecated.</span></span> <span data-ttu-id="242a6-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="242a6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="242a6-106">No se admite.</span><span class="sxs-lookup"><span data-stu-id="242a6-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="242a6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="242a6-107">Syntax</span></span>


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="242a6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="242a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="242a6-109">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="242a6-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="242a6-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="242a6-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="242a6-111">*Detención*</span><span class="sxs-lookup"><span data-stu-id="242a6-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="242a6-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="242a6-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="242a6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="242a6-113">Return value</span></span>

<span data-ttu-id="242a6-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="242a6-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="242a6-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="242a6-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="242a6-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="242a6-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="242a6-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="242a6-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="242a6-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="242a6-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="242a6-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="242a6-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="242a6-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="242a6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="242a6-121">**Interfaz IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="242a6-121">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> </dl>

 

 



