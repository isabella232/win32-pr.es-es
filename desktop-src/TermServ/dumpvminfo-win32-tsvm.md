---
title: Método DumpVmInfo de la clase Win32_TSVm
description: Este miembro es para la realización de pruebas internas y no debe usarse en el código.
ms.assetid: 40cb4fdc-f657-47c6-8daa-684a12be30e4
ms.tgt_platform: multiple
keywords:
- Método DumpVmInfo Servicios de Escritorio remoto
- Método DumpVmInfo Servicios de Escritorio remoto, clase Win32_TSVm
- Win32_TSVm de clase Servicios de Escritorio remoto, método DumpVmInfo
topic_type:
- apiref
api_name:
- Win32_TSVm.DumpVmInfo
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2d02a1d4ea07bd045da2850a4d7ccb0069977a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804034"
---
# <a name="dumpvminfo-method-of-the-win32_tsvm-class"></a><span data-ttu-id="fc4c9-106">Método DumpVmInfo de la \_ clase TSVm de Win32</span><span class="sxs-lookup"><span data-stu-id="fc4c9-106">DumpVmInfo method of the Win32\_TSVm class</span></span>

<span data-ttu-id="fc4c9-107">Este miembro es para la realización de pruebas internas y no debe usarse en el código.</span><span class="sxs-lookup"><span data-stu-id="fc4c9-107">This member is for internal testing purposes, and should not be used in your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc4c9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc4c9-108">Syntax</span></span>


```mof
uint32 DumpVmInfo();
```



## <a name="parameters"></a><span data-ttu-id="fc4c9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc4c9-109">Parameters</span></span>

<span data-ttu-id="fc4c9-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fc4c9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc4c9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc4c9-111">Return value</span></span>

<span data-ttu-id="fc4c9-112">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="fc4c9-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="fc4c9-113">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="fc4c9-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc4c9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc4c9-114">Requirements</span></span>



| <span data-ttu-id="fc4c9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc4c9-115">Requirement</span></span> | <span data-ttu-id="fc4c9-116">Value</span><span class="sxs-lookup"><span data-stu-id="fc4c9-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc4c9-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc4c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fc4c9-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fc4c9-118">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="fc4c9-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc4c9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fc4c9-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fc4c9-120">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="fc4c9-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fc4c9-121">Namespace</span></span><br/>                | <span data-ttu-id="fc4c9-122">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fc4c9-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="fc4c9-123">MOF</span><span class="sxs-lookup"><span data-stu-id="fc4c9-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc4c9-124"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc4c9-124"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="fc4c9-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fc4c9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc4c9-126"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc4c9-126"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc4c9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc4c9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc4c9-128">**Win32 \_ TSVm**</span><span class="sxs-lookup"><span data-stu-id="fc4c9-128">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





