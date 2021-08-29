---
title: Propiedad Configuración IRemoteDesktopClient
description: Recupera el objeto de configuración para el cliente Protocolo de escritorio remoto de contenedor de aplicaciones (RDP).
ms.assetid: 59999489-9ad0-4b85-9643-3b8355b817c2
ms.tgt_platform: multiple
keywords:
- Configuración propiedad Servicios de Escritorio remoto
- Configuración propiedad Servicios de Escritorio remoto , interfaz IRemoteDesktopClient
- Interfaz IRemoteDesktopClient Servicios de Escritorio remoto , Configuración propiedad
topic_type:
- apiref
api_name:
- IRemoteDesktopClient.Settings
- IRemoteDesktopClient.get_Settings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6f3369948cb99e67a345348c79073109ff5a9f929a2ff09b1acb510930bb2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125025"
---
# <a name="iremotedesktopclientsettings-property"></a>IRemoteDesktopClient::Configuración propiedad

Recupera el objeto de configuración para el cliente Protocolo de escritorio remoto de contenedor de aplicaciones (RDP).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Settings(
  [out, retval] IRemoteDesktopClientSettings **Settings
);
```



## <a name="property-value"></a>Valor de propiedad

Objeto de configuración para el cliente RDP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| IID<br/>                      | IID IRemoteDesktopClient se define como \_ 57D25668-625A-4905-BE4E-304CAA13F89C<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRemoteDesktopClient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
</dt> </dl>

 

