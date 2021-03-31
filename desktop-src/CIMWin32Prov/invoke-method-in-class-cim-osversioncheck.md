---
description: El método Invoke de la \_ clase CIM OSVersionCheck evalúa una comprobación determinada. Los detalles de cómo evalúa el método una comprobación determinada en un contexto CIM se describen en las subclases de comprobación CIM no abstractas \_ . Este método se hereda de la \_ comprobación CIM.
ms.assetid: ff06772c-e40c-49c8-b334-5ee480926245
ms.tgt_platform: multiple
title: Método Invoke de la clase CIM_OSVersionCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSVersionCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49d6944c4a28c956356fef430e47bc8636082930
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152984"
---
# <a name="invoke-method-of-the-cim_osversioncheck-class"></a><span data-ttu-id="514ef-105">Método Invoke de la \_ clase CIM OSVersionCheck</span><span class="sxs-lookup"><span data-stu-id="514ef-105">Invoke method of the CIM\_OSVersionCheck class</span></span>

<span data-ttu-id="514ef-106">El método **Invoke** de la clase [**CIM \_ OSVersionCheck**](cim-osversioncheck.md) evalúa una comprobación determinada.</span><span class="sxs-lookup"><span data-stu-id="514ef-106">The **Invoke** method of the [**CIM\_OSVersionCheck**](cim-osversioncheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="514ef-107">Los detalles de cómo evalúa el método una comprobación determinada en un contexto CIM se describen en las subclases de [**\_ comprobación CIM**](cim-check.md) no abstractas.</span><span class="sxs-lookup"><span data-stu-id="514ef-107">The details of how the method evaluates a particular check in a CIM context is described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="514ef-108">Este método se hereda de **la \_ comprobación CIM**.</span><span class="sxs-lookup"><span data-stu-id="514ef-108">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="514ef-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="514ef-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="514ef-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="514ef-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="514ef-111">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="514ef-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="514ef-112">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="514ef-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="514ef-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="514ef-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="514ef-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="514ef-114">Parameters</span></span>

<span data-ttu-id="514ef-115">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="514ef-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="514ef-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="514ef-116">Return value</span></span>

<span data-ttu-id="514ef-117">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="514ef-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="514ef-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="514ef-118">Remarks</span></span>

<span data-ttu-id="514ef-119">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="514ef-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="514ef-120">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="514ef-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="514ef-121">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="514ef-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="514ef-122">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="514ef-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="514ef-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="514ef-123">Requirements</span></span>



| <span data-ttu-id="514ef-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="514ef-124">Requirement</span></span> | <span data-ttu-id="514ef-125">Value</span><span class="sxs-lookup"><span data-stu-id="514ef-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="514ef-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="514ef-126">Minimum supported client</span></span><br/> | <span data-ttu-id="514ef-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="514ef-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="514ef-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="514ef-128">Minimum supported server</span></span><br/> | <span data-ttu-id="514ef-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="514ef-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="514ef-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="514ef-130">Namespace</span></span><br/>                | <span data-ttu-id="514ef-131">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="514ef-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="514ef-132">MOF</span><span class="sxs-lookup"><span data-stu-id="514ef-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="514ef-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="514ef-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="514ef-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="514ef-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="514ef-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="514ef-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="514ef-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="514ef-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="514ef-137">\_OSVERSIONCHECK CIM</span><span class="sxs-lookup"><span data-stu-id="514ef-137">CIM\_OSVersionCheck</span></span>](invoke-method-in-class-cim-osversioncheck.md)
</dt> <dt>

[<span data-ttu-id="514ef-138">**\_OSVERSIONCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="514ef-138">**CIM\_OSVersionCheck**</span></span>](cim-osversioncheck.md)
</dt> </dl>

 

