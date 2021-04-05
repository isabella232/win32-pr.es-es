---
description: Se usa para establecer el valor de brillo del sensor de luz ambiente.
ms.assetid: 8b3ec692-4043-42b3-8dd6-7a147620e382
title: Método WmiSetALSBrightness de la clase WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 0768917f9197b6ee3de52877e031acbbdc8f9aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279465"
---
# <a name="wmisetalsbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="51513-103">Método WmiSetALSBrightness de la clase WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="51513-103">WmiSetALSBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="51513-104">El método **WmiSetALSBrightness** se usa para establecer el valor de brillo del sensor de luz ambiente.</span><span class="sxs-lookup"><span data-stu-id="51513-104">The **WmiSetALSBrightness** method is used to set the ambient light sensor brightness value.</span></span> <span data-ttu-id="51513-105">Si se estableció una invalidación de brillo activa mediante el método [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) , esa invalidación tendrá prioridad sobre el conjunto de brillo de ALS mediante este método.</span><span class="sxs-lookup"><span data-stu-id="51513-105">If an active brightness override was established by using the [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) method, that override will take precedence over the ALS brightness set by using this method.</span></span> <span data-ttu-id="51513-106">Para que una invalidación de brillo de ALS habilitada surta efecto, se debe revertir la Directiva de brillo mediante el método [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) .</span><span class="sxs-lookup"><span data-stu-id="51513-106">For an enabled ALS brightness override to take effect, the brightness policy has to be reverted by using the [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="51513-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51513-107">Syntax</span></span>


```mof
uint32 WmiSetALSBrightness(
   uint8 Brightness
);
```



## <a name="parameters"></a><span data-ttu-id="51513-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51513-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51513-109">*Luminosidad*</span><span class="sxs-lookup"><span data-stu-id="51513-109">*Brightness*</span></span> 
</dt> <dd>

<span data-ttu-id="51513-110">Brillo de ALS como un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="51513-110">The ALS brightness as a percentage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51513-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51513-111">Return value</span></span>

<span data-ttu-id="51513-112">Devuelve cero (0) para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="51513-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="51513-113">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="51513-113">Any other number indicates an error.</span></span> <span data-ttu-id="51513-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="51513-114">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="51513-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51513-115">Requirements</span></span>



| <span data-ttu-id="51513-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="51513-116">Requirement</span></span> | <span data-ttu-id="51513-117">Value</span><span class="sxs-lookup"><span data-stu-id="51513-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51513-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51513-118">Minimum supported client</span></span><br/> | <span data-ttu-id="51513-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51513-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="51513-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51513-120">Minimum supported server</span></span><br/> | <span data-ttu-id="51513-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51513-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="51513-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="51513-122">Namespace</span></span><br/>                | <span data-ttu-id="51513-123">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="51513-123">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="51513-124">MOF</span><span class="sxs-lookup"><span data-stu-id="51513-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51513-125"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51513-125"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="51513-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="51513-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51513-127"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51513-127"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51513-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="51513-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51513-129">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="51513-129">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="51513-130">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="51513-130">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

