---
title: Propiedad RemoteMonitorLayoutMatchesLocal de IMsRdpClientNonScriptable5
description: Especifica si el diseño del monitor remoto es idéntico al diseño del monitor local.
ms.assetid: 8F3C6650-870C-417C-82FC-E145FC360012
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RemoteMonitorLayoutMatchesLocal
- Propiedad RemoteMonitorLayoutMatchesLocal Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad RemoteMonitorLayoutMatchesLocal
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.RemoteMonitorLayoutMatchesLocal
- IMsRdpClientNonScriptable5.get_RemoteMonitorLayoutMatchesLocal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5018b22865cc683fc9231c857a1b99b8acbfeca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150599"
---
# <a name="imsrdpclientnonscriptable5remotemonitorlayoutmatcheslocal-property"></a><span data-ttu-id="3459e-106">IMsRdpClientNonScriptable5:: RemoteMonitorLayoutMatchesLocal (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3459e-106">IMsRdpClientNonScriptable5::RemoteMonitorLayoutMatchesLocal property</span></span>

<span data-ttu-id="3459e-107">Especifica si el diseño del monitor remoto es idéntico al diseño del monitor local.</span><span class="sxs-lookup"><span data-stu-id="3459e-107">Specifies if the remote monitor layout is identical to the local monitor layout.</span></span> <span data-ttu-id="3459e-108">Si esta propiedad contiene **Variant \_ true**, el diseño del monitor remoto es idéntico al diseño del monitor local.</span><span class="sxs-lookup"><span data-stu-id="3459e-108">If this property contains **VARIANT\_TRUE**, the remote monitor layout is identical to the local monitor layout.</span></span> <span data-ttu-id="3459e-109">Si esta propiedad contiene **Variant \_ false**, los monitores remotos y locales tienen diseños diferentes.</span><span class="sxs-lookup"><span data-stu-id="3459e-109">If this property contains **VARIANT\_FALSE**, the remote and local monitors have different layouts.</span></span>

<span data-ttu-id="3459e-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3459e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3459e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3459e-111">Syntax</span></span>


```C++
HRESULT get_RemoteMonitorLayoutMatchesLocal(
  [out, retval] VARIANT_BOOL *pfRemoteMatchesLocal
);
```



## <a name="property-value"></a><span data-ttu-id="3459e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3459e-112">Property value</span></span>

<span data-ttu-id="3459e-113">Recibe el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3459e-113">Receives the property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3459e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3459e-114">Requirements</span></span>



| <span data-ttu-id="3459e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3459e-115">Requirement</span></span> | <span data-ttu-id="3459e-116">Value</span><span class="sxs-lookup"><span data-stu-id="3459e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3459e-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3459e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3459e-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3459e-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3459e-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3459e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3459e-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3459e-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="3459e-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3459e-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="3459e-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3459e-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="3459e-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3459e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3459e-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3459e-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="3459e-125">IID</span><span class="sxs-lookup"><span data-stu-id="3459e-125">IID</span></span><br/>                      | <span data-ttu-id="3459e-126">IID \_ IMsRdpClientNonScriptable5 se define como 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="3459e-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3459e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3459e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3459e-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="3459e-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





