---
description: El método StartService pone el servicio en estado Iniciado.
ms.assetid: 2efd2a06-a03c-4f4c-b2fa-889f84faac0f
ms.tgt_platform: multiple
title: Método StartService de la clase CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8abdeffa234461952f99013524042dcbba6e682
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274972"
---
# <a name="startservice-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="c580d-103">Método StartService de la \_ clase ClusteringService de CIM</span><span class="sxs-lookup"><span data-stu-id="c580d-103">StartService method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="c580d-104">El método **StartService** pone el servicio en estado Iniciado.</span><span class="sxs-lookup"><span data-stu-id="c580d-104">The **StartService** method puts the service in a started state.</span></span> <span data-ttu-id="c580d-105">En una subclase, se puede especificar el conjunto de códigos de retorno posibles mediante un calificador **ValueMap** en el método.</span><span class="sxs-lookup"><span data-stu-id="c580d-105">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="c580d-106">Las cadenas a las que se traduce el contenido **ValueMap** también se pueden especificar en la subclase como calificador de matriz **Values** .</span><span class="sxs-lookup"><span data-stu-id="c580d-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="c580d-107">Este método se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="c580d-107">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c580d-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="c580d-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c580d-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c580d-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c580d-110">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c580d-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c580d-111">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c580d-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c580d-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c580d-112">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="c580d-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c580d-113">Parameters</span></span>

<span data-ttu-id="c580d-114">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c580d-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c580d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c580d-115">Return value</span></span>

<span data-ttu-id="c580d-116">Devuelve un valor de 0 (cero) si el servicio se inició correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="c580d-116">Returns a value of 0 (zero) if the service was successfully started, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="c580d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c580d-117">Remarks</span></span>

<span data-ttu-id="c580d-118">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="c580d-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c580d-119">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="c580d-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c580d-120">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c580d-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c580d-121">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c580d-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c580d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c580d-122">Requirements</span></span>



| <span data-ttu-id="c580d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c580d-123">Requirement</span></span> | <span data-ttu-id="c580d-124">Value</span><span class="sxs-lookup"><span data-stu-id="c580d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c580d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c580d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c580d-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c580d-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c580d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c580d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c580d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c580d-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c580d-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c580d-129">Namespace</span></span><br/>                | <span data-ttu-id="c580d-130">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c580d-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c580d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c580d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c580d-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c580d-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c580d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c580d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c580d-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c580d-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c580d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c580d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c580d-136">\_CLUSTERINGSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="c580d-136">CIM\_ClusteringService</span></span>](startservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="c580d-137">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="c580d-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

