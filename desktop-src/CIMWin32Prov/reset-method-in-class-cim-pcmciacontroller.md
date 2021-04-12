---
description: El método Reset de la \_ clase PCMCIAController de CIM solicita un restablecimiento del dispositivo lógico.
ms.assetid: c58e3265-2849-4154-a03e-2e1cfa9e3d30
ms.tgt_platform: multiple
title: Método Reset de la clase CIM_PCMCIAController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCMCIAController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8576bc5c1ce291c355d2907761e5b342ea6f3bc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274976"
---
# <a name="reset-method-of-the-cim_pcmciacontroller-class"></a><span data-ttu-id="e1421-103">Método Reset de la \_ clase PCMCIAController de CIM</span><span class="sxs-lookup"><span data-stu-id="e1421-103">Reset method of the CIM\_PCMCIAController class</span></span>

<span data-ttu-id="e1421-104">El método **RESET** de la \_ clase PCMCIAController de CIM solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e1421-104">The **Reset** method of the CIM\_PCMCIAController class requests a reset of the logical device.</span></span> <span data-ttu-id="e1421-105">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e1421-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e1421-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="e1421-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e1421-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e1421-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e1421-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1421-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="e1421-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1421-109">Parameters</span></span>

<span data-ttu-id="e1421-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e1421-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1421-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1421-111">Return value</span></span>

<span data-ttu-id="e1421-112">Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y otro valor si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="e1421-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1421-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1421-113">Remarks</span></span>

<span data-ttu-id="e1421-114">WMI no implementa este método.</span><span class="sxs-lookup"><span data-stu-id="e1421-114">This method is not implemented by WMI.</span></span> <span data-ttu-id="e1421-115">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="e1421-115">To use this method, you must implement it in your own provider.</span></span> <span data-ttu-id="e1421-116">Para las clases WMI derivadas de [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md), vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e1421-116">For WMI classes derived from [**CIM\_PCMCIAController**](cim-pcmciacontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e1421-117">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="e1421-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e1421-118">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="e1421-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1421-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1421-119">Requirements</span></span>



| <span data-ttu-id="e1421-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1421-120">Requirement</span></span> | <span data-ttu-id="e1421-121">Value</span><span class="sxs-lookup"><span data-stu-id="e1421-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1421-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1421-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e1421-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1421-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e1421-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1421-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e1421-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1421-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e1421-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e1421-126">Namespace</span></span><br/>                | <span data-ttu-id="e1421-127">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e1421-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e1421-128">MOF</span><span class="sxs-lookup"><span data-stu-id="e1421-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1421-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1421-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1421-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e1421-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1421-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1421-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1421-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1421-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1421-133">\_PCMCIACONTROLLER CIM</span><span class="sxs-lookup"><span data-stu-id="e1421-133">CIM\_PCMCIAController</span></span>](reset-method-in-class-cim-pcmciacontroller.md)
</dt> <dt>

[<span data-ttu-id="e1421-134">**\_PCMCIACONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="e1421-134">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> </dl>

 

 




