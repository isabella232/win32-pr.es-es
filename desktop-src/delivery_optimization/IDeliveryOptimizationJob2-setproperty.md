---
title: 'IDeliveryOptimizationJob2:: SetProperty (método)'
description: Este método no se utiliza.
keywords:
- SetProperty (método)
- Método SetProperty, interfaz IDeliveryOptimizationJob2
- Interfaz IDeliveryOptimizationJob2, método SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41375ac3949dd4bcbdd22944f1f1a11d461fc3ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422372"
---
# <a name="ideliveryoptimizationjob2setproperty-method"></a>IDeliveryOptimizationJob2:: SetProperty (método)

Este método no se utiliza.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT SetProperty(
  [in]               DOJobPropertyId propId,
  [in, unique] const VARIANT         *propValue
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*propId* \[ de\]
</dt> <dd>

Sin usar.

</dd> <dt>

*propValue* \[ de\]
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si propId es **DOJobPropertyId_ExtendedErrorInfo**, el valor devuelto es **DO_E_READ_ONLY_PROPERTY**; en caso contrario, la función devuelve **DO_E_UNKNOWN_PROPERTY_ID**.

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

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
