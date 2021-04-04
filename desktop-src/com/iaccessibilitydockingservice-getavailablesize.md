---
title: IAccessibilityDockingService GetAvailableSize, método
description: Obtiene las dimensiones disponibles para acoplar una ventana de accesibilidad en un monitor.
ms.assetid: 1C838B01-EF26-4FCC-878F-A36DEFBA3142
keywords:
- Método GetAvailableSize COM
- Método GetAvailableSize COM, interfaz IAccessibilityDockingService
- Interfaz IAccessibilityDockingService COM, método GetAvailableSize
topic_type:
- apiref
api_name:
- IAccessibilityDockingService.GetAvailableSize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1b9f113792b14f5fb86e0349d083ea48ffdb3fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076690"
---
# <a name="iaccessibilitydockingservicegetavailablesize-method"></a><span data-ttu-id="38f9a-106">IAccessibilityDockingService:: GetAvailableSize (método)</span><span class="sxs-lookup"><span data-stu-id="38f9a-106">IAccessibilityDockingService::GetAvailableSize method</span></span>

<span data-ttu-id="38f9a-107">Obtiene las dimensiones disponibles para acoplar una ventana de accesibilidad en un monitor.</span><span class="sxs-lookup"><span data-stu-id="38f9a-107">Gets the dimensions available for docking an accessibility window on a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="38f9a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38f9a-108">Syntax</span></span>


```C++
HRESULT GetAvailableSize(
  [in]  HMONITOR hMonitor,
  [out] UINT     *puMaxHeight,
  [out] UINT     *puFixedWidth
);
```



## <a name="parameters"></a><span data-ttu-id="38f9a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38f9a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38f9a-110">*hMonitor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="38f9a-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38f9a-111">Especifica el monitor para el que se recuperará el tamaño de acoplamiento disponible.</span><span class="sxs-lookup"><span data-stu-id="38f9a-111">Specifies the monitor for which the available docking size will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="38f9a-112">*puMaxHeight* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="38f9a-112">*puMaxHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38f9a-113">Si se realiza correctamente, se establece en el alto máximo disponible para el acoplamiento en el *hMonitor* especificado, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="38f9a-113">On success, set to the maximum height available for docking on the specified *hMonitor*, in pixels.</span></span>

<span data-ttu-id="38f9a-114">En caso de error, establezca en cero.</span><span class="sxs-lookup"><span data-stu-id="38f9a-114">On failure, set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="38f9a-115">*puFixedWidth* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="38f9a-115">*puFixedWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38f9a-116">Si se realiza correctamente, se establece en el ancho fijo disponible para el acoplamiento en el *hMonitor* especificado, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="38f9a-116">On success, set to the fixed width available for docking on the specified *hMonitor*, in pixels.</span></span> <span data-ttu-id="38f9a-117">Cualquier ventana acoplada a este *hMonitor* de tamaño se ajustará a este ancho.</span><span class="sxs-lookup"><span data-stu-id="38f9a-117">Any window docked to this *hMonitor* will be sized to this width.</span></span>

<span data-ttu-id="38f9a-118">En caso de error, establezca en cero.</span><span class="sxs-lookup"><span data-stu-id="38f9a-118">On failure, set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38f9a-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38f9a-119">Return value</span></span>



| <span data-ttu-id="38f9a-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="38f9a-120">Return code</span></span>                                                                                                                          | <span data-ttu-id="38f9a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="38f9a-121">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="38f9a-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="38f9a-122"><dt>**S\_OK**</dt></span></span> </dl>                                                 | <span data-ttu-id="38f9a-123">Correcto.</span><span class="sxs-lookup"><span data-stu-id="38f9a-123">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="38f9a-124"><dt>**HRESULT \_ de \_ Win32 (error \_ de \_ identificador de monitor no válido \_ )**</dt></span><span class="sxs-lookup"><span data-stu-id="38f9a-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_MONITOR\_HANDLE)**</dt></span></span> </dl> | <span data-ttu-id="38f9a-125">El monitor especificado por el identificador de monitor no admite el acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="38f9a-125">The monitor specified by the monitor handle does not support docking.</span></span><br/> |



 

<span data-ttu-id="38f9a-126">Si *puMaxHeight* o *puFixedWidth* son NULL, se producirá una infracción de acceso.</span><span class="sxs-lookup"><span data-stu-id="38f9a-126">If either *puMaxHeight* or *puFixedWidth* are null, an access violation will occur.</span></span>

## <a name="remarks"></a><span data-ttu-id="38f9a-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38f9a-127">Remarks</span></span>

<span data-ttu-id="38f9a-128">Las ventanas de accesibilidad solo se pueden acoplar a un monitor que tenga al menos 768 píxeles de pantalla verticales.</span><span class="sxs-lookup"><span data-stu-id="38f9a-128">Accessibility windows can only be docked to a monitor that has at least 768 vertical screen pixels.</span></span> <span data-ttu-id="38f9a-129">Esta API no permitirá que estas ventanas se acoplen con un alto que haría que las aplicaciones de la tienda Windows dispongan de menos de 768 píxeles de pantalla verticales.</span><span class="sxs-lookup"><span data-stu-id="38f9a-129">This API will not allow such windows to be docked with a height that would cause Windows Store apps to have less than 768 vertical screen pixels.</span></span>

## <a name="examples"></a><span data-ttu-id="38f9a-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="38f9a-130">Examples</span></span>


```
IAccessibilityDockingService *pDockingService;
HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, CLSCTX_INPROV_SERVER, nullptr, IID_PPV_ARGS(&pDockingService));
if (SUCCEEDED(hr))
{
    UINT uMaxHeight;
    UINT uFixedWidth;

    HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
    if (hMonitor != nullptr)
    {
        hr = pDockingService->GetAvailableSize(hMonitor, &uMaxHeight, &uFixedWidth);
    }
}
```



## <a name="see-also"></a><span data-ttu-id="38f9a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="38f9a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f9a-132">**IAccessibilityDockingService**</span><span class="sxs-lookup"><span data-stu-id="38f9a-132">**IAccessibilityDockingService**</span></span>](/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice)
</dt> </dl>

 

 





