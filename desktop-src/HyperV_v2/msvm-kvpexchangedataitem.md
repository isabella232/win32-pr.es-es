---
description: Representa un par clave-valor.
ms.assetid: B13E9C5F-5B13-4EE5-AE5F-F51B61BDB9B7
title: Msvm_KvpExchangeDataItem clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeDataItem
- Msvm_KvpExchangeDataItem.InstanceID
- Msvm_KvpExchangeDataItem.Caption
- Msvm_KvpExchangeDataItem.Description
- Msvm_KvpExchangeDataItem.ElementName
- Msvm_KvpExchangeDataItem.Source
- Msvm_KvpExchangeDataItem.Name
- Msvm_KvpExchangeDataItem.Data
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1bf64dd4256dba97238d73f403da6a7fb6368fa7b730a0be208d62b2d84782a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522076"
---
# <a name="msvm_kvpexchangedataitem-class"></a>Clase Msvm \_ KvpExchangeDataItem

Representa un par clave-valor.

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_KvpExchangeDataItem : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Key-Value Pair Exchange Data Item";
  string Description = "Microsoft Key-Value Pair Exchange Data Item";
  string ElementName = "Key-Value Pair Exchange Data Item";
  uint16 Source;
  string Name;
  string Data;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ KvpExchangeDataItem** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ KvpExchangeDataItem** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Datos**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Parte del valor del par clave-valor.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Parte clave del par clave-valor.



