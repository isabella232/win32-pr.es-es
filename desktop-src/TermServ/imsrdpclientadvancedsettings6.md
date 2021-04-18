---
title: Interfaz IMsRdpClientAdvancedSettings6
description: Expone propiedades que administran la configuración avanzada de controles ActiveX.
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, descrito
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
ms.openlocfilehash: 8e61d3358f1af228dcd1b5a7431ee759b486df7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686033"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a>Interfaz IMsRdpClientAdvancedSettings6

Expone propiedades que administran la configuración avanzada de controles ActiveX. La interfaz **IMsRdpClientAdvancedSettings6** se deriva de la interfaz [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .

Para obtener una instancia de esta interfaz, use la propiedad [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obtener un puntero de interfaz [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) . A continuación, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero **IMsTscAdvancedSettings** y pase **IID \_ IMsRdpClientAdvancedSettings6** a **QueryInterface**.

## <a name="members"></a>Miembros

La interfaz **IMsRdpClientAdvancedSettings6** hereda de [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md). **IMsRdpClientAdvancedSettings6** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IMsRdpClientAdvancedSettings6** tiene estas propiedades.



| Propiedad                                                                                                  | Tipo de acceso           | Descripción                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticationServiceClass**](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | Lectura/escritura<br/> | Especifica el nombre de entidad de seguridad de servicio (SPN) que se va a usar para la autenticación en el servidor.<br/>                                     |
| [**AuthenticationType**](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | Solo lectura<br/>  | Especifica el tipo de autenticación utilizado para esta conexión.<br/>                                                          |
| [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | Lectura/escritura<br/> | Recupera o especifica si el control ActiveX debe intentar conectarse al servidor con fines administrativos.<br/> |
| [**EnableCredSspSupport**](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | Lectura/escritura<br/> | Especifica si el proveedor de servicios de seguridad de credenciales (CredSSP) está habilitado para esta conexión.<br/>                    |
| [**HotKeyFocusReleaseLeft**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | Lectura/escritura<br/> | Especifica el código de tecla virtual que se va a agregar a CTRL + ALT para determinar el reemplazo de la tecla de cambio de teclas para CTRL + ALT + Flecha izquierda.<br/>          |
| [**HotKeyFocusReleaseRight**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | Lectura/escritura<br/> | Especifica el código de tecla virtual que se va a agregar a CTRL + ALT para determinar el reemplazo de la tecla de cambio de teclas para CTRL + ALT + Flecha derecha.<br/>         |
| [**IMPRESO**](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | Lectura/escritura<br/> | Especifica la configuración del BLOB de preconexión (PCB) que se va a usar antes de la conexión para la transmisión al servidor.<br/>               |
| [**RelativeMouseMode**](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | Lectura/escritura<br/> | Especifica si el mouse debe usar el modo relativo.<br/>                                                                   |



 

## <a name="remarks"></a>Observaciones

La interfaz [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) ha extendido esta interfaz, heredando todos los métodos y propiedades de las interfaces anteriores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 se define como 222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Vea también

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

 

