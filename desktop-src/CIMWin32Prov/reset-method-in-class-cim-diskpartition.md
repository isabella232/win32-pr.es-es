---
description: El método Reset solicita un restablecimiento del dispositivo lógico. Este método se hereda del LogicalDevice de CIM \_ .
ms.assetid: 874f8eb4-784a-41ab-9c58-9e48486a7f71
ms.tgt_platform: multiple
title: Método Reset de la clase CIM_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskPartition.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 236a8c018b584fbc2d5ef1d13b0429d946b868fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274863"
---
# <a name="reset-method-of-the-cim_diskpartition-class"></a><span data-ttu-id="e7af0-104">Método Reset de la \_ clase DiskPartition de CIM</span><span class="sxs-lookup"><span data-stu-id="e7af0-104">Reset method of the CIM\_DiskPartition class</span></span>

<span data-ttu-id="e7af0-105">El método **RESET** solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e7af0-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="e7af0-106">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e7af0-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7af0-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="e7af0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e7af0-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e7af0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e7af0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7af0-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="e7af0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7af0-110">Parameters</span></span>

<span data-ttu-id="e7af0-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e7af0-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7af0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7af0-112">Return value</span></span>

<span data-ttu-id="e7af0-113">Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y otro valor si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="e7af0-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7af0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7af0-114">Remarks</span></span>

<span data-ttu-id="e7af0-115">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="e7af0-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e7af0-116">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="e7af0-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="e7af0-117">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="e7af0-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e7af0-118">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="e7af0-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7af0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7af0-119">Requirements</span></span>



| <span data-ttu-id="e7af0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7af0-120">Requirement</span></span> | <span data-ttu-id="e7af0-121">Value</span><span class="sxs-lookup"><span data-stu-id="e7af0-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7af0-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7af0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e7af0-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7af0-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e7af0-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7af0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e7af0-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7af0-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7af0-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e7af0-126">Namespace</span></span><br/>                | <span data-ttu-id="e7af0-127">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e7af0-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e7af0-128">MOF</span><span class="sxs-lookup"><span data-stu-id="e7af0-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7af0-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7af0-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7af0-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e7af0-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7af0-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7af0-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7af0-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7af0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7af0-133">\_DISKPARTITION CIM</span><span class="sxs-lookup"><span data-stu-id="e7af0-133">CIM\_DiskPartition</span></span>](reset-method-in-class-cim-diskpartition.md)
</dt> <dt>

[<span data-ttu-id="e7af0-134">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="e7af0-134">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> </dl>

 

 




