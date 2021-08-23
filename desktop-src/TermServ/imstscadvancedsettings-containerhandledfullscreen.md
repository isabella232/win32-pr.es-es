---
title: Propiedad IMsTscAdvancedSettings ContainerHandledFullScreen
description: Especifica si el modo de pantalla completa con control de contenedor está habilitado.
ms.assetid: 67679323-4a74-4d91-abd0-607415295f3d
ms.tgt_platform: multiple
keywords:
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto , interfaz IMsTscAdvancedSettings
- Interfaz IMsTscAdvancedSettings Servicios de Escritorio remoto , propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings
- Interfaz IMsRdpClientAdvancedSettings Servicios de Escritorio remoto , propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings2
- Interfaz IMsRdpClientAdvancedSettings2 Servicios de Escritorio remoto , propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings3
- Interfaz IMsRdpClientAdvancedSettings3 Servicios de Escritorio remoto , propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings4
- Interfaz IMsRdpClientAdvancedSettings4 Servicios de Escritorio remoto , propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings5
- Interfaz IMsRdpClientAdvancedSettings5 Servicios de Escritorio remoto , propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings6
- Interfaz IMsRdpClientAdvancedSettings6 Servicios de Escritorio remoto , propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto , propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto , propiedad ContainerHandledFullScreen
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.ContainerHandledFullScreen
- IMsTscAdvancedSettings.get_ContainerHandledFullScreen
- IMsTscAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.put_ContainerHandledFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 975581aaca4aad2511396e8ec426a7bf2a4720ff54202d42fbe932c0c2e9464d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513125"
---
# <a name="imstscadvancedsettingscontainerhandledfullscreen-property"></a>Propiedad IMsTscAdvancedSettings::ContainerHandledFullScreen

Especifica si el modo de pantalla completa con control de contenedor está habilitado.

> [!Note]  
> El valor de la propiedad **ContainerHandledFullScreen** no tiene ningún efecto cuando el control Escritorio remoto ActiveX es seguro para el scripting y devuelve **S \_ FALSE** cuando se intenta cambiar el valor.

 

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ContainerHandledFullScreen(
  [in]  BOOL ContainerHandledFullScreen
);

HRESULT get_ContainerHandledFullScreen(
  [out] BOOL *pContainerHandledFullScreen
);
```



## <a name="property-value"></a>Valor de propiedad

Establezca este parámetro en **TRUE** para habilitar el modo u otro valor para deshabilitar el modo.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente. Devuelve **S \_ FALSE si** no se admite.

## <a name="remarks"></a>Comentarios

Cuando este modo está habilitado, el contenedor actual procesa el cambio dentro y fuera del modo de pantalla completa. Este método solo se debe usar si el contenedor actual necesita un amplio control sobre el comportamiento del modo de pantalla completa. Cuando se establece esta propiedad, el control no entra ni sale del modo de pantalla completa en respuesta a la combinación de teclas de método abreviado de modo de pantalla completa (CTRL+ALT+BREAK); En su lugar, se llama a los eventos [**IMsTscAxEvents::OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) e [**IMsTscAxEvents::OnRequestLeaveFullScreen.**](imstscaxevents-onrequestleavefullscreen.md) Consulte [**IMsTscAxEvents para**](imstscaxevents-interface.md) obtener más información sobre estos eventos.

La mayoría de las aplicaciones de contenedor no necesitarán usar el modo de pantalla completa con control de contenedor.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings se define como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
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

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





