---
description: Se usa para controlar el estado de brillo del sensor de luz ambiente.
ms.assetid: ff400d4e-be8c-450b-ad53-d43b0ab84ab3
title: Método WmiSetALSBrightnessState de la clase WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightnessState
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 593b007f75c7eb134de4bb4c9f83c7246e9a51b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697852"
---
# <a name="wmisetalsbrightnessstate-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="d3c8c-103">Método WmiSetALSBrightnessState de la clase WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="d3c8c-103">WmiSetALSBrightnessState method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="d3c8c-104">El método **WmiSetALSBrightnessState** se usa para controlar el estado de brillo del sensor de luz ambiente.</span><span class="sxs-lookup"><span data-stu-id="d3c8c-104">The **WmiSetALSBrightnessState** method is used to control the ambient light sensor brightness state.</span></span> <span data-ttu-id="d3c8c-105">Si se estableció una invalidación de brillo activa mediante el método [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) , esa invalidación tendrá prioridad sobre el conjunto de brillo de ALS mediante este método.</span><span class="sxs-lookup"><span data-stu-id="d3c8c-105">If an active brightness override was established by using the [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) method, that override will take precedence over the ALS brightness set by using this method.</span></span> <span data-ttu-id="d3c8c-106">Para que una invalidación de brillo de ALS habilitada surta efecto, se debe revertir la Directiva de brillo mediante el método [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) .</span><span class="sxs-lookup"><span data-stu-id="d3c8c-106">For an enabled ALS brightness override to take effect, the brightness policy has to be reverted by using the [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c8c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3c8c-107">Syntax</span></span>


```mof
uint32 WmiSetALSBrightnessState(
   boolean State
);
```



## <a name="parameters"></a><span data-ttu-id="d3c8c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3c8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3c8c-109">*State*</span><span class="sxs-lookup"><span data-stu-id="d3c8c-109">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="d3c8c-110">Estado de brillo de ALS.</span><span class="sxs-lookup"><span data-stu-id="d3c8c-110">ALS brightness state.</span></span> <span data-ttu-id="d3c8c-111">False deshabilita la invalidación de brillo de ALS y true la habilita.</span><span class="sxs-lookup"><span data-stu-id="d3c8c-111">False disables the ALS brightness override and true enables it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3c8c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3c8c-112">Return value</span></span>

<span data-ttu-id="d3c8c-113">Devuelve cero (0) para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d3c8c-113">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="d3c8c-114">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="d3c8c-114">Any other number indicates an error.</span></span> <span data-ttu-id="d3c8c-115">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d3c8c-115">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c8c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3c8c-116">Requirements</span></span>



| <span data-ttu-id="d3c8c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3c8c-117">Requirement</span></span> | <span data-ttu-id="d3c8c-118">Value</span><span class="sxs-lookup"><span data-stu-id="d3c8c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c8c-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3c8c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c8c-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3c8c-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d3c8c-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3c8c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c8c-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3c8c-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d3c8c-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d3c8c-123">Namespace</span></span><br/>                | <span data-ttu-id="d3c8c-124">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="d3c8c-124">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="d3c8c-125">MOF</span><span class="sxs-lookup"><span data-stu-id="d3c8c-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3c8c-126"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3c8c-126"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3c8c-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d3c8c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3c8c-128"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3c8c-128"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3c8c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3c8c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c8c-130">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="d3c8c-130">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="d3c8c-131">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="d3c8c-131">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

