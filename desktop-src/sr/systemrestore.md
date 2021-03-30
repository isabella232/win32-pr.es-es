---
title: Clase SystemRestore
description: Proporciona métodos para deshabilitar y habilitar la supervisión, enumerar los puntos de restauración disponibles e iniciar una restauración en el sistema local.
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- Restauración del sistema de la clase SystemRestore
- SystemRestore (clase) restauración del sistema, descrito
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
ms.openlocfilehash: 64d2b609a7a49a9b319c15745600aa54193350e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079495"
---
# <a name="systemrestore-class"></a>Clase SystemRestore

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

La clase **SystemRestore** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **SystemRestore** tiene estos métodos.



| Método                                                             | Descripción                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [**CreateRestorePoint**](createrestorepoint-systemrestore.md)     | Crea un punto de restauración.<br/>                         |
| [**Disable**](disable-systemrestore.md)                           | Deshabilita la supervisión en una unidad determinada.<br/>       |
| [**Habilitar**](enable-systemrestore.md)                             | Habilita la supervisión en una unidad determinada.<br/>        |
| [**GetLastRestoreStatus**](getlastrestorestatus-systemrestore.md) | Recupera el estado de la última restauración del sistema.<br/> |
| [**Restaurar**](restore-systemrestore.md)                           | Inicia una restauración del sistema.<br/>                      |



 

### <a name="properties"></a>Propiedades

La clase **SystemRestore** tiene estas propiedades.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

La hora a la que se produjo el cambio de estado.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

La descripción que se va a mostrar para que el usuario pueda identificar fácilmente un punto de restauración. La longitud máxima de una cadena ANSI es MAX \_ desc. La longitud máxima de una cadena Unicode es MAX \_ DESC \_ W. Para obtener más información, vea [texto de descripción de punto de restauración](restore-point-description-text.md).

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Tipo del evento. Este miembro puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**Inicio \_ de Cambio de \_ sistema \_ anidado**</dt> <dt>102</dt> </dl> | Ha empezado un cambio en el sistema. Una llamada subsiguiente anidada no crea un nuevo punto de restauración. <br/> Las llamadas subsiguientes deben usar END \_ Nested \_ System \_ Change, no end \_ System \_ Change.<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**Inicio \_ de \_Cambio del sistema**</dt> <dt>100</dt> </dl>                       | Ha empezado un cambio en el sistema.<br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**Fin \_ de Cambio de \_ sistema \_ anidado**</dt> <dt>103</dt> </dl>       | Ha finalizado un cambio de sistema.<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**Fin \_ de \_Cambio del sistema**</dt> <dt>101</dt> </dl>                             | Ha finalizado un cambio de sistema.<br/>                                                                                                                                                           |



 

</dd> <dt>

**RestorePointType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

El tipo de punto de restauración. Este miembro puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                                          | Significado                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <dt>**Aplicación \_ de INSTALAR**</dt> <dt>0</dt> </dl>         | Se ha instalado una aplicación.<br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <dt>**Aplicación \_ de Desinstalar**</dt> <dt>1</dt> </dl>   | Se ha desinstalado una aplicación.<br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <dt>**Cancelado \_ OPERACIÓN**</dt> <dt>13</dt> </dl>        | Una aplicación debe eliminar el punto de restauración que creó. Por ejemplo, una aplicación usaría esta marca cuando un usuario cancela una instalación. <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**Dispositivo \_ de \_Instalación del controlador**</dt> <dt>10</dt> </dl> | Se ha instalado un controlador de dispositivo.<br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**Modificar \_ CONFIGURACIÓN**</dt> <dt>12</dt> </dl>                    | Una aplicación tiene características agregadas o eliminadas.<br/>                                                                                                  |



 

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Número de secuencia del punto de restauración.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede obtener una lista de puntos de restauración mediante el método [**SWbemServices. instances**](/windows/desktop/WmiSdk/swbemservices-instancesof) para recuperar una colección de objetos **SystemRestore** . Puede usar las propiedades de clase para identificar el punto de restauración.

## <a name="examples"></a>Ejemplos

En el siguiente script de ejemplo se enumeran los puntos de restauración actuales.


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



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                         |
| Espacio de nombres<br/>                | Raíz \\ predeterminada<br/>                                                          |
| MOF<br/>                      | <dl> <dt>MOF</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Instrumental de administración de Windows](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

