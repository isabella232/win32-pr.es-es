---
title: Método GetInt32Property de la clase Win32_RDMSVirtualDesktopCollection (Microsoft. Diagnostics. appanalysis. h)
description: Recupera una propiedad de entero de una colección de escritorios virtuales.
ms.assetid: 18ffca65-e7c0-4b17-902f-d74b2a81aba2
ms.tgt_platform: multiple
keywords:
- Método GetInt32Property Servicios de Escritorio remoto
- Método GetInt32Property Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de clase Servicios de Escritorio remoto, método GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e8e5518590bece8e8b904ea56bf7572b436b66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676601"
---
# <a name="getint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="edd9f-106">Método GetInt32Property de la \_ clase RDMSVirtualDesktopCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="edd9f-106">GetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="edd9f-107">Recupera una propiedad de entero de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="edd9f-107">Retrieves an integer property from a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="edd9f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edd9f-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="edd9f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edd9f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edd9f-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="edd9f-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd9f-111">Clave que identifica la propiedad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="edd9f-111">A key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="edd9f-112">*Valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="edd9f-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edd9f-113">Entero que recibe el valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="edd9f-113">An integer that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edd9f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edd9f-114">Return value</span></span>

<span data-ttu-id="edd9f-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="edd9f-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="edd9f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edd9f-116">Requirements</span></span>



| <span data-ttu-id="edd9f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="edd9f-117">Requirement</span></span> | <span data-ttu-id="edd9f-118">Value</span><span class="sxs-lookup"><span data-stu-id="edd9f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd9f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edd9f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="edd9f-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="edd9f-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="edd9f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edd9f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="edd9f-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="edd9f-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="edd9f-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="edd9f-123">Namespace</span></span><br/>                | <span data-ttu-id="edd9f-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="edd9f-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="edd9f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edd9f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="edd9f-126"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="edd9f-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="edd9f-127">MOF</span><span class="sxs-lookup"><span data-stu-id="edd9f-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="edd9f-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="edd9f-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="edd9f-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="edd9f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edd9f-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edd9f-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="edd9f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="edd9f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edd9f-132">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="edd9f-132">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





