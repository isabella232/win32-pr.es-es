---
title: Método SendLocation2D de la interfaz IMsRdpClientNonScriptable6
description: Envía un valor de latitud y longitud al servidor para que la ubicación geográfica del cliente se pueda reflejar en la sesión remota.
ms.tgt_platform: multiple
keywords:
- Método SendLocation2D Servicios de Escritorio remoto
- Método SendLocation2D Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable6
- Interfaz IMsRdpClientNonScriptable6 Servicios de Escritorio remoto, método SendLocation2D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation2D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 2e2e252f86249531c61922cf02f308bfaf2b76c2518ff9b420f5ec3fd80d9d88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990145"
---
# <a name="imsrdpclientnonscriptable6sendlocation2d-method"></a>Método IMsRdpClientNonScriptable6::SendLocation2D

Envía un valor de latitud y longitud al servidor para que la ubicación geográfica del cliente se pueda reflejar en la sesión remota.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT SendLocation2D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude
);
```

## <a name="parameters"></a>Parámetros

*latitud* \[ En\]

Latitud de una ubicación geográfica. El intervalo válido de valores de latitud está entre -90,0 y 90,0 grados.

*longitud* \[ En\]

Longitud de una ubicación geográfica. El intervalo válido de valores de latitud está entre -180,0 y 180,0 grados.

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** se realiza correctamente.

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
