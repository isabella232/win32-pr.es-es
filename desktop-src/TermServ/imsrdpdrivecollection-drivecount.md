---
title: Propiedad DriveCount de IMsRdpDriveCollection
description: Recupera el recuento de objetos de la colección. | Propiedad DriveCount de IMsRdpDriveCollection
ms.assetid: 33b39657-2cc1-4f1e-b23a-809a9737ed8d
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DriveCount
- Propiedad DriveCount Servicios de Escritorio remoto, interfaz IMsRdpDriveCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpDriveCollection, propiedad DriveCount
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveCount
- IMsRdpDriveCollection.get_DriveCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af724344cd7d88676483c13d1a6a8cfeb8548294
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689846"
---
# <a name="imsrdpdrivecollectiondrivecount-property"></a><span data-ttu-id="a3269-107">IMsRdpDriveCollection::D propiedad riveCount</span><span class="sxs-lookup"><span data-stu-id="a3269-107">IMsRdpDriveCollection::DriveCount property</span></span>

<span data-ttu-id="a3269-108">Recupera el recuento de objetos de la colección.</span><span class="sxs-lookup"><span data-stu-id="a3269-108">Retrieves the count of objects in the collection.</span></span>

<span data-ttu-id="a3269-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a3269-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3269-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3269-110">Syntax</span></span>


```C++
HRESULT get_DriveCount(
  [out] ULONG *pDriveCount
);
```



## <a name="property-value"></a><span data-ttu-id="a3269-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a3269-111">Property value</span></span>

<span data-ttu-id="a3269-112">Recuento de objetos.</span><span class="sxs-lookup"><span data-stu-id="a3269-112">The object count.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a3269-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a3269-113">Error codes</span></span>

<span data-ttu-id="a3269-114">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="a3269-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="a3269-115">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="a3269-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3269-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3269-116">Requirements</span></span>



| <span data-ttu-id="a3269-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3269-117">Requirement</span></span> | <span data-ttu-id="a3269-118">Value</span><span class="sxs-lookup"><span data-stu-id="a3269-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3269-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3269-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a3269-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3269-120">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a3269-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3269-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a3269-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3269-122">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a3269-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a3269-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="a3269-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3269-124"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="a3269-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a3269-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3269-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3269-126"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="a3269-127">IID</span><span class="sxs-lookup"><span data-stu-id="a3269-127">IID</span></span><br/>                      | <span data-ttu-id="a3269-128">IID \_ IMsRdpDriveCollection se define como 7ff17599-da2c-4677-Ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="a3269-128">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a3269-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3269-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3269-130">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="a3269-130">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





