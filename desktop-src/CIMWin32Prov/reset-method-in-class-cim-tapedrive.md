---
description: El método Reset de la \_ clase CIM TapeDrive solicita un restablecimiento del dispositivo lógico.
ms.assetid: 48097e0d-7986-46b9-884d-7534f3848dd7
ms.tgt_platform: multiple
title: Método Reset de la clase CIM_TapeDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e5fd76d038e743ba5148f4c82555d50f0a5dde5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907477"
---
# <a name="reset-method-of-the-cim_tapedrive-class"></a><span data-ttu-id="f597c-103">Método Reset de la \_ clase CIM TapeDrive</span><span class="sxs-lookup"><span data-stu-id="f597c-103">Reset method of the CIM\_TapeDrive class</span></span>

<span data-ttu-id="f597c-104">El método **RESET** de la \_ clase CIM TapeDrive solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f597c-104">The **Reset** method of the CIM\_TapeDrive class requests a reset of the logical device.</span></span> <span data-ttu-id="f597c-105">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f597c-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f597c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f597c-106">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="f597c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f597c-107">Parameters</span></span>

<span data-ttu-id="f597c-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f597c-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f597c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f597c-109">Return value</span></span>

<span data-ttu-id="f597c-110">Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y otro valor si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="f597c-110">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="f597c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f597c-111">Remarks</span></span>

<span data-ttu-id="f597c-112">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="f597c-112">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f597c-113">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="f597c-113">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f597c-114">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f597c-114">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f597c-115">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f597c-115">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f597c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f597c-116">Requirements</span></span>



| <span data-ttu-id="f597c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f597c-117">Requirement</span></span> | <span data-ttu-id="f597c-118">Value</span><span class="sxs-lookup"><span data-stu-id="f597c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f597c-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f597c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f597c-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f597c-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f597c-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f597c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f597c-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f597c-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f597c-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f597c-123">Namespace</span></span><br/>                | <span data-ttu-id="f597c-124">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f597c-124">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f597c-125">MOF</span><span class="sxs-lookup"><span data-stu-id="f597c-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f597c-126"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f597c-126"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f597c-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f597c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f597c-128"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f597c-128"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f597c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f597c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f597c-130">CIM \_ TapeDrive</span><span class="sxs-lookup"><span data-stu-id="f597c-130">CIM\_TapeDrive</span></span>](reset-method-in-class-cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="f597c-131">**CIM \_ TapeDrive**</span><span class="sxs-lookup"><span data-stu-id="f597c-131">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> </dl>

 

 




