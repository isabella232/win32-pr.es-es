---
title: Propiedad UseRedirectionServerName de IMsRdpPreferredRedirectionInfo
description: Obtiene y establece si se utiliza el nombre del servidor de redirección.
ms.assetid: D2239600-D75D-40FB-A6D0-4C7C4C5163E3
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad UseRedirectionServerName
- Propiedad UseRedirectionServerName Servicios de Escritorio remoto, interfaz IMsRdpPreferredRedirectionInfo
- Servicios de Escritorio remoto de la interfaz IMsRdpPreferredRedirectionInfo, propiedad UseRedirectionServerName
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo.UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.get_UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.put_UseRedirectionServerName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1635273078a2d09ca01c219ebf7eaa482eeb7a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801718"
---
# <a name="imsrdppreferredredirectioninfouseredirectionservername-property"></a><span data-ttu-id="eadda-106">IMsRdpPreferredRedirectionInfo:: UseRedirectionServerName (propiedad)</span><span class="sxs-lookup"><span data-stu-id="eadda-106">IMsRdpPreferredRedirectionInfo::UseRedirectionServerName property</span></span>

<span data-ttu-id="eadda-107">Obtiene y establece si se utiliza el nombre del servidor de redirección.</span><span class="sxs-lookup"><span data-stu-id="eadda-107">Gets and sets whether to use the redirection server name.</span></span>

<span data-ttu-id="eadda-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="eadda-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="eadda-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eadda-109">Syntax</span></span>


```C++
HRESULT put_UseRedirectionServerName(
  [in]  VARIANT_BOOL UseRedirectionServerName
);

HRESULT get_UseRedirectionServerName(
  [out] VARIANT_BOOL *UseRedirectionServerName
);
```



## <a name="property-value"></a><span data-ttu-id="eadda-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="eadda-110">Property value</span></span>

<span data-ttu-id="eadda-111">Indica si se va a usar el nombre del servidor de redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="eadda-111">Whether to use the redirection server name.</span></span>

## <a name="requirements"></a><span data-ttu-id="eadda-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eadda-112">Requirements</span></span>



| <span data-ttu-id="eadda-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="eadda-113">Requirement</span></span> | <span data-ttu-id="eadda-114">Value</span><span class="sxs-lookup"><span data-stu-id="eadda-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eadda-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eadda-115">Minimum supported client</span></span><br/> | <span data-ttu-id="eadda-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="eadda-116">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="eadda-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eadda-117">Minimum supported server</span></span><br/> | <span data-ttu-id="eadda-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eadda-118">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="eadda-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="eadda-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="eadda-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eadda-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="eadda-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eadda-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eadda-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eadda-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="eadda-123">IID</span><span class="sxs-lookup"><span data-stu-id="eadda-123">IID</span></span><br/>                      | <span data-ttu-id="eadda-124">IID \_ IMsRdpPreferredRedirectionInfo se define como FDD029F9-9574-4DEF-8529-64B521CCCAA4</span><span class="sxs-lookup"><span data-stu-id="eadda-124">IID\_IMsRdpPreferredRedirectionInfo is defined as FDD029F9-9574-4DEF-8529-64B521CCCAA4</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eadda-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="eadda-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eadda-126">**IMsRdpPreferredRedirectionInfo**</span><span class="sxs-lookup"><span data-stu-id="eadda-126">**IMsRdpPreferredRedirectionInfo**</span></span>](imsrdppreferredredirectioninfo.md)
</dt> </dl>

 

 





