---
title: Interfaz IMsRdpClientNonScriptable6
description: Proporciona acceso a las propiedades noscriptables de la sesión remota de un cliente en el control Escritorio remoto ActiveX cliente. Deriva de la interfaz IMsRdpClientNonScriptable5.
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClientNonScriptable6 Servicios de Escritorio remoto
- Interfaz IMsRdpClientNonScriptable6 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 6beede518b346ff4934730eb6fa8c3ed9f80dec980be031f9d09e774aeb359a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033225"
---
# <a name="imsrdpclientnonscriptable6-interface"></a>Interfaz IMsRdpClientNonScriptable6

Proporciona acceso a las propiedades noscriptables de la sesión remota de un cliente en el control Escritorio remoto ActiveX cliente. Deriva de la [**interfaz IMsRdpClientNonScriptable5.**](imsrdpclientnonscriptable5.md) Solo se puede acceder a los métodos de esta interfaz a través de vtable; no están disponibles para su uso en clientes que pueden incluir scripts.

Para obtener una instancia de esta interfaz, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el objeto [**IMsTscAx**](imstscax-interface.md) y pase **\_ IID IMsRdpClientNonScriptable6**.

## <a name="members"></a>Miembros

La **interfaz IMsRdpClientNonScriptable6** hereda de [**IMsRdpClientNonScriptable5.**](imsrdpclientnonscriptable5.md) **IMsRdpClientNonScriptable6** también tiene estos tipos de miembros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMsRdpClientNonScriptable6** tiene estos métodos.


| Método            | Descripción                   |
|:-----------------------------|:-----------------|
| [**SendLocation2D**](imsrdpclientnonscriptable6-sendlocation2d.md)     |  Envía un valor de latitud y longitud al servidor para que la ubicación geográfica del cliente se pueda reflejar en la sesión remota.                   |
| [**SendLocation3D**](imsrdpclientnonscriptable6-sendlocation3d.md)     | Envía un valor de latitud, longitud y altitud al servidor para que la ubicación geográfica del cliente se pueda reflejar en la sesión remota.                 |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1709 (compilación 16299)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| CLSID                    | CLSID \_ MsRdpClient12 se define como 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8<br/> CLSID \_ MsRdpClient12NotSafeForScripting se define como 3BB805C2-D9E2-4174-8A1E-C87D69563662<br/> CLSID \_ MsRdpClient11 se define como 22A7E88C-5BF5-4DE6-B687-60F7331DF190<br/> CLSID \_ MsRdpClient11NotSafeForScripting se define como 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8<br/>  |
| IID                      | IID \_ IMsRdpClientNonScriptable6 se define como 05293249-B28B-4DB8-BE64-1B2F496B910E            |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>
