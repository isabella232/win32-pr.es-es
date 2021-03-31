---
description: El método Invoke de la \_ clase CIM ExecuteProgram toma una acción concreta. Los detalles de cómo realiza la acción el método son específicos de la implementación. Este método se hereda de la \_ acción CIM.
ms.assetid: 14a12fae-14a6-412a-a778-8dd34a5843d1
ms.tgt_platform: multiple
title: Método Invoke de la clase CIM_ExecuteProgram
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExecuteProgram.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bdf9a4edb78bb47c0354991d161339099e4dc49f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423303"
---
# <a name="invoke-method-of-the-cim_executeprogram-class"></a><span data-ttu-id="a484f-105">Método Invoke de la \_ clase CIM ExecuteProgram</span><span class="sxs-lookup"><span data-stu-id="a484f-105">Invoke method of the CIM\_ExecuteProgram class</span></span>

<span data-ttu-id="a484f-106">El método **Invoke** de la clase [**CIM \_ ExecuteProgram**](cim-executeprogram.md) toma una acción concreta.</span><span class="sxs-lookup"><span data-stu-id="a484f-106">The **Invoke** method of the [**CIM\_ExecuteProgram**](cim-executeprogram.md) class takes a particular action.</span></span> <span data-ttu-id="a484f-107">Los detalles de cómo realiza la acción el método son específicos de la implementación.</span><span class="sxs-lookup"><span data-stu-id="a484f-107">The details of how the method performs the action are implementation specific.</span></span> <span data-ttu-id="a484f-108">Este método se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="a484f-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a484f-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a484f-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a484f-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a484f-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a484f-111">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="a484f-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a484f-112">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a484f-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a484f-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a484f-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="a484f-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a484f-114">Parameters</span></span>

<span data-ttu-id="a484f-115">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a484f-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a484f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a484f-116">Return value</span></span>

<span data-ttu-id="a484f-117">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="a484f-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a484f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a484f-118">Remarks</span></span>

<span data-ttu-id="a484f-119">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="a484f-119">WMI does not implement this class.</span></span>

<span data-ttu-id="a484f-120">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a484f-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a484f-121">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a484f-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a484f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a484f-122">Requirements</span></span>



| <span data-ttu-id="a484f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a484f-123">Requirement</span></span> | <span data-ttu-id="a484f-124">Value</span><span class="sxs-lookup"><span data-stu-id="a484f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a484f-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a484f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a484f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a484f-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a484f-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a484f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a484f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a484f-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a484f-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a484f-129">Namespace</span></span><br/>                | <span data-ttu-id="a484f-130">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a484f-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a484f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a484f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a484f-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a484f-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a484f-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a484f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a484f-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a484f-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a484f-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a484f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a484f-136">\_EXECUTEPROGRAM CIM</span><span class="sxs-lookup"><span data-stu-id="a484f-136">CIM\_ExecuteProgram</span></span>](invoke-method-in-class-cim-executeprogram.md)
</dt> <dt>

[<span data-ttu-id="a484f-137">**\_EXECUTEPROGRAM CIM**</span><span class="sxs-lookup"><span data-stu-id="a484f-137">**CIM\_ExecuteProgram**</span></span>](cim-executeprogram.md)
</dt> </dl>

 

