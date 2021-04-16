---
title: Método SetInt32Property de la clase Win32_RDSHCollection
description: Actualiza un valor de propiedad de entero de un \_ objeto RDSHCollection de Win32.
ms.assetid: 2a9a5d83-d147-43b3-b57c-6c744da0923d
ms.tgt_platform: multiple
keywords:
- Método SetInt32Property Servicios de Escritorio remoto
- Método SetInt32Property Servicios de Escritorio remoto, clase Win32_RDSHCollection
- Win32_RDSHCollection de clase Servicios de Escritorio remoto, método SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 136bb8ccf34004f747829fb43ee8080ccd1d3132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686164"
---
# <a name="setint32property-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="b4e0a-106">Método SetInt32Property de la \_ clase RDSHCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="b4e0a-106">SetInt32Property method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="b4e0a-107">Actualiza un valor de propiedad de entero de un objeto [**\_ RDSHCollection de Win32**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="b4e0a-107">Updates an integer property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4e0a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4e0a-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="b4e0a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4e0a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4e0a-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b4e0a-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e0a-111">Clave que identifica la propiedad que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="b4e0a-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="b4e0a-112">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b4e0a-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e0a-113">Nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="b4e0a-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4e0a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4e0a-114">Return value</span></span>

<span data-ttu-id="b4e0a-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="b4e0a-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4e0a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4e0a-116">Requirements</span></span>



| <span data-ttu-id="b4e0a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4e0a-117">Requirement</span></span> | <span data-ttu-id="b4e0a-118">Value</span><span class="sxs-lookup"><span data-stu-id="b4e0a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4e0a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4e0a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b4e0a-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b4e0a-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b4e0a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4e0a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b4e0a-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4e0a-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b4e0a-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b4e0a-123">Namespace</span></span><br/>                | <span data-ttu-id="b4e0a-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="b4e0a-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b4e0a-125">MOF</span><span class="sxs-lookup"><span data-stu-id="b4e0a-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4e0a-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4e0a-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4e0a-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4e0a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4e0a-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4e0a-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b4e0a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4e0a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4e0a-130">**Win32 \_ RDSHCollection**</span><span class="sxs-lookup"><span data-stu-id="b4e0a-130">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





