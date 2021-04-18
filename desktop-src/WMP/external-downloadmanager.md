---
title: External. DownloadManager
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad DownloadManager recupera el objeto DownloadManager.
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- Media Player de Windows externa. DownloadManager
topic_type:
- apiref
api_name:
- External.DownloadManager
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55e6371f5c8d1e5dfcb17762340a82e8d921c17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699762"
---
# <a name="externaldownloadmanager"></a><span data-ttu-id="ea9ab-106">External. DownloadManager</span><span class="sxs-lookup"><span data-stu-id="ea9ab-106">External.DownloadManager</span></span>

> [!Note]  
> <span data-ttu-id="ea9ab-107">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="ea9ab-108">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="ea9ab-109">La propiedad **Downloadmanager** recupera el objeto **Downloadmanager** .</span><span class="sxs-lookup"><span data-stu-id="ea9ab-109">The **DownloadManager** property retrieves the **DownloadManager** object.</span></span>

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a><span data-ttu-id="ea9ab-110">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="ea9ab-110">Possible Values</span></span>

<span data-ttu-id="ea9ab-111">Esta propiedad es un objeto **Downloadmanager** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-111">This property is a read-only **DownloadManager** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea9ab-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea9ab-112">Remarks</span></span>

<span data-ttu-id="ea9ab-113">En Windows Media Player 10 o versiones posteriores, solo se puede tener acceso a la propiedad y el objeto **Downloadmanager** desde los paneles de tareas servicio de tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-113">In Windows Media Player 10 or later, the **DownloadManager** property and object are accessible only from online store service task panes.</span></span> <span data-ttu-id="ea9ab-114">No se puede usar el **Downloadmanager** de otras características en las que el objeto **externo** está disponible, como HTMLView, la vista del centro de información y la información del álbum.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-114">You cannot use the **DownloadManager** from other features where the **External** object is available, such as HTMLView, Info Center View, and album information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea9ab-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea9ab-115">Requirements</span></span>



| <span data-ttu-id="ea9ab-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea9ab-116">Requirement</span></span> | <span data-ttu-id="ea9ab-117">Value</span><span class="sxs-lookup"><span data-stu-id="ea9ab-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9ab-118">Versión</span><span class="sxs-lookup"><span data-stu-id="ea9ab-118">Version</span></span><br/> | <span data-ttu-id="ea9ab-119">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="ea9ab-119">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="ea9ab-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ea9ab-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="ea9ab-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea9ab-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea9ab-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea9ab-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea9ab-123">**Objeto externo para las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="ea9ab-123">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





