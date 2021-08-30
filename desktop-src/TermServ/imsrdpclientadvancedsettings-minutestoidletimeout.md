---
title: IMsRdpClientAdvancedSettings MinutesToIdleTimeout, propiedad
description: Especifica el tiempo máximo, en minutos, que el cliente debe permanecer conectado sin la entrada del usuario. Si transcurre el tiempo especificado, el control llama al método IMsTscAxEvents OnIdleTimeoutNotification.
ms.assetid: 709238ea-45f8-4bdc-9bbe-019d54ca27bf
ms.tgt_platform: multiple
keywords:
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings
- Interfaz IMsRdpClientAdvancedSettings Servicios de Escritorio remoto propiedad , MinutesToIdleTimeout
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings2
- Interfaz IMsRdpClientAdvancedSettings2 Servicios de Escritorio remoto , propiedad MinutesToIdleTimeout
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings3
- Interfaz IMsRdpClientAdvancedSettings3 Servicios de Escritorio remoto , propiedad MinutesToIdleTimeout
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings4
- Interfaz IMsRdpClientAdvancedSettings4 Servicios de Escritorio remoto , propiedad MinutesToIdleTimeout
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings5
- Interfaz IMsRdpClientAdvancedSettings5 Servicios de Escritorio remoto , propiedad MinutesToIdleTimeout
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings6
- Interfaz IMsRdpClientAdvancedSettings6 Servicios de Escritorio remoto , propiedad MinutesToIdleTimeout
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto , propiedad MinutesToIdleTimeout
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto , propiedad MinutesToIdleTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.put_MinutesToIdleTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3d39d4f69931194683c928c6dfd7dc7809c22f5f8b4d2d82395acc8aa9ddfe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870915"
---
# <a name="imsrdpclientadvancedsettingsminutestoidletimeout-property"></a>IMsRdpClientAdvancedSettings::MinutesToIdleTimeout, propiedad

Especifica el tiempo máximo, en minutos, que el cliente debe permanecer conectado sin la entrada del usuario. Si transcurre el tiempo especificado, el control llama al método [**IMsTscAxEvents::OnIdleTimeoutNotification.**](imstscaxevents-onidletimeoutnotification.md)

Puede usar esta propiedad en una situación en la que necesite desconectar una sesión inactiva. por ejemplo, en un entorno de quiosco.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_MinutesToIdleTimeout(
  [in]  LONG minutesToIdleTimeout
);

HRESULT get_MinutesToIdleTimeout(
  [out] LONG *pminutesToIdleTimeout
);
```



## <a name="property-value"></a>Valor de propiedad

La nueva hora, en minutos. El valor predeterminado es cero, lo que deshabilita la característica. El valor máximo es 240, que representa 4 horas.

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

 

 





