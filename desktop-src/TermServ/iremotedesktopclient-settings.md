---
title: Propiedad de configuración IRemoteDesktopClient
description: Recupera el objeto de configuración para el cliente del contenedor de la aplicación Protocolo de escritorio remoto (RDP).
ms.assetid: 59999489-9ad0-4b85-9643-3b8355b817c2
ms.tgt_platform: multiple
keywords:
- Propiedad de configuración Servicios de Escritorio remoto
- Propiedad settings Servicios de Escritorio remoto, interfaz IRemoteDesktopClient
- Servicios de Escritorio remoto de la interfaz IRemoteDesktopClient, propiedad settings
topic_type:
- apiref
api_name:
- IRemoteDesktopClient.Settings
- IRemoteDesktopClient.get_Settings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e84324eaa12610d7ab898cbcb181e7712bc021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996676"
---
# <a name="iremotedesktopclientsettings-property"></a><span data-ttu-id="3344c-106">IRemoteDesktopClient:: Settings (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3344c-106">IRemoteDesktopClient::Settings property</span></span>

<span data-ttu-id="3344c-107">Recupera el objeto de configuración para el cliente del contenedor de la aplicación Protocolo de escritorio remoto (RDP).</span><span class="sxs-lookup"><span data-stu-id="3344c-107">Retrieves the settings object for the Remote Desktop Protocol (RDP) app container client.</span></span>

<span data-ttu-id="3344c-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3344c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3344c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3344c-109">Syntax</span></span>


```C++
HRESULT get_Settings(
  [out, retval] IRemoteDesktopClientSettings **Settings
);
```



## <a name="property-value"></a><span data-ttu-id="3344c-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3344c-110">Property value</span></span>

<span data-ttu-id="3344c-111">El objeto de configuración para el cliente RDP.</span><span class="sxs-lookup"><span data-stu-id="3344c-111">The settings object for the RDP client.</span></span>

## <a name="requirements"></a><span data-ttu-id="3344c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3344c-112">Requirements</span></span>



| <span data-ttu-id="3344c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3344c-113">Requirement</span></span> | <span data-ttu-id="3344c-114">Value</span><span class="sxs-lookup"><span data-stu-id="3344c-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3344c-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3344c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3344c-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3344c-116">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="3344c-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3344c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3344c-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3344c-118">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="3344c-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3344c-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="3344c-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3344c-120"><dt>MsTscAx.dll</dt></span></span> </dl>  |
| <span data-ttu-id="3344c-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3344c-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3344c-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3344c-122"><dt>MsTscAx.dll</dt></span></span> </dl>  |
| <span data-ttu-id="3344c-123">IID</span><span class="sxs-lookup"><span data-stu-id="3344c-123">IID</span></span><br/>                      | <span data-ttu-id="3344c-124">IID \_ IRemoteDesktopClient se define como 57D25668-625A-4905-BE4E-304CAA13F89C</span><span class="sxs-lookup"><span data-stu-id="3344c-124">IID\_IRemoteDesktopClient is defined as 57D25668-625A-4905-BE4E-304CAA13F89C</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3344c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="3344c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3344c-126">**IRemoteDesktopClient**</span><span class="sxs-lookup"><span data-stu-id="3344c-126">**IRemoteDesktopClient**</span></span>](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
</dt> </dl>

 

