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
# <a name="iaccessibilitydockingservicegetavailablesize-method"></a>IAccessibilityDockingService:: GetAvailableSize (método)

Obtiene las dimensiones disponibles para acoplar una ventana de accesibilidad en un monitor.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAvailableSize(
  [in]  HMONITOR hMonitor,
  [out] UINT     *puMaxHeight,
  [out] UINT     *puFixedWidth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMonitor* \[ de\]
</dt> <dd>

Especifica el monitor para el que se recuperará el tamaño de acoplamiento disponible.

</dd> <dt>

*puMaxHeight* \[ enuncia\]
</dt> <dd>

Si se realiza correctamente, se establece en el alto máximo disponible para el acoplamiento en el *hMonitor* especificado, en píxeles.

En caso de error, establezca en cero.

</dd> <dt>

*puFixedWidth* \[ enuncia\]
</dt> <dd>

Si se realiza correctamente, se establece en el ancho fijo disponible para el acoplamiento en el *hMonitor* especificado, en píxeles. Cualquier ventana acoplada a este *hMonitor* de tamaño se ajustará a este ancho.

En caso de error, establezca en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Código devuelto                                                                                                                          | Descripción                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                                 | Correcto.<br/>                                                              |
| <dl> <dt>**HRESULT \_ de \_ Win32 (error \_ de \_ identificador de monitor no válido \_ )**</dt> </dl> | El monitor especificado por el identificador de monitor no admite el acoplamiento.<br/> |



 

Si *puMaxHeight* o *puFixedWidth* son NULL, se producirá una infracción de acceso.

## <a name="remarks"></a>Observaciones

Las ventanas de accesibilidad solo se pueden acoplar a un monitor que tenga al menos 768 píxeles de pantalla verticales. Esta API no permitirá que estas ventanas se acoplen con un alto que haría que las aplicaciones de la tienda Windows dispongan de menos de 768 píxeles de pantalla verticales.

## <a name="examples"></a>Ejemplos


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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAccessibilityDockingService**](/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice)
</dt> </dl>

 

 





