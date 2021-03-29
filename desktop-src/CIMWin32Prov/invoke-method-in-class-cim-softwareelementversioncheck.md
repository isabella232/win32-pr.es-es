---
description: El método Invoke de la \_ clase CIM SoftwareElementVersionCheck evalúa una comprobación determinada.
ms.assetid: 5b477945-7ad4-49e2-b9c8-4a700a45f2b6
ms.tgt_platform: multiple
title: Método Invoke de la clase CIM_SoftwareElementVersionCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementVersionCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2d65921a07dd6e5ab6df54ea1ba71117c58a18dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538686"
---
# <a name="invoke-method-of-the-cim_softwareelementversioncheck-class"></a><span data-ttu-id="7556e-103">Método Invoke de la \_ clase CIM SoftwareElementVersionCheck</span><span class="sxs-lookup"><span data-stu-id="7556e-103">Invoke method of the CIM\_SoftwareElementVersionCheck class</span></span>

<span data-ttu-id="7556e-104">El método **Invoke** de la clase [**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) evalúa una comprobación determinada.</span><span class="sxs-lookup"><span data-stu-id="7556e-104">The **Invoke** method of the [**CIM\_SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="7556e-105">Los detalles de cómo evalúa el método una comprobación determinada en un contexto CIM se describen en las subclases de [**\_ comprobación CIM**](cim-check.md) no abstractas.</span><span class="sxs-lookup"><span data-stu-id="7556e-105">The details of how the method evaluates a particular check in a CIM context are described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="7556e-106">Este método se hereda de **la \_ comprobación CIM**.</span><span class="sxs-lookup"><span data-stu-id="7556e-106">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7556e-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="7556e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7556e-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7556e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7556e-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="7556e-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7556e-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7556e-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7556e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7556e-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="7556e-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7556e-112">Parameters</span></span>

<span data-ttu-id="7556e-113">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7556e-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7556e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7556e-114">Return value</span></span>

<span data-ttu-id="7556e-115">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="7556e-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7556e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7556e-116">Remarks</span></span>

<span data-ttu-id="7556e-117">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="7556e-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="7556e-118">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="7556e-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="7556e-119">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="7556e-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7556e-120">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="7556e-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7556e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7556e-121">Requirements</span></span>



| <span data-ttu-id="7556e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7556e-122">Requirement</span></span> | <span data-ttu-id="7556e-123">Value</span><span class="sxs-lookup"><span data-stu-id="7556e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7556e-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7556e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7556e-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7556e-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7556e-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7556e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7556e-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7556e-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7556e-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7556e-128">Namespace</span></span><br/>                | <span data-ttu-id="7556e-129">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7556e-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7556e-130">MOF</span><span class="sxs-lookup"><span data-stu-id="7556e-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7556e-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7556e-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7556e-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7556e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7556e-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7556e-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7556e-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="7556e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7556e-135">\_SOFTWAREELEMENTVERSIONCHECK CIM</span><span class="sxs-lookup"><span data-stu-id="7556e-135">CIM\_SoftwareElementVersionCheck</span></span>](invoke-method-in-class-cim-softwareelementversioncheck.md)
</dt> <dt>

[<span data-ttu-id="7556e-136">**\_SOFTWAREELEMENTVERSIONCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="7556e-136">**CIM\_SoftwareElementVersionCheck**</span></span>](cim-softwareelementversioncheck.md)
</dt> </dl>

 

