---
title: Interfaz INapComponentConfig (NapCommon.h)
description: Proporciona métodos de configuración del sistema NAP para validadores de estado del sistema (SHV).
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- NAP de la interfaz INapComponentConfig
- Interfaz NAP de INapComponentConfig, descrita
topic_type:
- apiref
api_name:
- INapComponentConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a1c61b3681178089b0cda813155f3629caa233a7995d28cee22b1f65754ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800027"
---
# <a name="inapcomponentconfig-interface"></a>Interfaz INapComponentConfig

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **interfaz INapComponentConfig proporciona métodos** de configuración del sistema NAP para validadores de estado del sistema (SHV).

> [!Note]  
> [**INapComponentConfig2**](inapcomponentconfig2.md) e [**INapComponentConfig3**](inapcomponentconfig3.md) heredan todos los métodos de esta interfaz y se deben usar en su lugar.

 

## <a name="members"></a>Miembros

La **interfaz INapComponentConfig** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapComponentConfig** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapComponentConfig** tiene estos métodos.



| Método                                                                          | Descripción                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**INapComponentConfig::GetConfig**](inapcomponentconfig-getconfig.md)         | Recupera la configuración del componente SHV.<br/>                                |
| [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)           | Inicia la interfaz de usuario personalizada para un componente SHV.<br/>              |
| [**INapComponentConfig::IsUISupported**](inapcomponentconfig-isuisupported.md) | Especifica si el componente SHV admite una interfaz de usuario personalizada.<br/> |
| [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md)         | Establece la configuración del componente SHV.<br/>                                     |



 

## <a name="remarks"></a>Comentarios

Los agentes de mantenimiento del sistema (SHA) o los clientes de cumplimiento de cuarentena (QEC) no deben implementar esta interfaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

