---
description: El método Reset de la \_ clase ManagementController de CIM solicita un restablecimiento del dispositivo lógico.
ms.assetid: 45f36ce0-6b36-4660-b841-d359e9a56ad0
ms.tgt_platform: multiple
title: Método Reset de la clase CIM_ManagementController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagementController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3314adcc12a4fd0cd1b44f197a37f5b027fce774
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659321"
---
# <a name="reset-method-of-the-cim_managementcontroller-class"></a><span data-ttu-id="93eab-103">Método Reset de la \_ clase ManagementController de CIM</span><span class="sxs-lookup"><span data-stu-id="93eab-103">Reset method of the CIM\_ManagementController class</span></span>

<span data-ttu-id="93eab-104">El método **RESET** de la \_ clase ManagementController de CIM solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93eab-104">The **Reset** method of the CIM\_ManagementController class requests a reset of the logical device.</span></span> <span data-ttu-id="93eab-105">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93eab-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93eab-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="93eab-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="93eab-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="93eab-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="93eab-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93eab-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="93eab-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93eab-109">Parameters</span></span>

<span data-ttu-id="93eab-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="93eab-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="93eab-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93eab-111">Return value</span></span>

<span data-ttu-id="93eab-112">Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y otro valor si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="93eab-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="93eab-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93eab-113">Remarks</span></span>

<span data-ttu-id="93eab-114">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="93eab-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="93eab-115">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="93eab-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="93eab-116">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="93eab-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="93eab-117">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="93eab-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="93eab-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93eab-118">Requirements</span></span>



| <span data-ttu-id="93eab-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="93eab-119">Requirement</span></span> | <span data-ttu-id="93eab-120">Value</span><span class="sxs-lookup"><span data-stu-id="93eab-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93eab-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93eab-121">Minimum supported client</span></span><br/> | <span data-ttu-id="93eab-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93eab-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93eab-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93eab-123">Minimum supported server</span></span><br/> | <span data-ttu-id="93eab-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93eab-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93eab-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="93eab-125">Namespace</span></span><br/>                | <span data-ttu-id="93eab-126">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="93eab-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="93eab-127">MOF</span><span class="sxs-lookup"><span data-stu-id="93eab-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93eab-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93eab-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="93eab-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93eab-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93eab-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93eab-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93eab-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="93eab-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93eab-132">\_MANAGEMENTCONTROLLER CIM</span><span class="sxs-lookup"><span data-stu-id="93eab-132">CIM\_ManagementController</span></span>](reset-method-in-class-cim-managementcontroller.md)
</dt> <dt>

[<span data-ttu-id="93eab-133">**\_MANAGEMENTCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="93eab-133">**CIM\_ManagementController**</span></span>](cim-managementcontroller.md)
</dt> </dl>

 

 




