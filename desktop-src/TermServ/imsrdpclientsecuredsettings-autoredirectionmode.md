---
title: Propiedad IMsRdpClientSecuredSettings AudioRedirectionMode
description: Especifica la configuración de redireccionamiento de audio, que especifica si se deben redirigir sonidos o reproducir sonidos en el servidor Escritorio remoto session host (host de sesión de Escritorio remoto).
ms.assetid: 6aa63a50-a714-4a9b-a4ec-c0551920467a
ms.tgt_platform: multiple
keywords:
- Propiedad AudioRedirectionMode Servicios de Escritorio remoto
- Propiedad AudioRedirectionMode Servicios de Escritorio remoto , interfaz IMsRdpClientSecuredSettings
- Interfaz IMsRdpClientSecuredSettings Servicios de Escritorio remoto , propiedad AudioRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.AudioRedirectionMode
- IMsRdpClientSecuredSettings.get_AudioRedirectionMode
- IMsRdpClientSecuredSettings.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef48b0898dd461c9be4e4e9d0cd443d4f9cf8ab8aaad34de1ca0ad9e3218c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117941092"
---
# <a name="imsrdpclientsecuredsettingsaudioredirectionmode-property"></a>Propiedad IMsRdpClientSecuredSettings::AudioRedirectionMode

Especifica la configuración de redireccionamiento de audio, que especifica si se deben redirigir sonidos o reproducir sonidos en el servidor Escritorio remoto session host (host de sesión de Escritorio remoto).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AudioRedirectionMode(
  [in]  LONG audioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] LONG *paudioRedirectionMode
);
```



## <a name="property-value"></a>Valor de propiedad

Nueva configuración. Este parámetro puede ser uno de los valores siguientes.

<dt>

0
</dt> <dd>

Redirigir sonidos al cliente. Este es el valor predeterminado.

</dd> <dt>

1
</dt> <dd>

Reproducir sonidos en el equipo remoto.

</dd> <dt>

2
</dt> <dd>

Deshabilitar el redireccionamiento de sonido; no reproducir sonidos en el servidor.

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

Estas propiedades no se pueden establecer cuando el control está conectado.

Consulte Proporcionar [seguridad de cliente RDP](providing-for-rdp-client-security.md) para obtener más información.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings se define como 605befcf-39c1-45cc-a811-068fb7be346d<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





