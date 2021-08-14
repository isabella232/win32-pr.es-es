---
title: SystemRestore (clase)
description: Proporciona métodos para deshabilitar y habilitar la supervisión, enumerar los puntos de restauración disponibles e iniciar una restauración en el sistema local.
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- SystemRestore class Restaurar sistema
- Clase SystemRestore Restaurar sistema , descrito
topic_type:
- apiref
api_name:
- SystemRestore
- SystemRestore.Description
- SystemRestore.RestorePointType
- SystemRestore.EventType
- SystemRestore.SequenceNumber
- SystemRestore.CreationTime
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca781f960f51c8f7804d56f3b2f5531517c3f16505f40dd48d442857fa58bf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967994"
---
# <a name="systemrestore-class"></a>SystemRestore (clase)

Proporciona métodos para deshabilitar y habilitar la supervisión, enumerar los puntos de restauración disponibles e iniciar una restauración en el sistema local.

## <a name="syntax"></a>Sintaxis

``` syntax
class SystemRestore
{
  String Description;
  uint32 RestorePointType;
  uint32 EventType;
  uint32 SequenceNumber;
  String CreationTime;
};
```

## <a name="members"></a>Miembros

La **clase SystemRestore** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase SystemRestore** tiene estos métodos.



| Método                                                             | Descripción                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [**CreateRestorePoint**](createrestorepoint-systemrestore.md)     | Crea un punto de restauración.<br/>                         |
| [**Deshabilitar**](disable-systemrestore.md)                           | Deshabilita la supervisión en una unidad determinada.<br/>       |
| [**Habilitar**](enable-systemrestore.md)                             | Habilita la supervisión en una unidad determinada.<br/>        |
| [**GetLastRestoreStatus**](getlastrestorestatus-systemrestore.md) | Recupera el estado de la última restauración del sistema.<br/> |
| [**Restauración**](restore-systemrestore.md)                           | Inicia una restauración del sistema.<br/>                      |



 

### <a name="properties"></a>Propiedades

La **clase SystemRestore** tiene estas propiedades.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Hora a la que se produjo el cambio de estado.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Descripción que se va a mostrar para que el usuario pueda identificar fácilmente un punto de restauración. La longitud máxima de una cadena ANSI es MAX \_ DESC. La longitud máxima de una cadena Unicode es MAX \_ DESC \_ W. Para obtener más información, vea [Texto de descripción del punto de restauración.](restore-point-description-text.md)

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Tipo del evento. Este miembro puede ser uno de los siguientes valores.



| Valor                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**BEGIN \_ CAMBIO \_ DEL \_ SISTEMA ANIDADO**</dt> <dt>102</dt> </dl> | Se ha iniciado un cambio en el sistema. Una llamada anidada posterior no crea un nuevo punto de restauración. <br/> Las llamadas posteriores deben usar END \_ NESTED \_ SYSTEM \_ CHANGE, no END SYSTEM \_ \_ CHANGE.<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**BEGIN \_ CAMBIO \_ DEL**</dt> <dt>SISTEMA 100</dt> </dl>                       | Se ha iniciado un cambio en el sistema.<br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**END \_ CAMBIO \_ DEL \_ SISTEMA ANIDADO**</dt> <dt>103</dt> </dl>       | Ha finalizado un cambio del sistema.<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**END \_ CAMBIO \_ DEL**</dt> <dt>SISTEMA 101</dt> </dl>                             | Ha finalizado un cambio del sistema.<br/>                                                                                                                                                           |



 

</dd> <dt>

**RestorePointType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Tipo de punto de restauración. Este miembro puede ser uno de los siguientes valores.



| Valor                                                                                                                                                                                                                                          | Significado                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <dt>**APLICACIÓN \_ INSTALL**</dt> <dt>0</dt> </dl>         | Se ha instalado una aplicación.<br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <dt>**APLICACIÓN \_ UNINSTALL**</dt> <dt>1</dt> </dl>   | Se ha desinstalado una aplicación.<br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <dt>**CANCELLED \_ OPERACIÓN**</dt> <dt>13</dt> </dl>        | Una aplicación debe eliminar el punto de restauración que creó. Por ejemplo, una aplicación usaría esta marca cuando un usuario cancela una instalación. <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**DISPOSITIVO \_ INSTALACIÓN \_ DEL CONTROLADOR**</dt> <dt>10</dt> </dl> | Se ha instalado un controlador de dispositivo.<br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**MODIFY \_ CONFIGURACIÓN**</dt> <dt>12</dt> </dl>                    | Una aplicación ha tenido características agregadas o eliminadas.<br/>                                                                                                  |



 

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Número de secuencia del punto de restauración.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Puede obtener una lista de puntos de restauración mediante el método [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) para recuperar una colección de **objetos SystemRestore.** Puede usar las propiedades de clase para identificar el punto de restauración.

## <a name="examples"></a>Ejemplos

El siguiente script de ejemplo enumera los puntos de restauración actuales.


```VB
'SystemRestore Class
'Provides methods for disabling and enabling monitoring, 
'listing available restore points, and initiating a 
'restore on the local system.

Set RPSet = GetObject("winmgmts:root/default").InstancesOf ("SystemRestore")
for each RP in RPSet
    wscript.Echo "Dir: RP" & RP.SequenceNumber & ", Name: " & RP.Description & ", Type: ", RP.RestorePointType & ", Time: " & RP.CreationTime
next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                         |
| Espacio de nombres<br/>                | Raíz \\ predeterminada<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Instrumental de administración de Windows](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

