---
description: El método Invoke de la \_ clase CIM RebootAction toma una acción concreta. Los detalles de cómo realiza la acción el método son específicos de la implementación. Este método se hereda de la \_ acción CIM.
ms.assetid: 27b6571e-94fe-423e-89ab-5ba2bc632882
ms.tgt_platform: multiple
title: Método Invoke de la clase CIM_RebootAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RebootAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e68849a486cc6a5b61dc55cf86e259e2f58435e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659464"
---
# <a name="invoke-method-of-the-cim_rebootaction-class"></a><span data-ttu-id="a6fae-105">Método Invoke de la \_ clase CIM RebootAction</span><span class="sxs-lookup"><span data-stu-id="a6fae-105">Invoke method of the CIM\_RebootAction class</span></span>

<span data-ttu-id="a6fae-106">El método **Invoke** de la clase [**CIM \_ RebootAction**](cim-rebootaction.md) toma una acción concreta.</span><span class="sxs-lookup"><span data-stu-id="a6fae-106">The **Invoke** method of the [**CIM\_RebootAction**](cim-rebootaction.md) class takes a particular action.</span></span> <span data-ttu-id="a6fae-107">Los detalles de cómo realiza la acción el método son específicos de la implementación.</span><span class="sxs-lookup"><span data-stu-id="a6fae-107">The details of how the method performs the action are implementation specific.</span></span> <span data-ttu-id="a6fae-108">Este método se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="a6fae-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a6fae-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a6fae-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a6fae-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a6fae-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a6fae-111">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="a6fae-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a6fae-112">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a6fae-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a6fae-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6fae-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="a6fae-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6fae-114">Parameters</span></span>

<span data-ttu-id="a6fae-115">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a6fae-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a6fae-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6fae-116">Return value</span></span>

<span data-ttu-id="a6fae-117">Devuelve un valor entero de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="a6fae-117">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6fae-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6fae-118">Remarks</span></span>

<span data-ttu-id="a6fae-119">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="a6fae-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a6fae-120">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="a6fae-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a6fae-121">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a6fae-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a6fae-122">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a6fae-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6fae-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6fae-123">Requirements</span></span>



| <span data-ttu-id="a6fae-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6fae-124">Requirement</span></span> | <span data-ttu-id="a6fae-125">Value</span><span class="sxs-lookup"><span data-stu-id="a6fae-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6fae-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6fae-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a6fae-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6fae-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a6fae-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6fae-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a6fae-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6fae-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a6fae-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a6fae-130">Namespace</span></span><br/>                | <span data-ttu-id="a6fae-131">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a6fae-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a6fae-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a6fae-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6fae-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6fae-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6fae-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a6fae-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6fae-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6fae-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6fae-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6fae-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6fae-137">\_REBOOTACTION CIM</span><span class="sxs-lookup"><span data-stu-id="a6fae-137">CIM\_RebootAction</span></span>](invoke-method-in-class-cim-rebootaction.md)
</dt> <dt>

[<span data-ttu-id="a6fae-138">**\_REBOOTACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="a6fae-138">**CIM\_RebootAction**</span></span>](cim-rebootaction.md)
</dt> </dl>

 

