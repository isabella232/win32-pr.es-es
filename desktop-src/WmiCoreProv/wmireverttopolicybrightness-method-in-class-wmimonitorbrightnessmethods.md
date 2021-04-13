---
description: El método WmiRevertToPolicyBrightness se usa para revertir el brillo a la configuración de directiva. Este método no tiene ningún efecto en la configuración de brillo de ALS.
ms.assetid: 9a520c3f-3563-4ef4-b397-14e487c8e8bb
title: Método WmiRevertToPolicyBrightness de la clase WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiRevertToPolicyBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 03e1ed74486c7a5a2f2c61dc858e715850ec516e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277326"
---
# <a name="wmireverttopolicybrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="24e6b-104">Método WmiRevertToPolicyBrightness de la clase WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="24e6b-104">WmiRevertToPolicyBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="24e6b-105">El método **WmiRevertToPolicyBrightness** se usa para revertir el brillo a la configuración de directiva.</span><span class="sxs-lookup"><span data-stu-id="24e6b-105">The **WmiRevertToPolicyBrightness** method is used to revert the brightness to the policy setting.</span></span> <span data-ttu-id="24e6b-106">Este método no tiene ningún efecto en la configuración de brillo de ALS.</span><span class="sxs-lookup"><span data-stu-id="24e6b-106">This method has no effect on the ALS brightness settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="24e6b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24e6b-107">Syntax</span></span>


```mof
uint32 WmiRevertToPolicyBrightness();
```



## <a name="parameters"></a><span data-ttu-id="24e6b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24e6b-108">Parameters</span></span>

<span data-ttu-id="24e6b-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="24e6b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="24e6b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24e6b-110">Return value</span></span>

<span data-ttu-id="24e6b-111">Devuelve cero (0) para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="24e6b-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="24e6b-112">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="24e6b-112">Any other number indicates an error.</span></span> <span data-ttu-id="24e6b-113">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="24e6b-113">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="24e6b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24e6b-114">Requirements</span></span>



| <span data-ttu-id="24e6b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="24e6b-115">Requirement</span></span> | <span data-ttu-id="24e6b-116">Value</span><span class="sxs-lookup"><span data-stu-id="24e6b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24e6b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24e6b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="24e6b-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24e6b-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="24e6b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24e6b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="24e6b-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24e6b-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="24e6b-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="24e6b-121">Namespace</span></span><br/>                | <span data-ttu-id="24e6b-122">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="24e6b-122">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="24e6b-123">MOF</span><span class="sxs-lookup"><span data-stu-id="24e6b-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24e6b-124"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24e6b-124"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="24e6b-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="24e6b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24e6b-126"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24e6b-126"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24e6b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="24e6b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24e6b-128">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="24e6b-128">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="24e6b-129">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="24e6b-129">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

