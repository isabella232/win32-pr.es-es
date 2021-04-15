---
title: Interfaz IMsRdpClientAdvancedSettings7
description: Expone métodos y propiedades que administran la configuración avanzada del control ActiveX.
ms.assetid: 2d6848b4-2ce6-4624-b46e-65e7daf2d0f1
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed28c5d26ecf280507ce3cce835a6d0a71fc3bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676641"
---
# <a name="imsrdpclientadvancedsettings7-interface"></a>Interfaz IMsRdpClientAdvancedSettings7

Expone métodos y propiedades que administran la configuración avanzada del control ActiveX.

Para obtener una instancia de esta interfaz, use la propiedad [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obtener un puntero de interfaz [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) . A continuación, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero **IMsTscAdvancedSettings** y pase **IID \_ IMsRdpClientAdvancedSettings7** a **QueryInterface**.

## <a name="members"></a>Miembros

La interfaz **IMsRdpClientAdvancedSettings7** hereda de **IMsRdpClientAdvancedSettings6**. **IMsRdpClientAdvancedSettings7** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IMsRdpClientAdvancedSettings7** tiene estas propiedades.



| Propiedad                                                                                                    | Tipo de acceso           | Descripción                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AudioCaptureRedirectionMode**](imsrdpclientadvancedsettings7-audiocaptureredirectionmode.md)<br/> | Lectura/escritura<br/> | Especifica o recupera un valor que indica si el dispositivo de entrada de audio predeterminado se redirige desde el cliente a la sesión remota.<br/> |
| [**AudioQualityMode**](imsrdpclientadvancedsettings7-audioqualitymode.md)<br/>                       | Lectura/escritura<br/> | Especifica o recupera un valor que indica la configuración del modo de calidad de audio para el audio redirigido.<br/>                                        |
| [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md)<br/>                           | Lectura/escritura<br/> | Especifica o recupera un valor que indica si SuperPan está habilitado o deshabilitado.<br/>                                                    |
| [**NetworkConnectionType**](imsrdpclientadvancedsettings7-networkconnectiontype.md)<br/>             | Lectura/escritura<br/> | Especifica o recupera un valor que indica el tipo de conexión de red.<br/>                                                                |
| [**RedirectDirectX**](imsrdpclientadvancedsettings7-redirectdirectx.md)<br/>                         | Lectura/escritura<br/> | No se usa esta propiedad.<br/>                                                                                                                |
| [**SuperPanAccelerationFactor**](imsrdpclientadvancedsettings7-superpanaccelerationfactor.md)<br/>   | Lectura/escritura<br/> | Especifica o recupera un valor que indica el factor de aceleración de SuperPan.<br/>                                                           |
| [**VideoPlaybackMode**](imsrdpclientadvancedsettings7-videoplaybackmode.md)<br/>                     | Lectura/escritura<br/> | Especifica o recupera un valor que indica el modo de reproducción de vídeo.<br/>                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 se define como 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

