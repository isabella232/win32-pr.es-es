---
title: Interfaz IMsRdpClientNonScriptable7
description: Proporciona acceso a las propiedades noscriptables de la sesión remota de un cliente en el control Escritorio remoto ActiveX cliente. Deriva de la interfaz IMsRdpClientNonScriptable6.
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClientNonScriptable7 Servicios de Escritorio remoto
- Interfaz IMsRdpClientNonScriptable7 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 01065ef73d1a23f0ac9416a39c4af74042c883e3b4d7f596cb95f6c01043f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117941112"
---
# <a name="imsrdpclientnonscriptable7-interface"></a>Interfaz IMsRdpClientNonScriptable7

Proporciona acceso a las propiedades noscriptables de la sesión remota de un cliente en el control Escritorio remoto ActiveX cliente. Deriva de la [**interfaz IMsRdpClientNonScriptable6.**](imsrdpclientnonscriptable6.md) Solo se puede acceder a los métodos de esta interfaz a través de la tabla virtual; no están disponibles para su uso en clientes que pueden incluir scripts.

Una instancia de esta interfaz se obtiene llamando a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el objeto [**IMsTscAx**](imstscax-interface.md) y pasando **IID \_ IMsRdpClientNonScriptable7**.

## <a name="members"></a>Miembros

La **interfaz IMsRdpClientNonScriptable7** hereda de [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md). **IMsRdpClientNonScriptable7** también tiene estos tipos de miembros:

- [Métodos](#methods)
- [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IMsRdpClientNonScriptable7** tiene estos métodos.


| Método            | Descripción              |
|:------------------|:-------------------------|
| [**DisableDpiCursorScalingForProcess**](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  Deshabilita el escalado local del cursor del mouse recibido del servidor, lo que garantiza que la forma del cursor se represente correctamente sin modificaciones.                   |

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClientNonScriptable7** tiene estas propiedades.

| Propiedad         | Tipo de acceso           | Descripción            |
|:-----------------|:----------------------|:-----------------------|
| [**CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | Solo lectura |  Obtiene la colección de cámaras (y las configuraciones asociadas) que están disponibles para el redireccionamiento.   |
| [**Portapapeles**](imsrdpclientnonscriptable7-clipboard.md)                       | Solo lectura |    Obtiene el controlador del Portapapeles que se usa para sincronizar los Portapapeles locales y remotos si está habilitada la sincronización manual del Portapapeles.    |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1803 (compilación 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| CLSID                    | CLSID \_ MsRdpClient12 se define como 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8<br/> CLSID \_ MsRdpClient12NotSafeForScripting se define como 3BB805C2-D9E2-4174-8A1E-C87D69563662<br/> CLSID \_ MsRdpClient11 se define como 22A7E88C-5BF5-4DE6-B687-60F7331DF190<br/> CLSID \_ MsRdpClient11NotSafeForScripting se define como 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8<br/>  |
| IID                      | IID \_ IMsRdpClientNonScriptable7 se define como 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC            |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>
