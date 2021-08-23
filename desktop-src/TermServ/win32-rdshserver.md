---
title: Win32_RDSHServer clase
description: Administra un servidor Escritorio remoto de sesión local (RDSH).
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Win32_RDSHServer clase Servicios de Escritorio remoto
- Win32_RDSHServer clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_RDSHServer
- Win32_RDSHServer.Name
- Win32_RDSHServer.ConnectionBroker
- Win32_RDSHServer.CollectionAlias
- Win32_RDSHServer.ServerState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066cea4044330ab79122e9346f6f32999202f854245e5508448e40aea3521fe0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422605"
---
# <a name="win32_rdshserver-class"></a>Clase RDSHServer de Win32 \_

Administra un servidor Escritorio remoto de sesión local (RDSH).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHServer
{
  string Name;
  string ConnectionBroker;
  string CollectionAlias;
  uint32 ServerState;
};
```

## <a name="members"></a>Miembros

La **clase \_ RDSHServer de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ RDSHServer de Win32** tiene estos métodos.



| Método                                                                          | Descripción                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetInt32Property**](getint32property-win32-rdshserver.md)                   | Recupera un valor de propiedad entero de un **objeto \_ RDSHServer de Win32.**<br/>                                                                                                 |
| [**GetPendingStartServerList**](win32-rdshserver-getpendingstartserverlist.md) | Recupera una lista de servidores en espera de inicio.<br/>                                                                                                                           |
| [**GetStringProperty**](getstringproperty-win32-rdshserver.md)                 | Recupera un valor de propiedad de cadena de **un objeto \_ RDSHServer de Win32.**<br/>                                                                                                   |
| [**SetInt32Property**](setint32property-win32-rdshserver.md)                   | Actualiza un valor de propiedad entero de **un objeto \_ RDSHServer de Win32.**<br/>                                                                                                   |
| [**SetStringProperty**](setstringproperty-win32-rdshserver.md)                 | Actualiza un valor de propiedad de cadena de **un objeto \_ RDSHServer de Win32.**<br/>                                                                                                     |
| [**TestAndSetState**](win32-rdshserver-testandsetstate.md)                     | Compara el estado actual con el comparador especificado; si los dos coinciden, el estado se establece en un nuevo valor. Independientemente de la coincidencia, también se devuelve el estado actual.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ RDSHServer de Win32** tiene estas propiedades.

<dl> <dt>

**CollectionAlias**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtiene y establece el alias en la colección RDSH a la que está asignado el servidor RDSH.

</dd> <dt>

**ConnectionBroker**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece el nombre de Conexión a Escritorio remoto Broker (RDCB) que administra el acceso de usuario al servidor RDSH.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene y establece el nombre del servidor RDSH.

</dd> <dt>

**ServerState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Describe el estado del servidor. Cualquier valor distinto de **TARGET \_ RUNNING** (3) está reservado y debe considerarse un estado no válido.

Los valores posibles son.

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

**TARGET \_ UNKNOWN** (1)


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

**TARGET \_ RUNNING** (3)


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

**TARGET \_ INVALID** (8)


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

**TARGET \_ STARTING** (9)


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

**TARGET \_ STOPPING** (10)


</dt> <dd></dd> </dl>

**Windows Server 2012 R2 y Windows Server 2012:** Esta propiedad no está disponible antes de Windows Server 2016.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ cimv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Escritorio remoto management Services Provider](rdms-api-reference.md)
</dt> </dl>

 

