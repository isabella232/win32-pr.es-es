---
title: Propiedad Property de la interfaz IMsRdpExtendedSettings
description: Contiene una propiedad con nombre.
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Propiedad de propiedad Servicios de Escritorio remoto
- Propiedad de propiedad Servicios de Escritorio remoto, interfaz IMsRdpExtendedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpExtendedSettings, propiedad propiedad
topic_type:
- apiref
api_name:
- IMsRdpExtendedSettings.Property
- IMsRdpExtendedSettings.get_Property
- IMsRdpExtendedSettings.put_Property
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eadc8ce59e5a2bd50a4e61ad75b5124b24c21b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "103805162"
---
# <a name="imsrdpextendedsettingsproperty-property"></a>IMsRdpExtendedSettings::P propiedad filtros

Contiene una propiedad con nombre.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Property(
  [in]          BSTR    bstrPropertyName,
  [in]          VARIANT *pValue
);

HRESULT get_Property(
  [in]          BSTR    bstrPropertyName,
  [out, retval] VARIANT *pValue
);
```



## <a name="property-value"></a>Valor de propiedad

Valor de la propiedad con nombre.

| Nombre de propiedad | Tipo de datos | Access | Se puede cambiar una vez iniciada la conexión | Descripción |
|----------|-----------|--------|-----------------------------------------|-------------|
| ConnectToChildSession | **VT \_ bool** | Lectura/Escritura | Sí | Establecer esta propiedad en **true** hace que el control de cliente se conecte a la sesión secundaria en el equipo local en lugar de a un servidor remoto. Si esta propiedad se establece en **true**, no se puede conectar a un servidor remoto porque todas las conexiones se redirigen a localhost. Para obtener más información sobre las sesiones secundarias, vea [sesiones secundarias](child-sessions.md). |
| DisableCredentialsDelegation | **VT \_ bool** | Lectura/Escritura | No | Si **es true**, las credenciales no se envían al servidor remoto. |
| EnableFrameBufferRedirection | **VT \_ bool** | Lectura/Escritura | No | Si es **true**, se intenta la redirección de búfer de fotogramas. En el caso de una conexión de bucle invertido (el mismo equipo es el cliente y el servidor), el redireccionamiento de búfer de fotogramas permite compartir la memoria del búfer de fotogramas entre las sesiones. |
| EnableHardwareMode | **VT \_ bool**  | Solo escritura | No | Si es **true**, se intenta el hardware de ayuda con la descodificación de gráficos. |
| IgnoreCursors | **VT \_ bool** | Solo escritura | No | Si **es true**, se omiten los cursores enviados por el servidor remoto. |
| ManualClipboardSyncEnabled | **VT \_ bool** | Lectura/Escritura | Sí | Establecer esta propiedad en **true** significa que los portapapeles locales y remotos no se mantendrán automáticamente sincronizados. En su lugar, se debe usar la interfaz [**IMsRdpClipboard**](imsrdpclipboard.md) para sincronizar los formatos del Portapapeles desde el portapapeles local con el portapapeles remoto y el portapapeles remoto con el portapapeles local. |
| ZoomLevel ( | **_VT \_ UI4_* | Lectura/Escritura | Sí | Implementa la característica de zoom mediante el control ActiveX RDP. La característica de zoom está disponible en el menú **sistema** de RDP. La propiedad **zoomLevel (** no tiene ningún efecto en el modo RemoteApp y en el modo de pantalla completa. [**IMsRdpClientAdvancedSettings:: SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) y **zoomLevel (** se excluyen mutuamente. |

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                                                                                                                                                                                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                                                                                                                                                                                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| CLSID<br/>                    | CLSID \_ MsRdpClient7NotSafeForScripting se define como 54d38bf7-b1ef-4479-9674-1bd6ea465258<br/> CLSID \_ MsRdpClient8NotSafeForScripting se define como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpExtendedSettings se define como 302D8188-0052-4807-806A-362B628F9AC5<br/>                                                                                                                                                                                                                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpExtendedSettings**](imsrdpextendedsettings.md)
</dt> </dl>

 

 





