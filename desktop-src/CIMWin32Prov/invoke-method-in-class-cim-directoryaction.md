---
description: El método Invoke de la \_ clase CIM DirectoryAction toma una acción concreta. Los detalles de cómo realiza la acción el método son específicos de la implementación. Este método se hereda de la \_ acción CIM.
ms.assetid: e919dfdb-a52d-4bcb-abff-e1273c406226
ms.tgt_platform: multiple
title: Método Invoke de la clase CIM_DirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f30184fe46cd8e8b9a595545ccba9a7d738af18e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907133"
---
# <a name="invoke-method-of-the-cim_directoryaction-class"></a><span data-ttu-id="94b46-105">Método Invoke de la \_ clase CIM DirectoryAction</span><span class="sxs-lookup"><span data-stu-id="94b46-105">Invoke method of the CIM\_DirectoryAction class</span></span>

<span data-ttu-id="94b46-106">El método **Invoke** de la clase [**CIM \_ DirectoryAction**](cim-directoryaction.md) toma una acción concreta.</span><span class="sxs-lookup"><span data-stu-id="94b46-106">The **Invoke** method of the [**CIM\_DirectoryAction**](cim-directoryaction.md) class takes a particular action.</span></span> <span data-ttu-id="94b46-107">Los detalles de cómo realiza la acción el método son específicos de la implementación.</span><span class="sxs-lookup"><span data-stu-id="94b46-107">Details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="94b46-108">Este método se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="94b46-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94b46-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="94b46-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="94b46-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="94b46-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="94b46-111">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="94b46-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="94b46-112">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="94b46-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="94b46-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94b46-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="94b46-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94b46-114">Parameters</span></span>

<span data-ttu-id="94b46-115">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="94b46-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="94b46-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94b46-116">Return value</span></span>

<span data-ttu-id="94b46-117">Devuelve un valor de 0 (cero) si se realiza correctamente, 1 (uno) si no se admite el método, y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="94b46-117">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="94b46-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94b46-118">Remarks</span></span>

<span data-ttu-id="94b46-119">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="94b46-119">WMI does not implement this class.</span></span>

<span data-ttu-id="94b46-120">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="94b46-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="94b46-121">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="94b46-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="94b46-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94b46-122">Requirements</span></span>



| <span data-ttu-id="94b46-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="94b46-123">Requirement</span></span> | <span data-ttu-id="94b46-124">Value</span><span class="sxs-lookup"><span data-stu-id="94b46-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94b46-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94b46-125">Minimum supported client</span></span><br/> | <span data-ttu-id="94b46-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94b46-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94b46-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94b46-127">Minimum supported server</span></span><br/> | <span data-ttu-id="94b46-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94b46-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94b46-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="94b46-129">Namespace</span></span><br/>                | <span data-ttu-id="94b46-130">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="94b46-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="94b46-131">MOF</span><span class="sxs-lookup"><span data-stu-id="94b46-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94b46-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94b46-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="94b46-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="94b46-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94b46-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94b46-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94b46-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="94b46-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94b46-136">\_DIRECTORYACTION CIM</span><span class="sxs-lookup"><span data-stu-id="94b46-136">CIM\_DirectoryAction</span></span>](invoke-method-in-class-cim-directoryaction.md)
</dt> <dt>

[<span data-ttu-id="94b46-137">**\_DIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="94b46-137">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> </dl>

 

