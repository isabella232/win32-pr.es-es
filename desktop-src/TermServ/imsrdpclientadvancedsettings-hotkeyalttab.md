---
title: Propiedad HotKeyAltTab de IMsRdpClientAdvancedSettings
description: Especifica el código de tecla virtual que se va a agregar a ALT para determinar el reemplazo de la tecla de cambio de teclas ALT + TAB.
ms.assetid: d7066fb4-f53f-4e55-ba12-fb4078ece144
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad HotKeyAltTab
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.HotKeyAltTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.HotKeyAltTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.HotKeyAltTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.HotKeyAltTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.HotKeyAltTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.HotKeyAltTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.HotKeyAltTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec7834a95b83ec43553d0ced1e056860cfb5abe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422140"
---
# <a name="imsrdpclientadvancedsettingshotkeyalttab-property"></a>IMsRdpClientAdvancedSettings:: HotKeyAltTab (propiedad)

Especifica el código de tecla virtual que se va a agregar a ALT para determinar el reemplazo de la tecla de cambio de teclas ALT + TAB.

Esta propiedad solo es válida cuando la propiedad [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) no está habilitada.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_HotKeyAltTab(
  [in]  LONG hotKeyAltTab
);

HRESULT get_HotKeyAltTab(
  [out] LONG *photKeyAltTab
);
```



## <a name="property-value"></a>Valor de propiedad

El nuevo código de tecla virtual. **VK \_ ANTES** es el valor predeterminado, con Alt + Re Pág como la secuencia resultante.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="remarks"></a>Observaciones

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                        |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                  |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





