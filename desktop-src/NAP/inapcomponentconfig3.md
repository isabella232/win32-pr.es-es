---
title: Interfaz INapComponentConfig3 (NapCommon.h)
description: Proporciona métodos de configuración del sistema NAP para validadores de estado del sistema (SHV) para establecer y modificar los datos de configuración de un identificador de configuración específico.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- NAP de interfaz INapComponentConfig3
- Nap de interfaz INapComponentConfig3 , descrito
topic_type:
- apiref
api_name:
- INapComponentConfig3
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea8ab7b42589fa548439b03c04ade56db498750ccd47841b806dcb6b506d3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803085"
---
# <a name="inapcomponentconfig3-interface"></a>Interfaz INapComponentConfig3

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **interfaz INapComponentConfig3** proporciona métodos de configuración del sistema NAP para que los validadores de estado del sistema (SHV) establezcan y modifiquen los datos de configuración de un identificador de configuración específico.

> [!Note]  
> Esta interfaz hereda todos los métodos de [**INapComponentConfig2**](inapcomponentconfig2.md) y se debe usar en su lugar.

 

## <a name="members"></a>Miembros

La **interfaz INapComponentConfig3** hereda de [**INapComponentConfig2.**](inapcomponentconfig2.md) **INapComponentConfig3** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz INapComponentConfig3** tiene estos métodos.



| Método                                                                                | Descripción                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig3::D eleteAllConfig**](inapcomponentconfig3-deleteallconfig.md) | Implementado por SHV para proporcionar una manera de restablecer el almacén de SHV a su estado original después de la instalación.<br/>      |
| [**INapComponentConfig3::D eleteConfig**](inapcomponentconfig3-deleteconfig.md)       | Implementado por SHV para proporcionar una manera de eliminar los datos de configuración de un identificador de configuración específico.<br/>  |
| [**INapComponentConfig3::GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md) | Implementado por SHV para proporcionar una manera de obtener datos de configuración para un identificador de configuración específico.<br/>  |
| [**INapComponentConfig3::NewConfig**](inapcomponentconfig3-newconfig.md)             | Implementado por SHV para proporcionar una manera de crear datos de configuración para un identificador de configuración específico.<br/>  |
| [**INapComponentConfig3::SetConfigToID**](inapcomponentconfig3-setconfigtoid.md)     | Implementado por SHV para proporcionar una manera de establecer los datos de configuración de un identificador de configuración específico.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta interfaz no debe implementarse por agentes de mantenimiento del sistema (SHA) ni clientes de cumplimiento de cuarentena (QFC).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                  |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

 





