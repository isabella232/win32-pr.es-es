---
title: Win32_SessionBrokerTargetEvent clase
description: Representa un cambio en un destino de agente de sesión.
ms.assetid: ee3ae0ed-eb8b-4777-9b9e-0e50722cf52a
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerTargetEvent clase Servicios de Escritorio remoto
- Win32_SessionBrokerTargetEvent clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTargetEvent
- Win32_SessionBrokerTargetEvent.SECURITY_DESCRIPTOR
- Win32_SessionBrokerTargetEvent.TIME_CREATED
- Win32_SessionBrokerTargetEvent.ChangeType
- Win32_SessionBrokerTargetEvent.PluginName
- Win32_SessionBrokerTargetEvent.TargetName
- Win32_SessionBrokerTargetEvent.FarmName
- Win32_SessionBrokerTargetEvent.Guid
- Win32_SessionBrokerTargetEvent.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92fcd6cb93e3ac7abaa5fef33e1557008eb29b46940fae6d5165809d9252fa16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769975"
---
# <a name="win32_sessionbrokertargetevent-class"></a>Clase \_ SessionBrokerTargetEvent de Win32

Representa un cambio en un destino de agente de sesión.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class Win32_SessionBrokerTargetEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint32 ChangeType;
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a>Miembros

La **clase \_ SessionBrokerTargetEvent de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SessionBrokerTargetEvent de Win32** tiene estas propiedades.

<dl> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el cambio que se ha producido. Puede ser uno de los siguientes valores.

<dt>

1 (0x1)
</dt> <dd>

No se especifica el tipo de cambio.

</dd> <dt>

2 (0x2)
</dt> <dd>

La dirección IP externa ha cambiado.

</dd> <dt>

4 (0x4)
</dt> <dd>

La dirección IP interna ha cambiado.

</dd> <dt>

8 (0x8)
</dt> <dd>

El destino se ha unido.

</dd> <dt>

16 (0x10)
</dt> <dd>

Se quitó el destino.

</dd> <dt>

32 (0x20)
</dt> <dd>

El estado del destino ha cambiado.

</dd> <dt>

64 (0x40)
</dt> <dd>

El destino está inactivo.

</dd> </dl>

</dd> <dt>

**Entorno**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El nombre del entorno. En el caso de un destino de máquina virtual (VM), podría ser el nombre de host de la máquina virtual.

**Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2012

</dd> <dt>

**FarmName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la granja a la que pertenece el destino.

**Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2012

</dd> <dt>

**Guid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

GUID del destino.

**Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2012

</dd> <dt>

**PluginName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del complemento.

**Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2012

</dd> <dt>

**\_DESCRIPTOR DE SEGURIDAD**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event). Para obtener más información sobre las constantes usadas para establecer este descriptor de seguridad, vea [Constantes de seguridad WMI](/windows/desktop/WmiSdk/wmi-security-constants).

</dd> <dt>

**TargetName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del destino.

**Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2012

</dd> <dt>

**HORA \_ CREADA**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 nanosegundos después del 1 de enero de 1601. La información está en formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/previous-versions//aa393262(v=vs.85))

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

