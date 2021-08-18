---
title: Propiedad IMsRdpClientAdvancedSettings HotKeyAltSpace
description: Especifica el código de clave virtual que se agregará a ALT para determinar el reemplazo de la tecla de acceso rápido para ALT+ESPACIO.
ms.assetid: 943935e9-a6f1-496e-895c-e993755e25cc
ms.tgt_platform: multiple
keywords:
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings
- Interfaz IMsRdpClientAdvancedSettings Servicios de Escritorio remoto , propiedad HotKeyAltSpace
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings2
- Interfaz IMsRdpClientAdvancedSettings2 Servicios de Escritorio remoto , propiedad HotKeyAltSpace
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings3
- Interfaz IMsRdpClientAdvancedSettings3 Servicios de Escritorio remoto , propiedad HotKeyAltSpace
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings4
- Interfaz IMsRdpClientAdvancedSettings4 Servicios de Escritorio remoto , propiedad HotKeyAltSpace
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings5
- Interfaz IMsRdpClientAdvancedSettings5 Servicios de Escritorio remoto , propiedad HotKeyAltSpace
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings6
- Interfaz IMsRdpClientAdvancedSettings6 Servicios de Escritorio remoto , propiedad HotKeyAltSpace
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto , propiedad HotKeyAltSpace
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto , propiedad HotKeyAltSpace
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltSpace
- IMsRdpClientAdvancedSettings.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.put_HotKeyAltSpace
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46a2d97b51962911d9dd7e0df1a35215f905dc0260743a0cea03ce066c870779
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870995"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltspace-property"></a>IMsRdpClientAdvancedSettings::HotKeyAltSpace, propiedad

Especifica el código de clave virtual que se agregará a ALT para determinar el reemplazo de la tecla de acceso rápido para ALT+ESPACIO.

Esta propiedad solo es válida cuando la [**propiedad KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) no está habilitada.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HotKeyAltSpace(
  [in]  LONG hotKeyAltSpace
);

HRESULT get_HotKeyAltSpace(
  [out] LONG *photKeyAltSpace
);
```



## <a name="property-value"></a>Valor de propiedad

Nuevo código de clave virtual. **VK \_ DELETE** es el valor predeterminado, con ALT+DELETE como secuencia resultante.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 





