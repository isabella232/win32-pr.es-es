---
title: IMsRdpDriveCollection RescanDrives, método
description: Actualiza la lista de objetos de la colección. | IMsRdpDriveCollection RescanDrives, método
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- Método RescanDrives Servicios de Escritorio remoto
- Método RescanDrives Servicios de Escritorio remoto, interfaz IMsRdpDriveCollection
- Interfaz IMsRdpDriveCollection Servicios de Escritorio remoto, método RescanDrives
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.RescanDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7488187e44caeaedb7c73b01ff8a3711e20dcdd1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689724"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a><span data-ttu-id="921cb-107">IMsRdpDriveCollection:: RescanDrives (método)</span><span class="sxs-lookup"><span data-stu-id="921cb-107">IMsRdpDriveCollection::RescanDrives method</span></span>

<span data-ttu-id="921cb-108">Actualiza la lista de objetos de la colección.</span><span class="sxs-lookup"><span data-stu-id="921cb-108">Refreshes the list of objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="921cb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="921cb-109">Syntax</span></span>


```C++
HRESULT RescanDrives(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a><span data-ttu-id="921cb-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="921cb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="921cb-111">*vboolDynRedir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="921cb-111">*vboolDynRedir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="921cb-112">El estado de redirección predeterminada que se aplicará a los dispositivos o unidades recién detectados.</span><span class="sxs-lookup"><span data-stu-id="921cb-112">The default redirection state that will be applied to any newly discovered devices or drives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="921cb-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="921cb-113">Return value</span></span>

<span data-ttu-id="921cb-114">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="921cb-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="921cb-115">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="921cb-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="921cb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="921cb-116">Requirements</span></span>



| <span data-ttu-id="921cb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="921cb-117">Requirement</span></span> | <span data-ttu-id="921cb-118">Value</span><span class="sxs-lookup"><span data-stu-id="921cb-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="921cb-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="921cb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="921cb-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="921cb-120">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="921cb-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="921cb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="921cb-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="921cb-122">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="921cb-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="921cb-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="921cb-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="921cb-124"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="921cb-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="921cb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="921cb-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="921cb-126"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="921cb-127">IID</span><span class="sxs-lookup"><span data-stu-id="921cb-127">IID</span></span><br/>                      | <span data-ttu-id="921cb-128">IID \_ IMsRdpDriveCollection se define como 7ff17599-da2c-4677-Ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="921cb-128">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="921cb-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="921cb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="921cb-130">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="921cb-130">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





