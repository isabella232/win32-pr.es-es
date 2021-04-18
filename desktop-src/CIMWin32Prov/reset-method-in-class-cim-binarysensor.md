---
description: El método Reset de la \_ clase BinarySensor de CIM solicita un restablecimiento del dispositivo lógico.
ms.assetid: 73ae915d-9649-4eca-8f9b-fb4165c94cbe
ms.tgt_platform: multiple
title: Método Reset de la clase CIM_BinarySensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BinarySensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f636cf277e144dc827adc0891d41dc136ce0a99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423360"
---
# <a name="reset-method-of-the-cim_binarysensor-class"></a><span data-ttu-id="34149-103">Método Reset de la \_ clase BinarySensor de CIM</span><span class="sxs-lookup"><span data-stu-id="34149-103">Reset method of the CIM\_BinarySensor class</span></span>

<span data-ttu-id="34149-104">El método **RESET** de la \_ clase BinarySensor de CIM solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="34149-104">The **Reset** method of the CIM\_BinarySensor class requests a reset of the logical device.</span></span> <span data-ttu-id="34149-105">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34149-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34149-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="34149-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="34149-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="34149-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="34149-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34149-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="34149-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34149-109">Parameters</span></span>

<span data-ttu-id="34149-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="34149-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="34149-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34149-111">Return value</span></span>

<span data-ttu-id="34149-112">Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y otro valor si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="34149-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="34149-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34149-113">Remarks</span></span>

<span data-ttu-id="34149-114">Actualmente, WMI no implementa este método.</span><span class="sxs-lookup"><span data-stu-id="34149-114">Currently, this method is not implemented by WMI.</span></span> <span data-ttu-id="34149-115">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="34149-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="34149-116">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="34149-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="34149-117">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="34149-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="34149-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34149-118">Requirements</span></span>



| <span data-ttu-id="34149-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="34149-119">Requirement</span></span> | <span data-ttu-id="34149-120">Value</span><span class="sxs-lookup"><span data-stu-id="34149-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34149-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34149-121">Minimum supported client</span></span><br/> | <span data-ttu-id="34149-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34149-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="34149-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34149-123">Minimum supported server</span></span><br/> | <span data-ttu-id="34149-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34149-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34149-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="34149-125">Namespace</span></span><br/>                | <span data-ttu-id="34149-126">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="34149-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="34149-127">MOF</span><span class="sxs-lookup"><span data-stu-id="34149-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34149-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34149-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="34149-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="34149-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34149-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34149-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34149-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="34149-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34149-132">\_BINARYSENSOR CIM</span><span class="sxs-lookup"><span data-stu-id="34149-132">CIM\_BinarySensor</span></span>](reset-method-in-class-cim-binarysensor.md)
</dt> <dt>

[<span data-ttu-id="34149-133">**\_BINARYSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="34149-133">**CIM\_BinarySensor**</span></span>](cim-binarysensor.md)
</dt> </dl>

 

 




