---
title: 'IDeliveryOptimizationJob2:: GetProperty (método)'
description: Devuelve una única propiedad del trabajo.
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
ms.openlocfilehash: 52e405685534c0dbae7c8c205dc5e114a3dbe68b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489826"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a>IDeliveryOptimizationJob2:: GetProperty (método)

Este método devuelve una única propiedad del trabajo.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT GetProperty(
  [in]  DOJobPropertyId propId,
  [out] VARIANT         *propValue
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*propId* \[ de\]
</dt> <dd>

IDENTIFICADOR de propiedad necesario que se va a obtener. Solo se admite **DOJobPropertyId_ExtendedErrorInfo** de tipo VT_BSTR.

</dd> <dt>

*propValue* \[ enuncia\]
</dt> <dd>

Valor de propiedad resultante, almacenado en un tipo VARIANT.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores HRESULT.

| Código devuelto                  | Descripción          |
|------------------------------|----------------------|
| **S_OK**                     | Correcto              |
| **DO_E_UNKNOWN_PROPERTY_ID** | IDENTIFICADOR de propiedad desconocido. |

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
