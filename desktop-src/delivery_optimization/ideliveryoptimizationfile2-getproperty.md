---
title: IDeliveryOptimizationFile2::GetProperty (método)
description: Este método devuelve una sola propiedad del Optimización de distribución archivo. | IDeliveryOptimizationFile2::GetProperty (método)
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
ms.openlocfilehash: b3b89c054d1d45023a0237aa6f1f3e186c2c836e
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520966"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a>IDeliveryOptimizationFile2::GetProperty (método)

Este método devuelve una sola propiedad del Optimización de distribución archivo.

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
