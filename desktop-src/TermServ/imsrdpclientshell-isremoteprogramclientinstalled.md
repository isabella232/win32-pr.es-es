---
title: Propiedad IsRemoteProgramClientInstalled de IMsRdpClientShell
description: Recupera si el cliente Conexión a Escritorio remoto (RDC) admite la funcionalidad de RemoteApp de Windows Server 2008 R2.
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad IsRemoteProgramClientInstalled
- Propiedad IsRemoteProgramClientInstalled Servicios de Escritorio remoto, interfaz IMsRdpClientShell
- Servicios de Escritorio remoto de la interfaz IMsRdpClientShell, propiedad IsRemoteProgramClientInstalled
topic_type:
- apiref
api_name:
- IMsRdpClientShell.IsRemoteProgramClientInstalled
- IMsRdpClientShell.get_IsRemoteProgramClientInstalled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787d45f10e109a89429be5032fda245aa3609567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150088"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a><span data-ttu-id="fc8d4-106">IMsRdpClientShell:: IsRemoteProgramClientInstalled (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fc8d4-106">IMsRdpClientShell::IsRemoteProgramClientInstalled property</span></span>

<span data-ttu-id="fc8d4-107">Recupera si el cliente Conexión a Escritorio remoto (RDC) admite la funcionalidad de RemoteApp de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-107">Retrieves whether the Remote Desktop Connection (RDC) client supports Windows Server 2008 R2 RemoteApp functionality.</span></span>

<span data-ttu-id="fc8d4-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc8d4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc8d4-109">Syntax</span></span>


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a><span data-ttu-id="fc8d4-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fc8d4-110">Property value</span></span>

<span data-ttu-id="fc8d4-111">Recupera si el cliente Conexión a Escritorio remoto (RDC) admite la funcionalidad de RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fc8d4-111">Retrieves whether the Remote Desktop Connection (RDC) client supports RemoteApp functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc8d4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc8d4-112">Requirements</span></span>



| <span data-ttu-id="fc8d4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc8d4-113">Requirement</span></span> | <span data-ttu-id="fc8d4-114">Value</span><span class="sxs-lookup"><span data-stu-id="fc8d4-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8d4-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc8d4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fc8d4-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc8d4-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fc8d4-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc8d4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fc8d4-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc8d4-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fc8d4-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fc8d4-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="fc8d4-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc8d4-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fc8d4-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fc8d4-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc8d4-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc8d4-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fc8d4-123">IID</span><span class="sxs-lookup"><span data-stu-id="fc8d4-123">IID</span></span><br/>                      | <span data-ttu-id="fc8d4-124">IID \_ IMsRdpClientShell se define como d012ae6d-c19a-4bfe-B367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="fc8d4-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="fc8d4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc8d4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc8d4-126">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="fc8d4-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





