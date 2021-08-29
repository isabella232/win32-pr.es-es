---
title: Propiedad Redirected de la interfaz IMsRdpCameraRedirConfig
description: Especifica si se redirige o no la cámara.
ms.tgt_platform: multiple
keywords:
- Propiedades redirigidas Servicios de Escritorio remoto
- Propiedad redirigida Servicios de Escritorio remoto interfaz , IMsRdpCameraRedirConfig
- Interfaz IMsRdpCameraRedirConfig Servicios de Escritorio remoto , propiedad redirigida
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.Redirected
- IMsRdpCameraRedirConfig.put_Redirected
- IMsRdpCameraRedirConfig.get_Redirected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 6f02d8764eb8fd9cb9f74bc42f8e8a3fee518e2d0841dd8a2ca23fa562354240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400985"
---
# <a name="imsrdpcameraredirconfigredirected-property"></a>Propiedad IMsRdpCameraRedirConfig::Redirected

Especifica si se redirige o no la cámara.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax

```C++
HRESULT put_Redirected(
    [in] VARIANT_BOOL fRedirected
);

HRESULT get_Redirected(
    [out, retval] VARIANT_BOOL* pfRedirected
);
```

## <a name="property-value"></a>Valor de propiedad

Valor que especifica si se redirige o no la cámara.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1803 (compilación 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfig se define como 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
</dt> </dl>