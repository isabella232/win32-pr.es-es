---
description: Detiene el servicio representado por el objeto derivado del \_ servicio CIM.
ms.assetid: f9eedde7-8d71-40a2-b1e9-7ba97e634f64
ms.tgt_platform: multiple
title: Método StopService de la clase CIM_Service (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 14a7d378b514a93906c3be4f711bd6ab5b88bf17
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153112"
---
# <a name="stopservice-method-of-the-cim_service-class-sdoiash"></a><span data-ttu-id="3a232-103">Método StopService de la clase CIM_Service (Sdoias. h)</span><span class="sxs-lookup"><span data-stu-id="3a232-103">StopService method of the CIM_Service class (Sdoias.h)</span></span>

<span data-ttu-id="3a232-104">El método **StopService** detiene el servicio representado por el objeto derivado del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="3a232-104">The **StopService** method stops the service represented by the object derived from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3a232-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="3a232-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3a232-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3a232-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3a232-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3a232-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3a232-108">Para obtener más información sobre el uso de este método, vea [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3a232-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a232-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a232-109">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="3a232-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a232-110">Parameters</span></span>

<span data-ttu-id="3a232-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3a232-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a232-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a232-112">Return value</span></span>

<span data-ttu-id="3a232-113">Devuelve un valor de 0 (cero) si el servicio se detuvo correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="3a232-113">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a232-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a232-114">Remarks</span></span>

<span data-ttu-id="3a232-115">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="3a232-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3a232-116">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="3a232-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3a232-117">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="3a232-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3a232-118">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="3a232-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a232-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a232-119">Requirements</span></span>



| <span data-ttu-id="3a232-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a232-120">Requirement</span></span> | <span data-ttu-id="3a232-121">Value</span><span class="sxs-lookup"><span data-stu-id="3a232-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a232-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a232-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3a232-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a232-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a232-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a232-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3a232-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a232-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a232-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3a232-126">Namespace</span></span><br/>                | <span data-ttu-id="3a232-127">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3a232-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3a232-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a232-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a232-129"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a232-129"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="3a232-130">MOF</span><span class="sxs-lookup"><span data-stu-id="3a232-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a232-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a232-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a232-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3a232-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a232-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a232-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a232-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a232-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a232-135">\_Servicio CIM</span><span class="sxs-lookup"><span data-stu-id="3a232-135">CIM\_Service</span></span>](stopservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="3a232-136">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="3a232-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

