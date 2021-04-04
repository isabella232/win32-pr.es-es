---
description: El método Invoke de la \_ clase de acción CIM toma una acción concreta. Los detalles de cómo realiza el método la acción son específicos de la implementación.
ms.assetid: 4f0be560-bd78-4c7f-b6e3-ca86837a84f9
ms.tgt_platform: multiple
title: Método Invoke de la clase CIM_Action
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Action.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e02e414fb05e0dd4ea97c3e3a4d87659fed4c963
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907136"
---
# <a name="invoke-method-of-the-cim_action-class"></a><span data-ttu-id="7eadc-104">Método Invoke de la \_ clase de acción CIM</span><span class="sxs-lookup"><span data-stu-id="7eadc-104">Invoke method of the CIM\_Action class</span></span>

<span data-ttu-id="7eadc-105">El método **Invoke** de la clase de [**\_ acción CIM**](cim-action.md) toma una acción concreta.</span><span class="sxs-lookup"><span data-stu-id="7eadc-105">The **Invoke** method of the [**CIM\_Action**](cim-action.md) class takes a particular action.</span></span> <span data-ttu-id="7eadc-106">Los detalles de cómo realiza el método la acción son específicos de la implementación.</span><span class="sxs-lookup"><span data-stu-id="7eadc-106">The details of how the method performs the action is implementation-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7eadc-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="7eadc-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7eadc-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7eadc-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7eadc-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="7eadc-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7eadc-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7eadc-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7eadc-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7eadc-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="7eadc-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7eadc-112">Parameters</span></span>

<span data-ttu-id="7eadc-113">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7eadc-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7eadc-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7eadc-114">Return value</span></span>

<span data-ttu-id="7eadc-115">Devuelve un valor de 0 (cero) si se realiza correctamente, 1 (uno) si no se admite el método, y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="7eadc-115">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7eadc-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7eadc-116">Remarks</span></span>

<span data-ttu-id="7eadc-117">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="7eadc-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="7eadc-118">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="7eadc-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="7eadc-119">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="7eadc-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7eadc-120">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="7eadc-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eadc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eadc-121">Requirements</span></span>



| <span data-ttu-id="7eadc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eadc-122">Requirement</span></span> | <span data-ttu-id="7eadc-123">Value</span><span class="sxs-lookup"><span data-stu-id="7eadc-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7eadc-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7eadc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7eadc-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7eadc-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7eadc-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7eadc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7eadc-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7eadc-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7eadc-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7eadc-128">Namespace</span></span><br/>                | <span data-ttu-id="7eadc-129">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7eadc-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7eadc-130">MOF</span><span class="sxs-lookup"><span data-stu-id="7eadc-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7eadc-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7eadc-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7eadc-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7eadc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eadc-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7eadc-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eadc-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="7eadc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eadc-135">Acción de CIM \_</span><span class="sxs-lookup"><span data-stu-id="7eadc-135">CIM\_Action</span></span>](invoke-method-in-class-cim-action.md)
</dt> <dt>

[<span data-ttu-id="7eadc-136">**Acción de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="7eadc-136">**CIM\_Action**</span></span>](cim-action.md)
</dt> <dt>

[<span data-ttu-id="7eadc-137">Clases CIM</span><span class="sxs-lookup"><span data-stu-id="7eadc-137">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

