---
title: Propiedad DisableRemoteAppCapsCheck de IMsRdpClientNonScriptable5
description: Especifica si el control ActiveX Escritorio remoto no debe comprobar las capacidades de RemoteApp en el servidor.
ms.assetid: dcc44d4b-ece5-4f5b-a00a-f90d7a2fa11a
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DisableRemoteAppCapsCheck
- Propiedad DisableRemoteAppCapsCheck Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad DisableRemoteAppCapsCheck
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.get_DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.put_DisableRemoteAppCapsCheck
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f65b0e1b56b3a1152f71aff25d4cf65a4420d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493180"
---
# <a name="imsrdpclientnonscriptable5disableremoteappcapscheck-property"></a><span data-ttu-id="5aa2a-106">IMsRdpClientNonScriptable5::D propiedad isableRemoteAppCapsCheck</span><span class="sxs-lookup"><span data-stu-id="5aa2a-106">IMsRdpClientNonScriptable5::DisableRemoteAppCapsCheck property</span></span>

<span data-ttu-id="5aa2a-107">Especifica si el control ActiveX Escritorio remoto no debe comprobar las capacidades de RemoteApp en el servidor.</span><span class="sxs-lookup"><span data-stu-id="5aa2a-107">Specifies whether the Remote Desktop ActiveX control should not check the server for RemoteApp capabilities.</span></span> <span data-ttu-id="5aa2a-108">Si esta propiedad contiene **Variant \_ true**, el control no debe comprobar las capacidades de RemoteApp en el servidor.</span><span class="sxs-lookup"><span data-stu-id="5aa2a-108">If this property contains **VARIANT\_TRUE**, the control should not check the server for RemoteApp capabilities.</span></span> <span data-ttu-id="5aa2a-109">Si esta propiedad contiene **Variant \_ false**, el control puede comprobar las capacidades de RemoteApp en el servidor.</span><span class="sxs-lookup"><span data-stu-id="5aa2a-109">If this property contains **VARIANT\_FALSE**, the control can check the server for RemoteApp capabilities.</span></span>

<span data-ttu-id="5aa2a-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5aa2a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa2a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5aa2a-111">Syntax</span></span>


```C++
HRESULT put_DisableRemoteAppCapsCheck(
  [in]          VARIANT_BOOL fDisableRemoteAppCapsCheck
);

HRESULT get_DisableRemoteAppCapsCheck(
  [out, retval] VARIANT_BOOL *pfDisableRemoteAppCapsCheck
);
```



## <a name="property-value"></a><span data-ttu-id="5aa2a-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5aa2a-112">Property value</span></span>

<span data-ttu-id="5aa2a-113">Especifica el nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5aa2a-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa2a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aa2a-114">Requirements</span></span>



| <span data-ttu-id="5aa2a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aa2a-115">Requirement</span></span> | <span data-ttu-id="5aa2a-116">Value</span><span class="sxs-lookup"><span data-stu-id="5aa2a-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa2a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aa2a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5aa2a-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5aa2a-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5aa2a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aa2a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5aa2a-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5aa2a-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="5aa2a-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5aa2a-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="5aa2a-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aa2a-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="5aa2a-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5aa2a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5aa2a-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aa2a-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="5aa2a-125">IID</span><span class="sxs-lookup"><span data-stu-id="5aa2a-125">IID</span></span><br/>                      | <span data-ttu-id="5aa2a-126">IID \_ IMsRdpClientNonScriptable5 se define como 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="5aa2a-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5aa2a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aa2a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa2a-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="5aa2a-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





