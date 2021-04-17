---
title: Propiedad SecuredSettingsEnabled de IMsRdpClientShell2
description: Recupera un valor que indica si la página web actual está en una zona de seguridad de direcciones URL de Internet Explorer de confianza.
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto, interfaz IMsRdpClientShell2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientShell2, propiedad SecuredSettingsEnabled
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.SecuredSettingsEnabled
- IMsRdpClientShell2.get_SecuredSettingsEnabled
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1009759051207db7e6b8d741c1dd91e3de1ffc36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676930"
---
# <a name="imsrdpclientshell2securedsettingsenabled-property"></a><span data-ttu-id="3d28b-106">IMsRdpClientShell2:: SecuredSettingsEnabled (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3d28b-106">IMsRdpClientShell2::SecuredSettingsEnabled property</span></span>

<span data-ttu-id="3d28b-107">Recupera un valor que indica si la página web actual está en una zona de seguridad de direcciones URL de Internet Explorer de confianza.</span><span class="sxs-lookup"><span data-stu-id="3d28b-107">Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span>

<span data-ttu-id="3d28b-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3d28b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d28b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d28b-109">Syntax</span></span>


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="3d28b-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3d28b-110">Property value</span></span>

<span data-ttu-id="3d28b-111">Un puntero a un valor booleano que indica si la página web actual está en una zona de seguridad de dirección URL de Internet Explorer de confianza.</span><span class="sxs-lookup"><span data-stu-id="3d28b-111">A pointer to a Boolean value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d28b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d28b-112">Requirements</span></span>



| <span data-ttu-id="3d28b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d28b-113">Requirement</span></span> | <span data-ttu-id="3d28b-114">Value</span><span class="sxs-lookup"><span data-stu-id="3d28b-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d28b-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d28b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3d28b-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d28b-116">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3d28b-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d28b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3d28b-118">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3d28b-118">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="3d28b-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d28b-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d28b-120"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d28b-120"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d28b-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d28b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d28b-122">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="3d28b-122">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

 





