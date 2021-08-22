---
title: IDeliveryOptimizationFile2::GetProperty (método)
description: Este método devuelve una sola propiedad del archivo DO. | IDeliveryOptimizationFile2::GetProperty (método)
keywords:
- Método GetProperty
- Método GetProperty, interfaz IDeliveryOptimizationFile2
- Interfaz IDeliveryOptimizationFile2, método GetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0f181eebe2aff8ccbbbf6d5400e3d5a78f123e2304567a413ecf4a35357229b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542095"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a>IDeliveryOptimizationFile2::GetProperty (método)

Este método devuelve una sola propiedad del archivo DO.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*propId* \[ En\]
</dt> <dd>

Identificador de propiedad necesario para obtener del tipo DOFilePropertyId.

</dd> <dt>

*propValue* \[ out\]
</dt> <dd>

Valor de propiedad almacenado en variant.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores HRESULT.

| Código devuelto                  | Descripción                                         |
|------------------------------|-----------------------------------------------------|
| **S_OK**                     | Correcto                                             |
| **DO_E_UNKNOWN_PROPERTY_ID** | Identificador de propiedad desconocido.                                |
| **DO_E_WRITE_ONLY_PROPERTY** | La propiedad es de solo escritura y no se puede leer.      |
| **E_NOT_SET**                | No se estableció ninguna propiedad a través del método SetProperty. |
| **E_OUTOFMEMORY**            |  Error de asignación de memoria                          |

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

## <a name="see-also"></a>Consulte también

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
