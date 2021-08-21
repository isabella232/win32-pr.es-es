---
title: IDeliveryOptimizationJob2::GetProperty (método)
description: Devuelve una sola propiedad del trabajo do.
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
ms.openlocfilehash: cdca86cb374eded0eabcc1d623d2218a6dc1f4cd5613a18e16b4ec9ab93156b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811256"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a>IDeliveryOptimizationJob2::GetProperty (método)

Este método devuelve una sola propiedad del trabajo do.

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
| **S_OK**                     | Success              |
| **DO_E_UNKNOWN_PROPERTY_ID** | Identificador de propiedad desconocido. |

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

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
