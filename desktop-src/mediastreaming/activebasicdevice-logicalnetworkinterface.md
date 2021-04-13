---
title: Propiedad ActiveBasicDevice LogicalNetworkInterface (PlayToDevice. h)
description: Obtiene el identificador de la interfaz de red lógica.
ms.assetid: 47C2E0BE-D3E3-4A9F-9FC6-873882811506
keywords:
- Propiedad LogicalNetworkInterface API de streaming de multimedia
- Propiedad LogicalNetworkInterface API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, propiedad LogicalNetworkInterface
topic_type:
- apiref
api_name:
- ActiveBasicDevice.LogicalNetworkInterface
- ActiveBasicDevice.get_LogicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95a87f2951ea09a0bba3d56da50b8f77a9d4a980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422238"
---
# <a name="activebasicdevicelogicalnetworkinterface-property"></a><span data-ttu-id="4e029-106">ActiveBasicDevice:: LogicalNetworkInterface (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4e029-106">ActiveBasicDevice::LogicalNetworkInterface property</span></span>

<span data-ttu-id="4e029-107">Obtiene el identificador de la interfaz de red lógica.</span><span class="sxs-lookup"><span data-stu-id="4e029-107">Gets the id of the logical network interface.</span></span>

<span data-ttu-id="4e029-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4e029-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e029-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e029-109">Syntax</span></span>


```C++
HRESULT get_LogicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a><span data-ttu-id="4e029-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4e029-110">Property value</span></span>

<span data-ttu-id="4e029-111">Un puntero a un **GUID** que especifica el identificador de la interfaz de red lógica.</span><span class="sxs-lookup"><span data-stu-id="4e029-111">A pointer to a **GUID** that specifies the id of the logical network interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e029-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e029-112">Requirements</span></span>



| <span data-ttu-id="4e029-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e029-113">Requirement</span></span> | <span data-ttu-id="4e029-114">Value</span><span class="sxs-lookup"><span data-stu-id="4e029-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e029-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e029-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4e029-116">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="4e029-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4e029-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e029-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4e029-118">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e029-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4e029-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e029-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e029-120"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e029-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e029-121">IDL</span><span class="sxs-lookup"><span data-stu-id="4e029-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4e029-122"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4e029-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="4e029-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e029-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e029-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e029-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e029-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e029-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="4e029-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4e029-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

