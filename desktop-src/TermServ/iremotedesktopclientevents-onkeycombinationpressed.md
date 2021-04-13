---
title: IRemoteDesktopClientEvents OnKeyCombinationPressed, método
description: Se le llama cuando se presionan combinaciones de teclas especiales en la sesión remota.
ms.assetid: 0A4EAD6C-5DA9-4ED3-BA79-92AE5AE81C9F
ms.tgt_platform: multiple
keywords:
- Método OnKeyCombinationPressed Servicios de Escritorio remoto
- Método OnKeyCombinationPressed Servicios de Escritorio remoto, interfaz IRemoteDesktopClientEvents
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto, método OnKeyCombinationPressed
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnKeyCombinationPressed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192cad6323578a9bde9fe38af1d2b1d2cf83473c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422129"
---
# <a name="iremotedesktopclienteventsonkeycombinationpressed-method"></a><span data-ttu-id="861df-106">IRemoteDesktopClientEvents:: OnKeyCombinationPressed (método)</span><span class="sxs-lookup"><span data-stu-id="861df-106">IRemoteDesktopClientEvents::OnKeyCombinationPressed method</span></span>

<span data-ttu-id="861df-107">Se le llama cuando se presionan combinaciones de teclas especiales en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="861df-107">Called when special key combinations are pressed in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="861df-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="861df-108">Syntax</span></span>


```C++
void OnKeyCombinationPressed(
  [in] long keyCombination
);
```



## <a name="parameters"></a><span data-ttu-id="861df-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="861df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="861df-110">*keyCombination* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="861df-110">*keyCombination* \[in\]</span></span>
<span data-ttu-id="861df-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="861df-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="861df-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="861df-112">Return value</span></span>

<span data-ttu-id="861df-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="861df-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="861df-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="861df-114">Requirements</span></span>



| <span data-ttu-id="861df-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="861df-115">Requirement</span></span> | <span data-ttu-id="861df-116">Value</span><span class="sxs-lookup"><span data-stu-id="861df-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="861df-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="861df-117">Minimum supported client</span></span><br/> | <span data-ttu-id="861df-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="861df-118">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="861df-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="861df-119">Minimum supported server</span></span><br/> | <span data-ttu-id="861df-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="861df-120">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="861df-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="861df-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="861df-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="861df-122"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="861df-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="861df-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="861df-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="861df-124"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="861df-125">IID</span><span class="sxs-lookup"><span data-stu-id="861df-125">IID</span></span><br/>                      | <span data-ttu-id="861df-126">DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="861df-126">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="861df-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="861df-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="861df-128">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="861df-128">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





