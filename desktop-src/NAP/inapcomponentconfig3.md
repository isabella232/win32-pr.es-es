---
title: Interfaz INapComponentConfig3 (NapCommon. h)
description: Proporciona métodos de configuración del sistema NAP para que los validadores de mantenimiento del sistema (SHV) establezcan y modifiquen los datos de configuración de un identificador de configuración específico.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- Interfaz INapComponentConfig3 NAP
- Interfaz INapComponentConfig3 NAP, descripción
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
ms.openlocfilehash: ac0cfead891da106a1a950ba83b9108b5950a738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676582"
---
# <a name="inapcomponentconfig3-interface"></a>Interfaz INapComponentConfig3

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La interfaz **INapComponentConfig3** proporciona métodos de configuración del sistema de NAP para que los validadores de mantenimiento del sistema (SHV) establezcan y modifiquen los datos de configuración de un identificador de configuración específico.

> [!Note]  
> Esta interfaz hereda todos los métodos de [**INapComponentConfig2**](inapcomponentconfig2.md) y se debe usar en su lugar.

 

## <a name="members"></a>Miembros

La interfaz **INapComponentConfig3** hereda de [**INapComponentConfig2**](inapcomponentconfig2.md). **INapComponentConfig3** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **INapComponentConfig3** tiene estos métodos.



| Método                                                                                | Descripción                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig3::D eleteAllConfig**](inapcomponentconfig3-deleteallconfig.md) | Implementado por SHV para proporcionar una manera de restablecer el almacén de SHV a su estado original después de la instalación.<br/>      |
| [**INapComponentConfig3::D eleteConfig**](inapcomponentconfig3-deleteconfig.md)       | Implementado por SHV para proporcionar una manera de eliminar los datos de configuración de un identificador de configuración específico.<br/>  |
| [**INapComponentConfig3::GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md) | Implementado por SHV para proporcionar una manera de obtener datos de configuración para un identificador de configuración específico.<br/>  |
| [**INapComponentConfig3:: documento newconfig**](inapcomponentconfig3-newconfig.md)             | Implementado por SHV para proporcionar una manera de crear datos de configuración para un identificador de configuración específico.<br/>  |
| [**INapComponentConfig3::SetConfigToID**](inapcomponentconfig3-setconfigtoid.md)     | Implementado por SHV para proporcionar una manera de establecer los datos de configuración para un identificador de configuración específico.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta interfaz no debe ser implementada por los agentes de mantenimiento del sistema (SHA) o los clientes de aplicación de cuarentena (QECs).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referencia de NAP](nap-reference.md)
</dt> </dl>

 

 





