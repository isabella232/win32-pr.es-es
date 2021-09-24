---
title: IDeliveryOptimizationJob2::GetProperty (método)
description: Devuelve una sola propiedad del Optimización de distribución trabajo.
keywords:
- Método GetProperty
- Método GetProperty, interfaz IDeliveryOptimizationJob2
- Interfaz IDeliveryOptimizationJob2, método GetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b849d4d9871a730e420f95b52f26b73b8e7b7a7
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520642"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a>IDeliveryOptimizationJob2::GetProperty (método)

Este método devuelve una sola propiedad del Optimización de distribución trabajo.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT GetProperty(
  [in]  DOJobPropertyId propId,
  [out] VARIANT         *propValue
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*propId* \[ En\]
</dt> <dd>

Identificador de propiedad necesario que se debe obtener. Solo **DOJobPropertyId_ExtendedErrorInfo** de tipo VT_BSTR se admite.

</dd> <dt>

*propValue* \[ out\]
</dt> <dd>

Valor de propiedad resultante, almacenado en un tipo VARIANT.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores HRESULT.

| Código devuelto                  | Descripción          |
|------------------------------|----------------------|
| **S_OK**                     | Correcto              |
| **DO_E_UNKNOWN_PROPERTY_ID** | Identificador de propiedad desconocido. |

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

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
