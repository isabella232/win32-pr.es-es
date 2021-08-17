---
title: IMsRdpClientAdvancedSettings3 (interfaz)
description: Administra la configuración avanzada del cliente. Deriva de la interfaz IMsRdpClientAdvancedSettings2.
ms.assetid: bfa9cf74-5943-45ca-9259-3ef0cc9ab2ab
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClientAdvancedSettings3 Servicios de Escritorio remoto
- Interfaz IMsRdpClientAdvancedSettings3 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df13ccfb0d955714984af82daaf693522ee7d61af9c608107c53dc9f5464b591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001383"
---
# <a name="imsrdpclientadvancedsettings3-interface"></a>IMsRdpClientAdvancedSettings3 (interfaz)

Administra la configuración avanzada del cliente. Deriva de la [**interfaz IMsRdpClientAdvancedSettings2.**](imsrdpclientadvancedsettings2.md) Esta interfaz incluye métodos para recuperar y establecer propiedades avanzadas (opcionales) para el control Escritorio remoto ActiveX control.

Para obtener una instancia de esta interfaz, use la propiedad [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) para obtener un puntero de interfaz [**IMsTscAdvancedSettings.**](imstscadvancedsettings-interface.md) A continuación, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero **IMsTscAdvancedSettings** y pase **\_ IMSRdpClientAdvancedSettings3** a **QueryInterface**.

## <a name="members"></a>Miembros

La **interfaz IMsRdpClientAdvancedSettings3** hereda de [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md). **IMsRdpClientAdvancedSettings3** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClientAdvancedSettings3** tiene estas propiedades.



| Propiedad                                                                                                            | Tipo de acceso           | Descripción                                                                            |
|:--------------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------|
| [**ConnectionBarShowMinimizeButton**](imsrdpclientadvancedsettings3-connectionbarshowminimizebutton.md)<br/> | Lectura/escritura<br/> | Especifica si se debe mostrar el **botón Minimizar** en la barra de conexión.<br/> |
| [**ConnectionBarShowRestoreButton**](imsrdpclientadvancedsettings3-connectionbarshowrestorebutton.md)<br/>   | Lectura/escritura<br/> | Especifica si se debe mostrar el botón **Restaurar** en la barra de conexión.<br/>  |



 

## <a name="remarks"></a>Comentarios

Esta interfaz se ha ampliado mediante las interfaces siguientes, donde cada nueva interfaz hereda todos los métodos y propiedades de las interfaces anteriores:

-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
-   [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings3 se define como 19cd856b-c542-4c53-acee-f127e3be1a59<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

