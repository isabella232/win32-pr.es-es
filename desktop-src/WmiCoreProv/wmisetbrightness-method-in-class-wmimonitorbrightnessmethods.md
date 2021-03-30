---
description: Establece el brillo de la pantalla del monitor de un equipo.
ms.assetid: 900cf5fd-6888-4f0b-8e0b-01eeaaeeeb8f
title: Método WmiSetBrightness de la clase WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 599610b0d81de283d97ca347486c4adcbe0103dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082867"
---
# <a name="wmisetbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="32c35-103">Método WmiSetBrightness de la clase WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="32c35-103">WmiSetBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="32c35-104">El método **WmiSetBrightness** establece el brillo de la pantalla de un monitor del equipo.</span><span class="sxs-lookup"><span data-stu-id="32c35-104">The **WmiSetBrightness** method sets the display brightness of a computer monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="32c35-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32c35-105">Syntax</span></span>


```mof
uint32 WmiSetBrightness(
   uint32 Timeout,
   uint8  Brightness
);
```



## <a name="parameters"></a><span data-ttu-id="32c35-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32c35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32c35-107">*Tiempo de espera*</span><span class="sxs-lookup"><span data-stu-id="32c35-107">*Timeout*</span></span> 
</dt> <dd>

<span data-ttu-id="32c35-108">Tiempo de espera, en segundos.</span><span class="sxs-lookup"><span data-stu-id="32c35-108">Timeout, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="32c35-109">*Luminosidad*</span><span class="sxs-lookup"><span data-stu-id="32c35-109">*Brightness*</span></span> 
</dt> <dd>

<span data-ttu-id="32c35-110">Brillo, en porcentaje.</span><span class="sxs-lookup"><span data-stu-id="32c35-110">Brightness, in percent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32c35-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32c35-111">Return value</span></span>

<span data-ttu-id="32c35-112">Devuelve cero (0) para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="32c35-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="32c35-113">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="32c35-113">Any other number indicates an error.</span></span> <span data-ttu-id="32c35-114">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="32c35-114">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="examples"></a><span data-ttu-id="32c35-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="32c35-115">Examples</span></span>

<span data-ttu-id="32c35-116">Para obtener una explicación amplia de cómo recuperar y establecer el brillo del monitor, vea el tema blog sobre el [uso de PowerShell para notificar y establecer el brillo del monitor](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) .</span><span class="sxs-lookup"><span data-stu-id="32c35-116">For an extended discussion of retrieving and setting monitor brightness, see the Scripting Guy's [Use PowerShell to Report and Set Monitor Brightness](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) blog topic.</span></span>

<span data-ttu-id="32c35-117">En el siguiente ejemplo de PowerShell se establece el brillo del monitor en 50%.</span><span class="sxs-lookup"><span data-stu-id="32c35-117">The following PowerShell sample sets the brightness of the monitor to 50%.</span></span>


```PowerShell
$brightness = 50
$delay = 5
$myMonitor = Get-WmiObject -Namespace root\wmi -Class WmiMonitorBrightnessMethods
$myMonitor.wmisetbrightness($delay, $brightness)
```



## <a name="requirements"></a><span data-ttu-id="32c35-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32c35-118">Requirements</span></span>



| <span data-ttu-id="32c35-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="32c35-119">Requirement</span></span> | <span data-ttu-id="32c35-120">Value</span><span class="sxs-lookup"><span data-stu-id="32c35-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32c35-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32c35-121">Minimum supported client</span></span><br/> | <span data-ttu-id="32c35-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32c35-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="32c35-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32c35-123">Minimum supported server</span></span><br/> | <span data-ttu-id="32c35-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32c35-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="32c35-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="32c35-125">Namespace</span></span><br/>                | <span data-ttu-id="32c35-126">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="32c35-126">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="32c35-127">MOF</span><span class="sxs-lookup"><span data-stu-id="32c35-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32c35-128"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32c35-128"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="32c35-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32c35-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32c35-130"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32c35-130"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32c35-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="32c35-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32c35-132">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="32c35-132">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="32c35-133">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="32c35-133">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

