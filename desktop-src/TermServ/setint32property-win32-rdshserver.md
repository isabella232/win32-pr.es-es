---
title: Método SetInt32Property de la clase Win32_RDSHServer
description: Actualiza un valor de propiedad de entero de un \_ objeto RDSHServer de Win32.
ms.assetid: fa8df023-120d-4174-adc1-868f08fdce56
ms.tgt_platform: multiple
keywords:
- Método SetInt32Property Servicios de Escritorio remoto
- Método SetInt32Property Servicios de Escritorio remoto, clase Win32_RDSHServer
- Win32_RDSHServer de clase Servicios de Escritorio remoto, método SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c22c8da9c046e0a42a6ec41f6ad5b3073c8d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802125"
---
# <a name="setint32property-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="37268-106">Método SetInt32Property de la \_ clase RDSHServer de Win32</span><span class="sxs-lookup"><span data-stu-id="37268-106">SetInt32Property method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="37268-107">Actualiza un valor de propiedad de entero de un objeto [**\_ RDSHServer de Win32**](win32-rdshserver.md) .</span><span class="sxs-lookup"><span data-stu-id="37268-107">Updates an integer property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="37268-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37268-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="37268-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37268-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37268-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="37268-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37268-111">Clave que identifica la propiedad que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="37268-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="37268-112">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="37268-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37268-113">Nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="37268-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37268-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37268-114">Return value</span></span>

<span data-ttu-id="37268-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="37268-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="37268-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37268-116">Requirements</span></span>



| <span data-ttu-id="37268-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="37268-117">Requirement</span></span> | <span data-ttu-id="37268-118">Value</span><span class="sxs-lookup"><span data-stu-id="37268-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="37268-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37268-119">Minimum supported client</span></span><br/> | <span data-ttu-id="37268-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="37268-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="37268-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37268-121">Minimum supported server</span></span><br/> | <span data-ttu-id="37268-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37268-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="37268-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="37268-123">Namespace</span></span><br/>                | <span data-ttu-id="37268-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="37268-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="37268-125">MOF</span><span class="sxs-lookup"><span data-stu-id="37268-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37268-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37268-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="37268-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="37268-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37268-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37268-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="37268-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="37268-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37268-130">**Win32 \_ RDSHServer**</span><span class="sxs-lookup"><span data-stu-id="37268-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





