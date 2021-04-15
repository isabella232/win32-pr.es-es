---
title: Propiedad overallConnectionTimeout de IMsRdpClientAdvancedSettings
description: Especifica la cantidad total de tiempo, en segundos, que el control de cliente espera a que se complete una conexión.
ms.assetid: 02fb24e1-b5e4-4d8e-a1c2-a9bd62a69bed
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad overallConnectionTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.overallConnectionTimeout
- IMsRdpClientAdvancedSettings.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_overallConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de6687d3d5cbccb3f7fdab94eca5ba4f2331c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676670"
---
# <a name="imsrdpclientadvancedsettingsoverallconnectiontimeout-property"></a>IMsRdpClientAdvancedSettings:: overallConnectionTimeout (propiedad)

Especifica la cantidad total de tiempo, en segundos, que el control de cliente espera a que se complete una conexión.

Si transcurre el tiempo especificado antes de que se complete la conexión, el control se desconecta y llama al método [**IMsTscAxEvents:: OnDisconnection**](imstscaxevents-ondisconnected.md) .

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_overallConnectionTimeout(
  [in]  LONG overallConnectionTimeout
);

HRESULT get_overallConnectionTimeout(
  [out] LONG *poverallConnectionTimeout
);
```



## <a name="property-value"></a>Valor de propiedad

La nueva hora, en segundos. El valor máximo es 600, que representa 10 minutos.

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
</dt> <dt>

[**singleConnectionTimeout**](imsrdpclientadvancedsettings-singleconnectiontimeout.md)
</dt> </dl>

 

 





