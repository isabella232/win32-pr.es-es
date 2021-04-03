---
description: El método EvictNode quita un equipo de un clúster. El nodo que se va a expulsar se especifica como un parámetro para el método.
ms.assetid: 4691d536-ade3-4a02-bc28-e31ebaf5d9e4
ms.tgt_platform: multiple
title: Método EvictNode de la clase CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.EvictNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d68ddc1adc0af335dcf2d4139cf7c1f0a381d986
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807255"
---
# <a name="evictnode-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="168f4-104">Método EvictNode de la \_ clase ClusteringService de CIM</span><span class="sxs-lookup"><span data-stu-id="168f4-104">EvictNode method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="168f4-105">El método **EvictNode** quita un equipo de un clúster.</span><span class="sxs-lookup"><span data-stu-id="168f4-105">The **EvictNode** method removes a computer system from a cluster.</span></span> <span data-ttu-id="168f4-106">El nodo que se va a expulsar se especifica como un parámetro para el método.</span><span class="sxs-lookup"><span data-stu-id="168f4-106">The node to be evicted is specified as a parameter to the method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="168f4-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="168f4-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="168f4-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="168f4-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="168f4-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="168f4-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="168f4-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="168f4-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="168f4-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="168f4-111">Syntax</span></span>


```mof
uint32 EvictNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a><span data-ttu-id="168f4-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="168f4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="168f4-113">*CS* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="168f4-113">*CS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="168f4-114">Referencia al sistema del equipo que se va a quitar del clúster.</span><span class="sxs-lookup"><span data-stu-id="168f4-114">Reference to the computer system to remove from the cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="168f4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="168f4-115">Return value</span></span>

<span data-ttu-id="168f4-116">Devuelve 0 (cero) si se expulsa correctamente el sistema del equipo, 1 (uno) si no se admite el método, y cualquier otro número si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="168f4-116">Returns 0 (zero) if the computer system is successfully evicted, 1 (one) if the method is not supported, and any other number if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="168f4-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="168f4-117">Remarks</span></span>

<span data-ttu-id="168f4-118">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="168f4-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="168f4-119">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="168f4-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="168f4-120">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="168f4-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="168f4-121">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="168f4-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="168f4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="168f4-122">Requirements</span></span>



| <span data-ttu-id="168f4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="168f4-123">Requirement</span></span> | <span data-ttu-id="168f4-124">Value</span><span class="sxs-lookup"><span data-stu-id="168f4-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="168f4-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="168f4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="168f4-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="168f4-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="168f4-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="168f4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="168f4-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="168f4-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="168f4-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="168f4-129">Namespace</span></span><br/>                | <span data-ttu-id="168f4-130">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="168f4-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="168f4-131">MOF</span><span class="sxs-lookup"><span data-stu-id="168f4-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="168f4-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="168f4-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="168f4-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="168f4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="168f4-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="168f4-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="168f4-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="168f4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="168f4-136">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="168f4-136">**CIM\_ClusteringService**</span></span>](evictnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="168f4-137">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="168f4-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

