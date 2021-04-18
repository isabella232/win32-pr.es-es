---
title: Propiedad AllowPromptingForCredentials de IMsRdpClientNonScriptable5
description: Especifica si el control ActiveX Escritorio remoto puede solicitar las credenciales al usuario.
ms.assetid: 9a780886-39ee-4d3b-9a54-fa209708d9f8
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AllowPromptingForCredentials
- Propiedad AllowPromptingForCredentials Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad AllowPromptingForCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.get_AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.put_AllowPromptingForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c326a83a46b41d3578c958e24fd901beb7c7b321
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686240"
---
# <a name="imsrdpclientnonscriptable5allowpromptingforcredentials-property"></a><span data-ttu-id="d595f-106">IMsRdpClientNonScriptable5:: AllowPromptingForCredentials (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d595f-106">IMsRdpClientNonScriptable5::AllowPromptingForCredentials property</span></span>

<span data-ttu-id="d595f-107">Especifica si el control ActiveX Escritorio remoto puede solicitar las credenciales al usuario.</span><span class="sxs-lookup"><span data-stu-id="d595f-107">Specifies whether the Remote Desktop ActiveX control can prompt the user for credentials.</span></span> <span data-ttu-id="d595f-108">Si esta propiedad contiene **Variant \_ true**, se puede solicitar credenciales al usuario.</span><span class="sxs-lookup"><span data-stu-id="d595f-108">If this property contains **VARIANT\_TRUE**, the user can be prompted for credentials.</span></span> <span data-ttu-id="d595f-109">Si esta propiedad contiene **Variant \_ false**, no se puede solicitar credenciales al usuario.</span><span class="sxs-lookup"><span data-stu-id="d595f-109">If this property contains **VARIANT\_FALSE**, the user cannot be prompted for credentials.</span></span>

<span data-ttu-id="d595f-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d595f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d595f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d595f-111">Syntax</span></span>


```C++
HRESULT put_AllowPromptingForCredentials(
  [in]          VARIANT_BOOL fAllow
);

HRESULT get_AllowPromptingForCredentials(
  [out, retval] VARIANT_BOOL *pfAllow
);
```



## <a name="property-value"></a><span data-ttu-id="d595f-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d595f-112">Property value</span></span>

<span data-ttu-id="d595f-113">Especifica el nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d595f-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d595f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d595f-114">Requirements</span></span>



| <span data-ttu-id="d595f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d595f-115">Requirement</span></span> | <span data-ttu-id="d595f-116">Value</span><span class="sxs-lookup"><span data-stu-id="d595f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d595f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d595f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d595f-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d595f-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d595f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d595f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d595f-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d595f-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="d595f-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d595f-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="d595f-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d595f-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d595f-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d595f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d595f-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d595f-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d595f-125">IID</span><span class="sxs-lookup"><span data-stu-id="d595f-125">IID</span></span><br/>                      | <span data-ttu-id="d595f-126">IID \_ IMsRdpClientNonScriptable5 se define como 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="d595f-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d595f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d595f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d595f-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="d595f-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





