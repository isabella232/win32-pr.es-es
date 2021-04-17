---
description: Opciones para enumerar los modos de presentación.
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: DXGI_ENUM_MODES (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056ad959f0b86fb6f357d690f2daab908275e038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670222"
---
# <a name="dxgi_enum_modes"></a><span data-ttu-id="de974-103">\_modos de enumeración de DXGI \_</span><span class="sxs-lookup"><span data-stu-id="de974-103">DXGI\_ENUM\_MODES</span></span>

<span data-ttu-id="de974-104">Opciones para enumerar los modos de presentación.</span><span class="sxs-lookup"><span data-stu-id="de974-104">Options for enumerating display modes.</span></span>



| <span data-ttu-id="de974-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="de974-105">Constant/value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="de974-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="de974-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <span data-ttu-id="de974-107"><dt>**DXGI \_ Modos de ENUMERAción \_ \_ entrelazados**</dt> <dt>1UL</dt></span><span class="sxs-lookup"><span data-stu-id="de974-107"><dt>**DXGI\_ENUM\_MODES\_INTERLACED**</dt> <dt>1UL</dt></span></span> </dl>                 | <span data-ttu-id="de974-108">Incluye modos entrelazados.</span><span class="sxs-lookup"><span data-stu-id="de974-108">Include interlaced modes.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <span data-ttu-id="de974-109"><dt>**DXGI \_ Modos de ENUMERAción \_ \_ escala**</dt> <dt>2UL</dt></span><span class="sxs-lookup"><span data-stu-id="de974-109"><dt>**DXGI\_ENUM\_MODES\_SCALING**</dt> <dt>2UL</dt></span></span> </dl>                          | <span data-ttu-id="de974-110">Incluye modos de escalado elástico.</span><span class="sxs-lookup"><span data-stu-id="de974-110">Include stretched-scaling modes.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <span data-ttu-id="de974-111"><dt>**DXGI \_ Modos de ENUMERAción \_ \_ estéreo**</dt> <dt>4UL</dt></span><span class="sxs-lookup"><span data-stu-id="de974-111"><dt>**DXGI\_ENUM\_MODES\_STEREO**</dt> <dt>4UL</dt></span></span> </dl>                             | <span data-ttu-id="de974-112">Incluye modos estereofónicos.</span><span class="sxs-lookup"><span data-stu-id="de974-112">Include stereo modes.</span></span><br/> <span data-ttu-id="de974-113">**Direct3D 11:** Este valor de enumeración se admite a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="de974-113">**Direct3D 11:** This enumeration value is supported starting with Windows 8.</span></span><br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <span data-ttu-id="de974-114"><dt>**DXGI \_ Modos de ENUMERAción 8UL \_ \_ \_ estéreo deshabilitados**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="de974-114"><dt>**DXGI\_ENUM\_MODES\_DISABLED\_STEREO**</dt> <dt>8UL</dt></span></span> </dl> | <span data-ttu-id="de974-115">Incluye modos estereofónicos que están ocultos porque el usuario ha deshabilitado el estéreo.</span><span class="sxs-lookup"><span data-stu-id="de974-115">Include stereo modes that are hidden because the user has disabled stereo.</span></span> <span data-ttu-id="de974-116">Las aplicaciones del panel de control pueden usar esta opción para mostrar las capacidades de estéreo que se han deshabilitado como parte de una interfaz de usuario que habilita y deshabilita el estéreo.</span><span class="sxs-lookup"><span data-stu-id="de974-116">Control panel applications can use this option to show stereo capabilities that have been disabled as part of a user interface that enables and disables stereo.</span></span><br/> <span data-ttu-id="de974-117">**Direct3D 11:** Este valor de enumeración se admite a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="de974-117">**Direct3D 11:** This enumeration value is supported starting with Windows 8.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="de974-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de974-118">Remarks</span></span>

<span data-ttu-id="de974-119">Estas opciones de marca se usan en [**IDXGIOutput:: GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) para enumerar los modos de presentación.</span><span class="sxs-lookup"><span data-stu-id="de974-119">These flag options are used in [**IDXGIOutput::GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) to enumerate display modes.</span></span>

<span data-ttu-id="de974-120">Estas opciones de marca también se usan en [**IDXGIOutput1:: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) para enumerar los modos de presentación.</span><span class="sxs-lookup"><span data-stu-id="de974-120">These flag options are also used in [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) to enumerate display modes.</span></span>

## <a name="requirements"></a><span data-ttu-id="de974-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de974-121">Requirements</span></span>



| <span data-ttu-id="de974-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="de974-122">Requirement</span></span> | <span data-ttu-id="de974-123">Value</span><span class="sxs-lookup"><span data-stu-id="de974-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="de974-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de974-124">Header</span></span><br/> | <dl> <span data-ttu-id="de974-125"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="de974-125"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de974-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="de974-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de974-127">Constantes de DXGI</span><span class="sxs-lookup"><span data-stu-id="de974-127">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




