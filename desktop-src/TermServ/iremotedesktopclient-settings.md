---
title: Propiedad de configuración IRemoteDesktopClient
description: Recupera el objeto de configuración para el cliente del contenedor de la aplicación Protocolo de escritorio remoto (RDP).
ms.assetid: 59999489-9ad0-4b85-9643-3b8355b817c2
ms.tgt_platform: multiple
keywords:
- Propiedad de configuración Servicios de Escritorio remoto
- Propiedad settings Servicios de Escritorio remoto, interfaz IRemoteDesktopClient
- Servicios de Escritorio remoto de la interfaz IRemoteDesktopClient, propiedad settings
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
ms.openlocfilehash: 45e84324eaa12610d7ab898cbcb181e7712bc021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996676"
---
# <a name="iremotedesktopclientsettings-property"></a>IRemoteDesktopClient:: Settings (propiedad)

Recupera el objeto de configuración para el cliente del contenedor de la aplicación Protocolo de escritorio remoto (RDP).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Settings(
  [out, retval] IRemoteDesktopClientSettings **Settings
);
```



## <a name="property-value"></a>Valor de propiedad

El objeto de configuración para el cliente RDP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| IID<br/>                      | IID \_ IRemoteDesktopClient se define como 57D25668-625A-4905-BE4E-304CAA13F89C<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRemoteDesktopClient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
</dt> </dl>

 

