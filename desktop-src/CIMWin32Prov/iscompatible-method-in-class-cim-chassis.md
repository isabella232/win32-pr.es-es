---
description: Comprueba si el chasis físico al que se hace referencia puede estar contenido o insertado en el paquete físico.
ms.assetid: 9a1aa1b7-2b95-4887-9d14-e416ff69f9df
ms.tgt_platform: multiple
title: Método IsCompatible de la clase CIM_Chassis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8796582b153a7283429715569eeed91e4dd38fc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659459"
---
# <a name="iscompatible-method-of-the-cim_chassis-class"></a><span data-ttu-id="3f7e3-103">Método IsCompatible de la \_ clase de chasis CIM</span><span class="sxs-lookup"><span data-stu-id="3f7e3-103">IsCompatible method of the CIM\_Chassis class</span></span>

<span data-ttu-id="3f7e3-104">El método **IsCompatible** comprueba si el chasis físico al que se hace referencia puede estar contenido o insertado en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="3f7e3-104">The **IsCompatible** method verifies whether the referenced physical chassis can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="3f7e3-105">En una subclase, el conjunto de códigos de retorno posibles se puede especificar mediante un calificador [**ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) en el método.</span><span class="sxs-lookup"><span data-stu-id="3f7e3-105">In a subclass, the set of possible return codes can be specified by using a [**ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) qualifier on the method.</span></span> <span data-ttu-id="3f7e3-106">Las cadenas a las que se traduce el contenido **ValueMap** también se pueden especificar en la subclase como calificador de matriz **Values** .</span><span class="sxs-lookup"><span data-stu-id="3f7e3-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="3f7e3-107">Este método se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="3f7e3-107">This method is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3f7e3-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="3f7e3-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3f7e3-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3f7e3-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3f7e3-110">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3f7e3-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3f7e3-111">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3f7e3-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3f7e3-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f7e3-112">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="3f7e3-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f7e3-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f7e3-114">*ElementToCheck* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f7e3-114">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f7e3-115">Referencia al elemento físico para el que se comprueba la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="3f7e3-115">Reference to the physical element for which to check compatibility.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f7e3-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f7e3-116">Return value</span></span>

<span data-ttu-id="3f7e3-117">Devuelve un valor de 0 (cero) si se realiza correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="3f7e3-117">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f7e3-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f7e3-118">Remarks</span></span>

<span data-ttu-id="3f7e3-119">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="3f7e3-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3f7e3-120">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="3f7e3-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3f7e3-121">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="3f7e3-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3f7e3-122">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="3f7e3-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f7e3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f7e3-123">Requirements</span></span>



| <span data-ttu-id="3f7e3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f7e3-124">Requirement</span></span> | <span data-ttu-id="3f7e3-125">Value</span><span class="sxs-lookup"><span data-stu-id="3f7e3-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f7e3-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f7e3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3f7e3-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3f7e3-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3f7e3-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f7e3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3f7e3-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f7e3-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3f7e3-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3f7e3-130">Namespace</span></span><br/>                | <span data-ttu-id="3f7e3-131">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3f7e3-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3f7e3-132">MOF</span><span class="sxs-lookup"><span data-stu-id="3f7e3-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f7e3-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f7e3-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f7e3-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3f7e3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f7e3-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f7e3-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f7e3-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f7e3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f7e3-137">**\_Chasis CIM**</span><span class="sxs-lookup"><span data-stu-id="3f7e3-137">**CIM\_Chassis**</span></span>](iscompatible-method-in-class-cim-chassis.md)
</dt> <dt>

[<span data-ttu-id="3f7e3-138">**\_Chasis CIM**</span><span class="sxs-lookup"><span data-stu-id="3f7e3-138">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> </dl>

 

