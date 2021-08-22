---
title: IDeliveryOptimizationFile2::SetProperty (método)
description: Este método devuelve una sola propiedad del archivo DO. | IDeliveryOptimizationFile2::SetProperty (método)
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
ms.openlocfilehash: 99ed42acb94f260e229abfe9df428aaa61d3658cb887892b84bb73fd6e7e63e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635725"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a>IDeliveryOptimizationFile2::SetProperty (método)

Este método devuelve una sola propiedad del archivo DO.

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
| **S_OK**                     | Success                                                            |
| **DO_E_UNKNOWN_PROPERTY_ID** | Identificador de propiedad desconocido                                                |
| **DO_E_INVALID_STATE**       | El trabajo no está actualmente en un estado que permita una configuración de propiedad |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|---------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible  | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]                                   |
| Servidor mínimo compatible  | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]                               |
| Header                    | Deliveryoptimization.h                                                           |
| Idl                       | DeliveryOptimization.idl                                                         |
| Biblioteca                   | Dosvc.lib                                                                        |
| Archivo DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 se define como 18995A26-BF59-4MIENTO-9F8B-D5092D5A2405 |

## <a name="see-also"></a>Vea también

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
