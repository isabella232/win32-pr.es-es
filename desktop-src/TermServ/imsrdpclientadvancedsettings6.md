---
title: Interfaz IMsRdpClientAdvancedSettings6
description: Expone propiedades que administran la configuración avanzada ActiveX control.
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClientAdvancedSettings6 Servicios de Escritorio remoto
- Interfaz IMsRdpClientAdvancedSettings6 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf4c108345e3dae0b5c8f4e45c3a1c07299cccdaed44404718e599c0ef973957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352132"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a>Interfaz IMsRdpClientAdvancedSettings6

Expone propiedades que administran la configuración avanzada ActiveX control. La **interfaz IMsRdpClientAdvancedSettings6** se deriva de la [**interfaz IMsRdpClientAdvancedSettings5.**](imsrdpclientadvancedsettings5.md)

Para obtener una instancia de esta interfaz, use la propiedad [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) para obtener un puntero de interfaz [**IMsTscAdvancedSettings.**](imstscadvancedsettings-interface.md) A continuación, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero **IMsTscAdvancedSettings** y pase **IID \_ IMsRdpClientAdvancedSettings6** a **QueryInterface**.

## <a name="members"></a>Miembros

La **interfaz IMsRdpClientAdvancedSettings6** hereda de [**IMsRdpClientAdvancedSettings5.**](imsrdpclientadvancedsettings5.md) **IMsRdpClientAdvancedSettings6** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClientAdvancedSettings6** tiene estas propiedades.



| Propiedad                                                                                                  | Tipo de acceso           | Descripción                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticationServiceClass**](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | Lectura/escritura<br/> | Especifica el nombre de entidad de seguridad de servicio (SPN) que se usará para la autenticación en el servidor.<br/>                                     |
| [**AuthenticationType**](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | Solo lectura<br/>  | Especifica el tipo de autenticación utilizada para esta conexión.<br/>                                                          |
| [**ConnectToAdminadminserver**](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | Lectura/escritura<br/> | Recupera o especifica si el control ActiveX debe intentar conectarse al servidor con fines administrativos.<br/> |
| [**EnableCredSspSupport**](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | Lectura/escritura<br/> | Especifica si el proveedor de servicios de seguridad de credenciales (CredSSP) está habilitado para esta conexión.<br/>                    |
| [**HotKeyFocusReleaseLeft**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | Lectura/escritura<br/> | Especifica el código de clave virtual que se agregará a CTRL+ALT para determinar el reemplazo de la tecla de acceso rápido para CTRL+ALT+FLECHA IZQUIERDA.<br/>          |
| [**HotKeyFocusReleaseRight**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | Lectura/escritura<br/> | Especifica el código de clave virtual que se agregará a CTRL+ALT para determinar el reemplazo de la tecla de acceso rápido para CTRL+ALT+FLECHA DERECHA.<br/>         |
| [**Pcb**](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | Lectura/escritura<br/> | Especifica la configuración de BLOB de preconexión (PWS) que se usará antes de conectarse para la transmisión al servidor.<br/>               |
| [**RelativeMouseMode**](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | Lectura/escritura<br/> | Especifica si el mouse debe usar el modo relativo.<br/>                                                                   |



 

## <a name="remarks"></a>Comentarios

Esta interfaz se ha ampliado mediante la interfaz [**IMsRdpClientAdvancedSettings7,**](imsrdpclientadvancedsettings7.md) heredando todos los métodos y propiedades de las interfaces anteriores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 se define como 222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

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

 

