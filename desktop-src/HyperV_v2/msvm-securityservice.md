---
description: Representa el servicio de seguridad. Se usa para configurar las opciones de seguridad del sistema virtual.
ms.assetid: 00097d81-9fea-4b84-b5dd-e45af46d6e0a
title: Msvm_SecurityService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc7b15af3d3033487464fe7b29a93dc649ffbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002091"
---
# <a name="msvm_securityservice-class"></a>MSVM \_ SecurityService (clase)

Representa el servicio de seguridad. Se usa para configurar las opciones de seguridad del sistema virtual.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityService : CIM_Service
{
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ SecurityService** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **MSVM \_ SecurityService** tiene estos métodos.



| Método                                                                                            | Descripción                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**GetKeyProtector**](msvm-securityservice-getkeyprotector.md)                                   | Método para recuperar el protector de clave de un sistema virtual.<br/>   |
| [**ModifySecuritySettings**](msvm-securityservice-modifysecuritysettings.md)                     | Modifica la configuración de seguridad actual de una máquina virtual.<br/> |
| [**RestoreLastKnownGoodKeyProtector**](msvm-securityservice-restorelastknowngoodkeyprotector.md) | Método que se va a restaurar al último protector de clave válido conocido.<br/> |
| [**SetKeyProtector**](msvm-securityservice-setkeyprotector.md)                                   | Método para establecer el protector de clave de un sistema virtual.<br/>        |
| [**SetSecurityPolicy**](msvm-securityservice-setsecuritypolicy.md)                               | Método para establecer el protector de clave de un sistema virtual.<br/>        |
| [**StartService**](msvm-securityservice-startservice.md)                                         | inicia el servicio.<br/>                                          |
| [**StopService**](msvm-securityservice-stopservice.md)                                           | detiene el servicio.<br/>                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Servicio CIM**](cim-service.md)
</dt> </dl>

 

 




