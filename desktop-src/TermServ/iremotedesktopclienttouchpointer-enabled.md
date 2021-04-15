---
title: Propiedad IRemoteDesktopClientTouchPointer habilitada
description: Si la característica de puntero táctil está habilitada en el control de cliente del contenedor de la aplicación RDP.
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Propiedad Enabled Servicios de Escritorio remoto
- Servicios de Escritorio remoto de propiedad habilitada, interfaz IRemoteDesktopClientTouchPointer
- Interfaz IRemoteDesktopClientTouchPointer Servicios de Escritorio remoto, propiedad Enabled
topic_type:
- apiref
api_name:
- IRemoteDesktopClientTouchPointer.Enabled
- IRemoteDesktopClientTouchPointer.get_Enabled
- IRemoteDesktopClientTouchPointer.put_Enabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd534a9f8ec77903f196bbdfa10e1823a18dff4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686062"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a><span data-ttu-id="47c2d-106">IRemoteDesktopClientTouchPointer:: Enabled (propiedad)</span><span class="sxs-lookup"><span data-stu-id="47c2d-106">IRemoteDesktopClientTouchPointer::Enabled property</span></span>

<span data-ttu-id="47c2d-107">Si la característica de puntero táctil está habilitada en el control de cliente del contenedor de la aplicación RDP.</span><span class="sxs-lookup"><span data-stu-id="47c2d-107">Whether the touch pointer feature is enabled on the RDP app container client control.</span></span>

<span data-ttu-id="47c2d-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="47c2d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c2d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47c2d-109">Syntax</span></span>


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a><span data-ttu-id="47c2d-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="47c2d-110">Property value</span></span>

<span data-ttu-id="47c2d-111">**true** si está habilitada la característica de puntero táctil; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="47c2d-111">**true** if the touch pointer feature is enabled; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="47c2d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47c2d-112">Requirements</span></span>



| <span data-ttu-id="47c2d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="47c2d-113">Requirement</span></span> | <span data-ttu-id="47c2d-114">Value</span><span class="sxs-lookup"><span data-stu-id="47c2d-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47c2d-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47c2d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="47c2d-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="47c2d-116">Windows 8</span></span><br/>                                                                                |
| <span data-ttu-id="47c2d-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47c2d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="47c2d-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="47c2d-118">Windows Server 2012</span></span><br/>                                                                      |
| <span data-ttu-id="47c2d-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="47c2d-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="47c2d-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47c2d-120"><dt>MsTscAx.dll</dt></span></span> </dl>              |
| <span data-ttu-id="47c2d-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="47c2d-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47c2d-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47c2d-122"><dt>MsTscAx.dll</dt></span></span> </dl>              |
| <span data-ttu-id="47c2d-123">IID</span><span class="sxs-lookup"><span data-stu-id="47c2d-123">IID</span></span><br/>                      | <span data-ttu-id="47c2d-124">IID \_ IRemoteDesktopClientTouchPointer se define como 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9</span><span class="sxs-lookup"><span data-stu-id="47c2d-124">IID\_IRemoteDesktopClientTouchPointer is defined as 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47c2d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="47c2d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c2d-126">**IRemoteDesktopClientTouchPointer**</span><span class="sxs-lookup"><span data-stu-id="47c2d-126">**IRemoteDesktopClientTouchPointer**</span></span>](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer)
</dt> </dl>

 

