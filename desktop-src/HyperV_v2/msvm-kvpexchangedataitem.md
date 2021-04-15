---
description: Representa un par clave-valor.
ms.assetid: B13E9C5F-5B13-4EE5-AE5F-F51B61BDB9B7
title: Msvm_KvpExchangeDataItem (clase)
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
ms.openlocfilehash: 540c54a694dab1c80a32f9648a90c5b5bf1e48a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688570"
---
# <a name="msvm_kvpexchangedataitem-class"></a>MSVM \_ KvpExchangeDataItem (clase)

Representa un par clave-valor.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

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

La clase **MSVM \_ KvpExchangeDataItem** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ KvpExchangeDataItem** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Data**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Parte del valor del par clave-valor.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Parte de la clave del par clave-valor.



| Clave                                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>"CSDVersion"</dt> </dl>                 | Cadena que representa la Service Pack más reciente instalada en el sistema invitado. Por ejemplo, "Service Pack 2". Si no se ha instalado ningún Service Pack, esta cadena está vacía.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>FullyQualifiedDomainName</dt> </dl>   | Cadena que representa el nombre DNS completo que identifica de forma única el equipo local. Este nombre es una combinación del nombre de host DNS y el nombre de dominio DNS, con el formato *hostname*. *NombreDeDominio*. Si el equipo local es un nodo de un clúster, este valor es el nombre DNS completo del servidor virtual de clústeres. Este valor coincide con el nombre devuelto por la función [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) cuando el parámetro *NameType* es "ComputerNameDnsFullyQualified".<br/> |
| <dl> <dt>"IntegrationServicesVersion"</dt> </dl> | Una cadena que representa la versión del Integration Services instalado actualmente en la máquina virtual invitada (por ejemplo, "6.1.7000.0").<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>"NetworkAddressIPv4"</dt> </dl>         | Una cadena que contiene una lista delimitada por signos de punto y coma de las direcciones IPv4 asignadas actualmente a la máquina virtual invitada. La lista se actualiza automáticamente cuando se produce un cambio de configuración de TCP/IP en la máquina virtual invitada. Cada dirección se representa en notación punto-decimal. <br/>                                                                                                                                                                                                                         |
| <dl> <dt>"NetworkAddressIPv6"</dt> </dl>         | Una cadena que contiene una lista delimitada por signos de punto y coma de las direcciones IPv6 asignadas actualmente a la máquina virtual invitada. La lista se actualiza automáticamente cuando se produce un cambio de configuración de TCP/IP en la máquina virtual invitada. Cada dirección se representa en notación hexadecimal con dos puntos. No se garantiza que las listas IPv4 e IPv6 estén sincronizadas en todo momento.<br/>                                                                                                                                             |
| <dl> <dt>"OSBuildNumber"</dt> </dl>              | Cadena que representa el número de compilación del sistema operativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>"OSEditionId"</dt> </dl>                | Una cadena que representa la edición (SKU) del sistema operativo de la máquina virtual invitada. Para obtener una lista de los valores posibles, vea la función [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .<br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>OSName</dt> </dl>                     | Cadena que representa el nombre del sistema operativo. Este valor procede de la siguiente entrada del registro: **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProductName**<br/> <br/>                                                                                                                                                                                                                                                                                |
| <dl> <dt>OSMajorVersion</dt> </dl>             | Cadena que representa el número de versión principal del sistema operativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <dt>OSMinorVersion</dt> </dl>             | Cadena que representa el número de versión secundaria del sistema operativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <dt>"OSPlatformId"</dt> </dl>               | Cadena que representa la plataforma del sistema operativo. Los valores posibles de la propiedad **Data** son "1" para indicar un sistema de Windows no compatible y "2" para indicar un sistema de Windows compatible.<br/>                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>OSVersion</dt> </dl>                  | Cadena que representa la versión del sistema operativo. El formato de esta cadena es *MajorVersion*. *MinorVersion*. *BuildNumber*. Por ejemplo, "5.2.3790" para Windows Server 2003.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>ProcessorArchitecture</dt> </dl>      | Cadena que representa la arquitectura del procesador del sistema operativo. Para obtener una lista de valores, vea el miembro **wProcessorArchitecture** de la estructura de [**\_ información del sistema**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) .<br/>                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>ProductType</dt> </dl>                | Cadena que representa el tipo de producto. Para obtener una lista de valores, vea el miembro **wProductType** de la estructura [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>"RDPAddressIPv4"</dt> </dl>             | Una cadena que contiene una lista delimitada por signos de punto y coma de las direcciones IPv4 en las que la pila RDP de la máquina virtual invitada está escuchando actualmente. Si la pila RDP no se está ejecutando actualmente, la cadena estará vacía. La lista se actualiza automáticamente siempre que un cambio de configuración de TCP/IP afecte a la pila de RDP en la máquina virtual invitada. Cada dirección se representa en notación punto-decimal.<br/>                                                                                                                   |
| <dl> <dt>"RDPAddressIPv6"</dt> </dl>             | Una cadena que contiene una lista delimitada por signos de punto y coma de las direcciones IPv6 en las que la pila RDP de la máquina virtual invitada está escuchando actualmente. Si la pila RDP no se está ejecutando actualmente, la cadena estará vacía. La lista se actualiza automáticamente siempre que un cambio de configuración de TCP/IP afecte a la pila de RDP en la máquina virtual invitada. Cada dirección se representa en notación hexadecimal con dos puntos.<br/>                                                                                                             |
| <dl> <dt>"ServicePackMajor"</dt> </dl>           | Cadena que representa el número de versión principal de la Service Pack más reciente instalada en el sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>"ServicePackMinor"</dt> </dl>           | Cadena que representa el número de versión secundaria de la Service Pack más reciente instalada en el sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>"SuiteMask"</dt> </dl>                  | Cadena que representa los conjuntos de productos disponibles en el sistema. Esta cadena es una combinación de cualquiera de los valores del miembro **wSuiteMask** de la estructura [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .<br/>                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

**Origen**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Origen de los datos.



| Value                                                                        | Significado                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | "HostExchangeItems" cuando lo inserte el host.<br/>                                                                                                                                                                                      |
| <dl> <dt>1</dt> </dl> | "GuestExchangeItems" cuando lo inserte la máquina virtual invitada.<br/>                                                                                                                                                                    |
| <dl> <dt>2</dt> </dl> | "GuestIntrinsicExchangeItems" cuando lo rellena automáticamente la máquina virtual invitada.<br/>                                                                                                                                          |
| <dl> <dt>4</dt> </dl> | Indica que el elemento es solo de host y no se comparte con la máquina virtual invitada. Se usa con la propiedad **HostOnlyItems** de la clase [**\_ KvpExchangeComponentSettingData de MSVM**](msvm-kvpexchangecomponentsettingdata.md) . <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ KvpExchangeDataItem** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ManagedElement de CIM \_**](cim-managedelement.md)
</dt> <dt>

[**ManagedElement de CIM \_**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)
</dt> </dl>

 

