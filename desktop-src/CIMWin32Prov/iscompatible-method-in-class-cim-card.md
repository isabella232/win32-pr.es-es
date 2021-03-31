---
description: El método IsCompatible comprueba si el elemento físico al que se hace referencia puede estar contenido o insertado en el paquete físico.
ms.assetid: 809a1871-dfa2-499b-9adf-118dec71586b
ms.tgt_platform: multiple
title: Método IsCompatible de la clase CIM_Card
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Card.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0573cc9902826d2a283e549414cf31aae98cc331
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152981"
---
# <a name="iscompatible-method-of-the-cim_card-class"></a><span data-ttu-id="c79e1-103">Método IsCompatible de la \_ clase CIM Card</span><span class="sxs-lookup"><span data-stu-id="c79e1-103">IsCompatible method of the CIM\_Card class</span></span>

<span data-ttu-id="c79e1-104">El método **IsCompatible** comprueba si el elemento físico al que se hace referencia puede estar contenido o insertado en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="c79e1-104">The **IsCompatible** method verifies whether the referenced physical element may be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="c79e1-105">En una subclase, se puede especificar el conjunto de códigos de retorno posibles mediante un calificador **ValueMap** en el método.</span><span class="sxs-lookup"><span data-stu-id="c79e1-105">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="c79e1-106">Las cadenas a las que se traduce el contenido **ValueMap** también se pueden especificar en la subclase como calificador de matriz **Values** .</span><span class="sxs-lookup"><span data-stu-id="c79e1-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="c79e1-107">Este método se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="c79e1-107">This method is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c79e1-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="c79e1-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c79e1-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c79e1-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c79e1-110">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c79e1-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c79e1-111">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c79e1-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c79e1-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c79e1-112">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="c79e1-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c79e1-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c79e1-114">*ElementToCheck* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c79e1-114">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c79e1-115">Referencia al elemento físico en el que se ejecuta el método **IsCompatible** .</span><span class="sxs-lookup"><span data-stu-id="c79e1-115">Reference to the physical element that the **IsCompatible** method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c79e1-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c79e1-116">Return value</span></span>

<span data-ttu-id="c79e1-117">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="c79e1-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="c79e1-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c79e1-118">Remarks</span></span>

<span data-ttu-id="c79e1-119">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="c79e1-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c79e1-120">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="c79e1-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c79e1-121">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c79e1-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c79e1-122">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c79e1-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c79e1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c79e1-123">Requirements</span></span>



| <span data-ttu-id="c79e1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c79e1-124">Requirement</span></span> | <span data-ttu-id="c79e1-125">Value</span><span class="sxs-lookup"><span data-stu-id="c79e1-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c79e1-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c79e1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c79e1-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c79e1-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c79e1-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c79e1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c79e1-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c79e1-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c79e1-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c79e1-130">Namespace</span></span><br/>                | <span data-ttu-id="c79e1-131">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c79e1-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c79e1-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c79e1-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c79e1-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c79e1-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c79e1-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c79e1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c79e1-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c79e1-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c79e1-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="c79e1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c79e1-137">\_Tarjeta CIM</span><span class="sxs-lookup"><span data-stu-id="c79e1-137">CIM\_Card</span></span>](iscompatible-method-in-class-cim-card.md)
</dt> <dt>

[<span data-ttu-id="c79e1-138">**\_Tarjeta CIM**</span><span class="sxs-lookup"><span data-stu-id="c79e1-138">**CIM\_Card**</span></span>](cim-card.md)
</dt> </dl>

 

