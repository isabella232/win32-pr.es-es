---
description: El método Reset de la \_ clase CIM tacómetro solicita un restablecimiento del dispositivo lógico.
ms.assetid: c8806511-6796-49e9-bdcd-959e5c5f9da0
ms.tgt_platform: multiple
title: Método Reset de la clase CIM_Tachometer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Tachometer.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 368c764ed0f20d8da0e4f08d53e788592809e29d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538554"
---
# <a name="reset-method-of-the-cim_tachometer-class"></a><span data-ttu-id="6f55c-103">Método Reset de la \_ clase CIM tacómetro</span><span class="sxs-lookup"><span data-stu-id="6f55c-103">Reset method of the CIM\_Tachometer class</span></span>

<span data-ttu-id="6f55c-104">El método **RESET** de la \_ clase CIM tacómetro solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6f55c-104">The **Reset** method of the CIM\_Tachometer class requests a reset of the logical device.</span></span> <span data-ttu-id="6f55c-105">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6f55c-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f55c-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="6f55c-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6f55c-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6f55c-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6f55c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f55c-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="6f55c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f55c-109">Parameters</span></span>

<span data-ttu-id="6f55c-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6f55c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f55c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f55c-111">Return value</span></span>

<span data-ttu-id="6f55c-112">Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y otro valor si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="6f55c-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f55c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f55c-113">Remarks</span></span>

<span data-ttu-id="6f55c-114">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="6f55c-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="6f55c-115">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="6f55c-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="6f55c-116">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="6f55c-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6f55c-117">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="6f55c-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f55c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f55c-118">Requirements</span></span>



| <span data-ttu-id="6f55c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f55c-119">Requirement</span></span> | <span data-ttu-id="6f55c-120">Value</span><span class="sxs-lookup"><span data-stu-id="6f55c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f55c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f55c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6f55c-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f55c-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f55c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f55c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6f55c-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f55c-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f55c-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6f55c-125">Namespace</span></span><br/>                | <span data-ttu-id="6f55c-126">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6f55c-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6f55c-127">MOF</span><span class="sxs-lookup"><span data-stu-id="6f55c-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f55c-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f55c-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f55c-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f55c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f55c-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f55c-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f55c-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f55c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f55c-132">\_Tacómetro CIM</span><span class="sxs-lookup"><span data-stu-id="6f55c-132">CIM\_Tachometer</span></span>](reset-method-in-class-cim-tachometer.md)
</dt> <dt>

[<span data-ttu-id="6f55c-133">**\_Tacómetro CIM**</span><span class="sxs-lookup"><span data-stu-id="6f55c-133">**CIM\_Tachometer**</span></span>](cim-tachometer.md)
</dt> </dl>

 

 




