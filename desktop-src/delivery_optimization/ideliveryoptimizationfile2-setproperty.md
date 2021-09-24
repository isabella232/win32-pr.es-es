---
title: IDeliveryOptimizationFile2::SetProperty (Método)
description: Este método devuelve una sola propiedad del Optimización de distribución archivo. | IDeliveryOptimizationFile2::SetProperty (Método)
keywords:
- SetProperty (método)
- Método SetProperty, interfaz IDeliveryOptimizationFile2
- Interfaz IDeliveryOptimizationFile2, método SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9c392c603ed067520b0f189dfbf547bc12ee80a
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520827"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a>IDeliveryOptimizationFile2::SetProperty (Método)

Este método devuelve una sola propiedad del Optimización de distribución archivo.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*propId* \[ En\]
</dt> <dd>

Identificador de propiedad necesario para establecer el tipo DOFilePropertyId.

</dd> <dt>

*propValue* \[ En\]
</dt> <dd>

Valor de propiedad que se establece, de tipo VARIANT.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores HRESULT.

| Código devuelto                  | Descripción                                                        |
|------------------------------|--------------------------------------------------------------------|
| **S_OK**                     | Correcto                                                            |
| **DO_E_UNKNOWN_PROPERTY_ID** | Id. de propiedad desconocida                                                |
| **DO_E_INVALID_STATE**       | El trabajo no está actualmente en un estado que permita una configuración de propiedad |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|---------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible  | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]                                   |
| Servidor mínimo compatible  | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]                               |
| Encabezado                    | Deliveryoptimization.h                                                           |
| IDL                       | DeliveryOptimization.idl                                                         |
| Biblioteca                   | Dosvc.lib                                                                        |
| Archivo DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 se define como 18995A26-BF59-4MIENTO-9F8B-D5092D5A2405 |

## <a name="see-also"></a>Consulte también

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
