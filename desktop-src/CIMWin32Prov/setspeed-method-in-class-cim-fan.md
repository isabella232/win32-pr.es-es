---
description: El método SetSpeed solicita que la velocidad del ventilador se establezca en el valor especificado en el parámetro de entrada del método.
ms.assetid: 7dd1cd57-66c5-4b50-9a73-31caf0b824e6
ms.tgt_platform: multiple
title: Método SetSpeed de la clase CIM_Fan
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Fan.SetSpeed
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16d90dbef3a9318ad144303e5720cea0abbde03e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907530"
---
# <a name="setspeed-method-of-the-cim_fan-class"></a><span data-ttu-id="141e7-103">Método SetSpeed de la \_ clase de ventilador CIM</span><span class="sxs-lookup"><span data-stu-id="141e7-103">SetSpeed method of the CIM\_Fan class</span></span>

<span data-ttu-id="141e7-104">El método **SETSPEED** solicita que la velocidad del ventilador se establezca en el valor especificado en el parámetro de entrada del método.</span><span class="sxs-lookup"><span data-stu-id="141e7-104">The **SetSpeed** method requests that the fan speed be set to the value specified in the method's input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="141e7-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="141e7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="141e7-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="141e7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="141e7-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="141e7-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="141e7-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="141e7-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="141e7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="141e7-109">Syntax</span></span>


```mof
uint32 SetSpeed(
  [in] uint64 DesiredSpeed
);
```



## <a name="parameters"></a><span data-ttu-id="141e7-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="141e7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="141e7-111">*DesiredSpeed* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="141e7-111">*DesiredSpeed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="141e7-112">Velocidad de ventilador solicitada, en revoluciones por minuto.</span><span class="sxs-lookup"><span data-stu-id="141e7-112">Requested fan speed, in revolutions per minute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="141e7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="141e7-113">Return value</span></span>

<span data-ttu-id="141e7-114">Devuelve un valor de 0 (cero) si se realiza correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="141e7-114">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="141e7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="141e7-115">Remarks</span></span>

<span data-ttu-id="141e7-116">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="141e7-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="141e7-117">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="141e7-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="141e7-118">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="141e7-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="141e7-119">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="141e7-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="141e7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="141e7-120">Requirements</span></span>



| <span data-ttu-id="141e7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="141e7-121">Requirement</span></span> | <span data-ttu-id="141e7-122">Value</span><span class="sxs-lookup"><span data-stu-id="141e7-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="141e7-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="141e7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="141e7-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="141e7-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="141e7-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="141e7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="141e7-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="141e7-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="141e7-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="141e7-127">Namespace</span></span><br/>                | <span data-ttu-id="141e7-128">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="141e7-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="141e7-129">MOF</span><span class="sxs-lookup"><span data-stu-id="141e7-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="141e7-130"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="141e7-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="141e7-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="141e7-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="141e7-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="141e7-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="141e7-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="141e7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="141e7-134">\_Ventilador CIM</span><span class="sxs-lookup"><span data-stu-id="141e7-134">CIM\_Fan</span></span>](setspeed-method-in-class-cim-fan.md)
</dt> <dt>

[<span data-ttu-id="141e7-135">**\_Ventilador CIM**</span><span class="sxs-lookup"><span data-stu-id="141e7-135">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> </dl>

 

