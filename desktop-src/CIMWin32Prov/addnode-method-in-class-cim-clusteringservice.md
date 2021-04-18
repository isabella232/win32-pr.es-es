---
description: Incorpora un nuevo sistema informático a un clúster.
ms.assetid: 26d9428e-99de-4dcb-96ed-d773f28e015a
ms.tgt_platform: multiple
title: Método AddNode de la clase CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.AddNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1769ebb876fd2ae99c800a61b80d339a850ab232
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659532"
---
# <a name="addnode-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="a5f78-103">Método AddNode de la \_ clase ClusteringService de CIM</span><span class="sxs-lookup"><span data-stu-id="a5f78-103">AddNode method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="a5f78-104">El método **AddNode** pone un nuevo sistema de equipo en un clúster.</span><span class="sxs-lookup"><span data-stu-id="a5f78-104">The **AddNode** method brings a new computer system into a cluster.</span></span> <span data-ttu-id="a5f78-105">El nodo que se va a agregar se especifica como un parámetro para el método.</span><span class="sxs-lookup"><span data-stu-id="a5f78-105">The node to be added is specified as a parameter to the method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5f78-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a5f78-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a5f78-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a5f78-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a5f78-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="a5f78-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a5f78-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a5f78-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f78-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5f78-110">Syntax</span></span>


```mof
uint32 AddNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a><span data-ttu-id="a5f78-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5f78-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5f78-112">*CS* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a5f78-112">*CS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f78-113">Referencia al sistema del equipo que se va a agregar al clúster.</span><span class="sxs-lookup"><span data-stu-id="a5f78-113">Reference to the computer system to add to the cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5f78-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5f78-114">Return value</span></span>

<span data-ttu-id="a5f78-115">Devuelve un valor de 0 (cero) si se realiza correctamente, 1 (uno) si no se admite la operación y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="a5f78-115">Returns a value of 0 (zero) on success, 1 (one) if the operation is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5f78-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5f78-116">Remarks</span></span>

<span data-ttu-id="a5f78-117">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="a5f78-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a5f78-118">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="a5f78-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a5f78-119">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a5f78-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a5f78-120">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a5f78-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5f78-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5f78-121">Requirements</span></span>



| <span data-ttu-id="a5f78-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5f78-122">Requirement</span></span> | <span data-ttu-id="a5f78-123">Value</span><span class="sxs-lookup"><span data-stu-id="a5f78-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f78-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5f78-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a5f78-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5f78-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a5f78-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5f78-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a5f78-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5f78-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a5f78-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a5f78-128">Namespace</span></span><br/>                | <span data-ttu-id="a5f78-129">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a5f78-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a5f78-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a5f78-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5f78-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5f78-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5f78-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a5f78-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5f78-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5f78-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5f78-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5f78-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5f78-135">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="a5f78-135">**CIM\_ClusteringService**</span></span>](addnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="a5f78-136">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="a5f78-136">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

