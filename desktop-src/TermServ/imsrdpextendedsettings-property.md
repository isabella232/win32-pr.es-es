---
title: Propiedad Property de la interfaz IMsRdpExtendedSettings
description: Contiene una propiedad con nombre.
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Propiedades de propiedad Servicios de Escritorio remoto
- Propiedad de Servicios de Escritorio remoto , interfaz IMsRdpExtendedSettings
- Interfaz IMsRdpExtendedSettings Servicios de Escritorio remoto , propiedad Property
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
ms.openlocfilehash: 7deeb0e4d6d0f393bae09bacc9ff6709defe51bf6ca6128cbeb64e2f4f6e35cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138508"
---
# <a name="imsrdpextendedsettingsproperty-property"></a>IMsRdpExtendedSettings::P roperty

Contiene una propiedad con nombre.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


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

Valor de propiedad con nombre.

| Nombre de propiedad | Tipo de datos | Access | Se puede cambiar después de iniciar la conexión | Descripción |
|----------|-----------|--------|-----------------------------------------|-------------|
| ConnectToChildSession | **VT \_ BOOL** | Lectura/Escritura | Sí | Al establecer esta propiedad en **True,** el control de cliente se conecta a la sesión secundaria en el equipo local en lugar de a un servidor remoto. Si esta propiedad se establece en **true**, no puede conectarse a un servidor remoto porque todas las conexiones se redirigen a localhost. Para obtener más información sobre las sesiones secundarias, vea [Sesiones secundarias](child-sessions.md). |
| DisableCredentialsDelegation | **VT \_ BOOL** | Lectura/Escritura | No | Si **es True,** las credenciales no se envían al servidor remoto. |
| EnableFrameBufferRedirection | **VT \_ BOOL** | Lectura/Escritura | No | Si es **True,** se intenta la redirección del búfer de fotogramas. Para una conexión de bucle atrás (el mismo equipo es cliente y servidor), el redireccionamiento del búfer de fotogramas permite que la memoria del búfer de fotogramas se comparta entre las sesiones. |
| EnableHardwareMode | **VT \_ BOOL**  | Solo escritura | No | Si **es True,** se intenta la ayuda de hardware con la decodificación de gráficos. |
| IgnoreCursors | **VT \_ BOOL** | Solo escritura | No | Si **es True,** se omiten los cursores enviados por el servidor remoto. |
| ManualClipboardSyncEnabled | **VT \_ BOOL** | Lectura/Escritura | Sí | Establecer esta propiedad en **True significa** que los portapapeles locales y remotos no se mantendrán sincronizados automáticamente. En su lugar, la interfaz [**IMsRdpClipboard**](imsrdpclipboard.md) debe usarse para sincronizar los formatos del Portapapeles local con el Portapapeles remoto y el Portapapeles remoto con el Portapapeles local. |
| ZoomLevel | ***VT \_ UI4** | Lectura/Escritura | Sí | Implementa la característica Zoom mediante el control de ActiveX RDP. La característica Zoom está disponible en el **menú Sistema** de RDP. La **propiedad ZoomLevel** no tiene ningún efecto en el modo RemoteApp y el modo de pantalla completa. [**IMsRdpClientAdvancedSettings::SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) y **ZoomLevel** son mutuamente excluyentes. |

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

 

 





