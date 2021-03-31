---
title: Propiedad GetRemoteMonitorsBoundingBox de IMsRdpClientNonScriptable5
description: Especifica el rectángulo delimitador del monitor remoto.
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GetRemoteMonitorsBoundingBox
- Propiedad GetRemoteMonitorsBoundingBox Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad GetRemoteMonitorsBoundingBox
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.GetRemoteMonitorsBoundingBox
- IMsRdpClientNonScriptable5.get_GetRemoteMonitorsBoundingBox
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f67192b78c734359fc6113969eb5eb410e1bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996681"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a><span data-ttu-id="0cdd4-106">IMsRdpClientNonScriptable5:: GetRemoteMonitorsBoundingBox (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0cdd4-106">IMsRdpClientNonScriptable5::GetRemoteMonitorsBoundingBox property</span></span>

<span data-ttu-id="0cdd4-107">Especifica el rectángulo delimitador del monitor remoto.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-107">Specifies the bounding rectangle of the remote monitor.</span></span>

<span data-ttu-id="0cdd4-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cdd4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0cdd4-109">Syntax</span></span>


```C++
HRESULT get_GetRemoteMonitorsBoundingBox(
  [out] LONG *pLeft,
  [out] LONG *pTop,
  [out] LONG *pRight,
  [out] LONG *pBottom
);
```



## <a name="property-value"></a><span data-ttu-id="0cdd4-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0cdd4-110">Property value</span></span>

<span data-ttu-id="0cdd4-111">Recibe el borde izquierdo del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-111">Receives the left edge of the rectangle.</span></span>

<span data-ttu-id="0cdd4-112">Recibe el borde superior del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-112">Receives the top edge of the rectangle.</span></span>

<span data-ttu-id="0cdd4-113">Recibe el borde derecho del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-113">Receives the right edge of the rectangle.</span></span>

<span data-ttu-id="0cdd4-114">Recibe el borde inferior del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-114">Receives the bottom edge of the rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cdd4-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0cdd4-115">Remarks</span></span>

<span data-ttu-id="0cdd4-116">Todas las coordenadas están en coordenadas de la pantalla virtual, que son relativas a la esquina superior izquierda del monitor principal.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-116">All coordinates are in virtual screen coordinates, which are relative to the upper-left corner of the primary monitor.</span></span> <span data-ttu-id="0cdd4-117">Si no es el monitor principal, algunos o todos estos valores pueden ser negativos.</span><span class="sxs-lookup"><span data-stu-id="0cdd4-117">If this is not the primary monitor, some or all of these values may be negative.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cdd4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cdd4-118">Requirements</span></span>



| <span data-ttu-id="0cdd4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cdd4-119">Requirement</span></span> | <span data-ttu-id="0cdd4-120">Value</span><span class="sxs-lookup"><span data-stu-id="0cdd4-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cdd4-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cdd4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0cdd4-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0cdd4-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0cdd4-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cdd4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0cdd4-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0cdd4-124">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="0cdd4-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0cdd4-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="0cdd4-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cdd4-126"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="0cdd4-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0cdd4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cdd4-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cdd4-128"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="0cdd4-129">IID</span><span class="sxs-lookup"><span data-stu-id="0cdd4-129">IID</span></span><br/>                      | <span data-ttu-id="0cdd4-130">IID \_ IMsRdpClientNonScriptable5 se define como 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="0cdd4-130">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0cdd4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cdd4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cdd4-132">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="0cdd4-132">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





