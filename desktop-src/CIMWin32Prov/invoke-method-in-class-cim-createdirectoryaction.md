---
description: El método Invoke de la \_ clase CIM CreateDirectoryAction toma una acción concreta. Los detalles sobre cómo realiza la acción el método son específicos de la implementación. Este método se hereda de la \_ acción CIM.
ms.assetid: f14e215d-31f2-46c5-b45e-3de64ce46bf2
ms.tgt_platform: multiple
title: Método Invoke de la clase CIM_CreateDirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CreateDirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 690a29ae0ea85e0b965d2a426703eea87aee9184
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807237"
---
# <a name="invoke-method-of-the-cim_createdirectoryaction-class"></a><span data-ttu-id="21ec4-105">Método Invoke de la \_ clase CIM CreateDirectoryAction</span><span class="sxs-lookup"><span data-stu-id="21ec4-105">Invoke method of the CIM\_CreateDirectoryAction class</span></span>

<span data-ttu-id="21ec4-106">El método **Invoke** de la clase [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) toma una acción concreta.</span><span class="sxs-lookup"><span data-stu-id="21ec4-106">The **Invoke** method of the [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class takes a particular action.</span></span> <span data-ttu-id="21ec4-107">Los detalles sobre cómo realiza la acción el método son específicos de la implementación.</span><span class="sxs-lookup"><span data-stu-id="21ec4-107">Details about how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="21ec4-108">Este método se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="21ec4-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="21ec4-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="21ec4-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="21ec4-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="21ec4-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="21ec4-111">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="21ec4-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="21ec4-112">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="21ec4-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="21ec4-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21ec4-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="21ec4-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21ec4-114">Parameters</span></span>

<span data-ttu-id="21ec4-115">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="21ec4-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21ec4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21ec4-116">Return value</span></span>

<span data-ttu-id="21ec4-117">Devuelve un valor de 0 si se ejecuta correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="21ec4-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="21ec4-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21ec4-118">Remarks</span></span>

<span data-ttu-id="21ec4-119">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="21ec4-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="21ec4-120">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="21ec4-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="21ec4-121">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="21ec4-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="21ec4-122">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="21ec4-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="21ec4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21ec4-123">Requirements</span></span>



| <span data-ttu-id="21ec4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="21ec4-124">Requirement</span></span> | <span data-ttu-id="21ec4-125">Value</span><span class="sxs-lookup"><span data-stu-id="21ec4-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21ec4-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21ec4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="21ec4-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21ec4-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="21ec4-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21ec4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="21ec4-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21ec4-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21ec4-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="21ec4-130">Namespace</span></span><br/>                | <span data-ttu-id="21ec4-131">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="21ec4-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="21ec4-132">MOF</span><span class="sxs-lookup"><span data-stu-id="21ec4-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21ec4-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21ec4-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="21ec4-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="21ec4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21ec4-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21ec4-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21ec4-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="21ec4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21ec4-137">**\_CREATEDIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="21ec4-137">**CIM\_CreateDirectoryAction**</span></span>](invoke-method-in-class-cim-createdirectoryaction.md)
</dt> <dt>

[<span data-ttu-id="21ec4-138">**\_CREATEDIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="21ec4-138">**CIM\_CreateDirectoryAction**</span></span>](cim-createdirectoryaction.md)
</dt> </dl>

 

