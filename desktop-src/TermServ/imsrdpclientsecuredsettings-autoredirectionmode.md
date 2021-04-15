---
title: Propiedad AudioRedirectionMode de IMsRdpClientSecuredSettings
description: Especifica la configuración de redirección de audio, que especifica si se deben redirigir sonidos o reproducir sonidos en el servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: 6aa63a50-a714-4a9b-a4ec-c0551920467a
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AudioRedirectionMode
- Propiedad AudioRedirectionMode Servicios de Escritorio remoto, interfaz IMsRdpClientSecuredSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientSecuredSettings, propiedad AudioRedirectionMode
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
ms.openlocfilehash: 858342811ec97def95031ebed0605b5a81cf80fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535571"
---
# <a name="imsrdpclientsecuredsettingsaudioredirectionmode-property"></a>IMsRdpClientSecuredSettings:: AudioRedirectionMode (propiedad)

Especifica la configuración de redirección de audio, que especifica si se deben redirigir sonidos o reproducir sonidos en el servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_AudioRedirectionMode(
  [in]  LONG audioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] LONG *paudioRedirectionMode
);
```



## <a name="property-value"></a>Valor de propiedad

La nueva configuración. Este parámetro puede ser uno de los valores siguientes.

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

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="remarks"></a>Observaciones

Estas propiedades no se pueden establecer cuando el control está conectado.

Para obtener más información, consulte [proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md) .

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings se define como 605befcf-39c1-45cc-A811-068fb7be346d<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





