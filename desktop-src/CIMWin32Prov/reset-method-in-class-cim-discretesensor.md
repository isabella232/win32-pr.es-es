---
description: El método Reset solicita un restablecimiento del dispositivo lógico. Este método se hereda del LogicalDevice de CIM \_ .
ms.assetid: 4ddbad2a-e586-434a-a33e-7d60dcb67b3a
ms.tgt_platform: multiple
title: Método Reset de la clase CIM_DiscreteSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiscreteSensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d45544e62144c2d3aa14d898b5d595d3ea5b34f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806974"
---
# <a name="reset-method-of-the-cim_discretesensor-class"></a><span data-ttu-id="6f9d8-104">Método Reset de la \_ clase DiscreteSensor de CIM</span><span class="sxs-lookup"><span data-stu-id="6f9d8-104">Reset method of the CIM\_DiscreteSensor class</span></span>

<span data-ttu-id="6f9d8-105">El método **RESET** solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6f9d8-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="6f9d8-106">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f9d8-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f9d8-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="6f9d8-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6f9d8-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6f9d8-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6f9d8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f9d8-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="6f9d8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f9d8-110">Parameters</span></span>

<span data-ttu-id="6f9d8-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6f9d8-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f9d8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f9d8-112">Return value</span></span>

<span data-ttu-id="6f9d8-113">Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y otro valor si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="6f9d8-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f9d8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f9d8-114">Remarks</span></span>

<span data-ttu-id="6f9d8-115">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="6f9d8-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="6f9d8-116">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="6f9d8-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="6f9d8-117">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="6f9d8-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6f9d8-118">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="6f9d8-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f9d8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f9d8-119">Requirements</span></span>



| <span data-ttu-id="6f9d8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f9d8-120">Requirement</span></span> | <span data-ttu-id="6f9d8-121">Value</span><span class="sxs-lookup"><span data-stu-id="6f9d8-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f9d8-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f9d8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6f9d8-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f9d8-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f9d8-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f9d8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6f9d8-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f9d8-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f9d8-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6f9d8-126">Namespace</span></span><br/>                | <span data-ttu-id="6f9d8-127">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6f9d8-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6f9d8-128">MOF</span><span class="sxs-lookup"><span data-stu-id="6f9d8-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f9d8-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f9d8-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f9d8-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f9d8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f9d8-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f9d8-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f9d8-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f9d8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f9d8-133">\_DISCRETESENSOR CIM</span><span class="sxs-lookup"><span data-stu-id="6f9d8-133">CIM\_DiscreteSensor</span></span>](reset-method-in-class-cim-discretesensor.md)
</dt> <dt>

[<span data-ttu-id="6f9d8-134">**\_DISCRETESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="6f9d8-134">**CIM\_DiscreteSensor**</span></span>](cim-discretesensor.md)
</dt> </dl>

 

 




