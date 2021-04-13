---
title: 'IDeliveryOptimizationFile2:: GetProperty (método)'
description: 'Este método devuelve una única propiedad del archivo DO. | IDeliveryOptimizationFile2:: GetProperty (método)'
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
ms.openlocfilehash: c53167287cf821ceca26782dab9b8011d40a1785
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362344"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a>IDeliveryOptimizationFile2:: GetProperty (método)

Este método devuelve una única propiedad del archivo DO.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*propId* \[ de\]
</dt> <dd>

El identificador de propiedad necesario para obtener de tipo DOFilePropertyId.

</dd> <dt>

*propValue* \[ enuncia\]
</dt> <dd>

Valor de propiedad almacenado en una variante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores HRESULT.

| Código devuelto                  | Descripción                                         |
|------------------------------|-----------------------------------------------------|
| **S_OK**                     | Correcto                                             |
| **DO_E_UNKNOWN_PROPERTY_ID** | IDENTIFICADOR de propiedad desconocido.                                |
| **DO_E_WRITE_ONLY_PROPERTY** | La propiedad es de solo escritura y no se puede leer.      |
| **E_NOT_SET**                | No se estableció ninguna propiedad mediante el método SetProperty. |
| **E_OUTOFMEMORY**            |  Error de asignación de memoria                          |

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
