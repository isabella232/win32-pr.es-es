---
title: Interfaz INapComponentConfig (NapCommon. h)
description: Proporciona métodos de configuración del sistema NAP para los validadores de mantenimiento del sistema (SHV).
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- Interfaz INapComponentConfig NAP
- Interfaz INapComponentConfig NAP, descripción
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
ms.openlocfilehash: 63a13ae74ba1de79803ff4a2d3716eec7fe934a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422179"
---
# <a name="inapcomponentconfig-interface"></a>Interfaz INapComponentConfig

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La interfaz **INapComponentConfig** proporciona métodos de configuración del sistema NAP para los validadores de mantenimiento del sistema (SHV).

> [!Note]  
> [**INapComponentConfig2**](inapcomponentconfig2.md) y [**INapComponentConfig3**](inapcomponentconfig3.md) heredan todos los métodos de esta interfaz y deben usarse en su lugar.

 

## <a name="members"></a>Miembros

La interfaz **INapComponentConfig** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapComponentConfig** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **INapComponentConfig** tiene estos métodos.



| Método                                                                          | Descripción                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**INapComponentConfig:: GetConfig**](inapcomponentconfig-getconfig.md)         | Recupera la configuración del componente SHV.<br/>                                |
| [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)           | Inicia la interfaz de usuario personalizada para un componente de SHV.<br/>              |
| [**INapComponentConfig::IsUISupported**](inapcomponentconfig-isuisupported.md) | Especifica si el componente de SHV admite una interfaz de usuario personalizada.<br/> |
| [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md)         | Establece la configuración del componente SHV.<br/>                                     |



 

## <a name="remarks"></a>Observaciones

Esta interfaz no debe ser implementada por los agentes de mantenimiento del sistema (SHA) o los clientes de aplicación de cuarentena (QECs).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