| Clave                                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>"CSDVersion"</dt> </dl>                 | Cadena que representa el Service Pack más reciente instalado en el sistema invitado. Por ejemplo, "Service Pack 2". Si no se ha instalado ningún Service Pack, esta cadena está vacía.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>"FullyQualifiedDomainName"</dt> </dl>   | Cadena que representa el nombre DNS completo que identifica de forma única el equipo local. Este nombre es una combinación del nombre de host DNS y el nombre de dominio DNS, con el formato *HostName*. *DomainName*. Si el equipo local es un nodo de un clúster, este valor es el nombre DNS completo del servidor virtual del clúster. Este valor coincide con el nombre devuelto por la función [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) cuando el parámetro *NameType* es "ComputerNameDnsFullyQualified".<br/> |
| <dl> <dt>"IntegrationServicesVersion"</dt> </dl> | Cadena que representa la versión del Integration Services instalada actualmente en la máquina virtual invitada (por ejemplo, "6.1.7000.0").<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>"NetworkAddressIPv4"</dt> </dl>         | Cadena que contiene una lista delimitada por punto y coma de las direcciones IPv4 asignadas actualmente a la máquina virtual invitada. La lista se actualiza automáticamente cada vez que se produce un cambio de configuración de TCP/IP en la máquina virtual invitada. Cada dirección se representa en notación decimal de punto. <br/>                                                                                                                                                                                                                         |
| <dl> <dt>"NetworkAddressIPv6"</dt> </dl>         | Cadena que contiene una lista delimitada por punto y coma de las direcciones IPv6 asignadas actualmente a la máquina virtual invitada. La lista se actualiza automáticamente cada vez que se produce un cambio de configuración de TCP/IP en la máquina virtual invitada. Cada dirección se representa en notación hexadecimal de dos puntos. No se garantiza que las listas IPv4 e IPv6 estén sincronizadas en todo momento.<br/>                                                                                                                                             |
| <dl> <dt>"OSBuildNumber"</dt> </dl>              | Cadena que representa el número de compilación del sistema operativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>"OSEditionId"</dt> </dl>                | Cadena que representa la edición (SKU) del sistema operativo de la máquina virtual invitada. Para obtener una lista de los valores posibles, vea [**la función GetProductInfo.**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo)<br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>"OSName"</dt> </dl>                     | Cadena que representa el nombre del sistema operativo. Este valor procede de la siguiente entrada del Registro: **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProductName**<br/> <br/>                                                                                                                                                                                                                                                                                |
| <dl> <dt>"OSMajorVersion"</dt> </dl>             | Cadena que representa el número de versión principal del sistema operativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <dt>"OSMinorVersion"</dt> </dl>             | Cadena que representa el número de versión secundaria del sistema operativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <dt>"OSPlatformId"</dt> </dl>               | Cadena que representa la plataforma del sistema operativo. Los valores posibles de la propiedad **Data** son "1" para indicar un sistema de Windows no compatible y "2" para indicar un sistema Windows compatible.<br/>                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>"OSVersion"</dt> </dl>                  | Cadena que representa la versión del sistema operativo. El formato de esta cadena es *MajorVersion*. *MinorVersion*. *BuildNumber*. Por ejemplo, "5.2.3790" para Windows Server 2003.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>"ProcessorArchitecture"</dt> </dl>      | Cadena que representa la arquitectura del procesador del sistema operativo. Para obtener una lista de valores, vea el **miembro wProcessorArchitecture** de la [**estructura SYSTEM \_ INFO.**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)<br/>                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>"ProductType"</dt> </dl>                | Cadena que representa el tipo de producto. Para obtener una lista de valores, vea el **miembro wProductType** de la [**estructura OSVERSIONINFOEX.**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>"RDPAddressIPv4"</dt> </dl>             | Cadena que contiene una lista delimitada por punto y coma de las direcciones IPv4 en las que escucha actualmente la pila RDP de la máquina virtual invitada. Si la pila RDP no se está ejecutando actualmente, la cadena estará vacía. La lista se actualiza automáticamente cada vez que un cambio de configuración de TCP/IP afecta a la pila RDP en la máquina virtual invitada. Cada dirección se representa en notación decimal de punto.<br/>                                                                                                                   |
| <dl> <dt>"RDPAddressIPv6"</dt> </dl>             | Cadena que contiene una lista delimitada por punto y coma de las direcciones IPv6 en las que escucha actualmente la pila RDP de la máquina virtual invitada. Si la pila RDP no se está ejecutando actualmente, la cadena estará vacía. La lista se actualiza automáticamente cada vez que un cambio de configuración de TCP/IP afecta a la pila RDP en la máquina virtual invitada. Cada dirección se representa en notación hexadecimal de dos puntos.<br/>                                                                                                             |
| <dl> <dt>"ServicePackMajor"</dt> </dl>           | Cadena que representa el número de versión principal del Service Pack más reciente instalado en el sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>"ServicePackMinor"</dt> </dl>           | Cadena que representa el número de versión secundaria del Service Pack más reciente instalado en el sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>"SuiteMask"</dt> </dl>                  | Cadena que representa los conjuntos de productos disponibles en el sistema. Esta cadena es una combinación de cualquiera de los valores del **miembro wSuiteMask** de la [**estructura OSVERSIONINFOEX.**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)<br/>                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

**Origen**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Origen de los datos.



| Valor                                                                        | Significado                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | "HostExchangeItems" cuando lo inserta el host.<br/>                                                                                                                                                                                      |
| <dl> <dt>1</dt> </dl> | "GuestExchangeItems" cuando lo inserta la máquina virtual invitada.<br/>                                                                                                                                                                    |
| <dl> <dt>2</dt> </dl> | "GuestIntrinsicExchangeItems" cuando la máquina virtual invitada rellena automáticamente.<br/>                                                                                                                                          |
| <dl> <dt>4</dt> </dl> | Indica que el elemento es solo host y no se comparte con la máquina virtual invitada. Se usa con **la propiedad HostOnlyItems** de la [**clase Msvm \_ KvpExchangeComponentSettingData.**](msvm-kvpexchangecomponentsettingdata.md) <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase Msvm \_ KvpExchangeDataItem** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento administrado de CIM \_**](cim-managedelement.md)
</dt> <dt>

[**Elemento administrado de CIM \_**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)
</dt> </dl>

 

