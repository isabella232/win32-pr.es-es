---
title: 'IDeliveryOptimizationFile2:: SetProperty (método)'
description: 'Este método devuelve una única propiedad del archivo DO. | IDeliveryOptimizationFile2:: SetProperty (método)'
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
ms.openlocfilehash: 74113fca944e79e9ecba8f822f73769775631821
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717491"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a>IDeliveryOptimizationFile2:: SetProperty (método)

Este método devuelve una única propiedad del archivo DO.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*propId* \[ de\]
</dt> <dd>

El identificador de propiedad necesario para establecer de tipo DOFilePropertyId.

</dd> <dt>

*propValue* \[ de\]
</dt> <dd>

Valor de propiedad que se va a establecer, de tipo VARIANT.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores HRESULT.

| Código devuelto                  | Descripción                                                        |
|------------------------------|--------------------------------------------------------------------|
| **S_OK**                     | Correcto                                                            |
| **DO_E_UNKNOWN_PROPERTY_ID** | IDENTIFICADOR de propiedad desconocido                                                |
| **DO_E_INVALID_STATE**       | El trabajo no está actualmente en un estado que permita una configuración de propiedad |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|---------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible  | Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]                                   |
| Servidor mínimo compatible  | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]                               |
| Encabezado                    | Deliveryoptimization. h                                                           |
| IDL                       | DeliveryOptimization. idl                                                         |
| Biblioteca                   | Dosvc. lib                                                                        |
| Archivo DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 se define como 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>Vea también

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
