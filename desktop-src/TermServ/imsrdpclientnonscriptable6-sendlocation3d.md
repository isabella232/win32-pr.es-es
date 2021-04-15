---
title: Método SendLocation3D de la interfaz IMsRdpClientNonScriptable6
description: Envía un valor de latitud, longitud y altitud al servidor para que la ubicación geográfica del cliente se pueda reflejar en la sesión remota.
ms.tgt_platform: multiple
keywords:
- Método SendLocation3D Servicios de Escritorio remoto
- Método SendLocation3D Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable6
- Interfaz IMsRdpClientNonScriptable6 Servicios de Escritorio remoto, método SendLocation3D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation3D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: c63e779b6d6d090544af40a7ee6d9c05f8c49494
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104494146"
---
# <a name="imsrdpclientnonscriptable6sendlocation3d-method"></a>IMsRdpClientNonScriptable6:: SendLocation3D (método)

Envía un valor de latitud, longitud y altitud al servidor para que la ubicación geográfica del cliente se pueda reflejar en la sesión remota.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT SendLocation3D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude,
  [in] INT32 altitude
);
```

## <a name="parameters"></a>Parámetros

*latitud* \[ de\]

La latitud de una ubicación geográfica. El intervalo válido de valores de latitud es de-90,0 a 90,0 grados.

*longitud* \[ de\]

Longitud de una ubicación geográfica. El intervalo válido de valores de latitud es de-180,0 a 180,0 grados.

*altitud* \[ de\]

La altitud de una ubicación geográfica en metros.

## <a name="return-value"></a>Valor devuelto

Vuelva **a \_ Aceptar si es** correcto.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1709 (compilación 16299)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable6 se define como 05293249-B28B-4DB8-BE64-1B2F496B910E            |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>
