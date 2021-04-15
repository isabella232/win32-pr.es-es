---
description: Win32 \_ NetworkProtocol&\# 8194; La clase WMI representa un protocolo y sus características de red en un sistema de Win32.
ms.assetid: c864a694-d507-4629-91c5-bd26ccf397f7
ms.tgt_platform: multiple
title: Win32_NetworkProtocol (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkProtocol
- Win32_NetworkProtocol.Caption
- Win32_NetworkProtocol.Description
- Win32_NetworkProtocol.InstallDate
- Win32_NetworkProtocol.Status
- Win32_NetworkProtocol.ConnectionlessService
- Win32_NetworkProtocol.GuaranteesDelivery
- Win32_NetworkProtocol.GuaranteesSequencing
- Win32_NetworkProtocol.MaximumAddressSize
- Win32_NetworkProtocol.MaximumMessageSize
- Win32_NetworkProtocol.MessageOriented
- Win32_NetworkProtocol.MinimumAddressSize
- Win32_NetworkProtocol.Name
- Win32_NetworkProtocol.PseudoStreamOriented
- Win32_NetworkProtocol.SupportsBroadcasting
- Win32_NetworkProtocol.SupportsConnectData
- Win32_NetworkProtocol.SupportsDisconnectData
- Win32_NetworkProtocol.SupportsEncryption
- Win32_NetworkProtocol.SupportsExpeditedData
- Win32_NetworkProtocol.SupportsFragmentation
- Win32_NetworkProtocol.SupportsGracefulClosing
- Win32_NetworkProtocol.SupportsGuaranteedBandwidth
- Win32_NetworkProtocol.SupportsMulticasting
- Win32_NetworkProtocol.SupportsQualityofService
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33817fa4aa55747ecf9d4e89f5dcf406160c0c67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496595"
---
# <a name="win32_networkprotocol-class"></a>\_Clase Win32 NetworkProtocol

La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkProtocol de Win32** representa un protocolo y sus características de red en un sistema de Win32.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkProtocol : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  ConnectionlessService;
  boolean  GuaranteesDelivery;
  boolean  GuaranteesSequencing;
  uint32   MaximumAddressSize;
  uint32   MaximumMessageSize;
  boolean  MessageOriented;
  uint32   MinimumAddressSize;
  string   Name;
  boolean  PseudoStreamOriented;
  boolean  SupportsBroadcasting;
  boolean  SupportsConnectData;
  boolean  SupportsDisconnectData;
  boolean  SupportsEncryption;
  boolean  SupportsExpeditedData;
  boolean  SupportsFragmentation;
  boolean  SupportsGracefulClosing;
  boolean  SupportsGuaranteedBandwidth;
  boolean  SupportsMulticasting;
  boolean  SupportsQualityofService;
};
```

## <a name="members"></a>Miembros

La **clase \_ NetworkProtocol de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ NetworkProtocol de Win32** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descripción textual del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**ConnectionlessService**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API de Win32 \_ \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP1 \_ sin conexión")
</dt> </dl>

El protocolo admite el servicio sin conexión. Un servicio sin conexión (datagrama) describe un protocolo de comunicaciones o transporte en el que los paquetes de datos se enrutan de forma independiente entre sí y pueden seguir rutas diferentes y llegar en un orden diferente al que se enviaron. Por el contrario, un servicio orientado a la conexión proporciona un circuito virtual a través del cual los paquetes de datos se reciben en el mismo orden en que se transmitiron. Si se produce un error en la conexión entre equipos, se notifica a la aplicación.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")
</dt> </dl>

Una descripción textual del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**GuaranteesDelivery**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API de Win32 \_ \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP \_ entrega garantizada \_ ")
</dt> </dl>

El protocolo admite la entrega de paquetes de datos. Si esta marca es **false**, no está seguro de que todos los datos enviados llegarán al destino previsto.

</dd> <dt>

**GuaranteesSequencing**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| Protocolo \_ info \| dwServiceFlags \| XP \_ \_ orden garantizado")
</dt> </dl>

El protocolo garantiza que los datos llegarán en el orden en que se enviaron. Tenga en cuenta que esta característica no garantiza la entrega de los datos, solo su orden.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")
</dt> </dl>

Indica cuándo se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**MaximumAddressSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets Structures \| Protocol \_ info \| iMaxSockAddr"), [**unidades**](../wmisdk/standard-qualifiers.md) ("caracteres")
</dt> </dl>

Longitud máxima de una dirección de socket compatible con el protocolo. Las direcciones de socket pueden ser elementos como una dirección URL ( `www.microsoft.com` ) o una dirección IP ( `130.215.24.1` ).

</dd> <dt>

**MaximumMessageSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets Structures \| Protocol \_ info \| dwMessageSize"), [**unidades**](../wmisdk/standard-qualifiers.md) ("caracteres")
</dt> </dl>

Tamaño máximo de mensaje admitido por el protocolo. Es el tamaño máximo de un mensaje que puede ser enviado o recibido por el host. En el caso de los protocolos que no admiten tramas de mensajes, el tamaño máximo real de un mensaje que se puede enviar a una dirección determinada puede ser inferior a este valor.

</dd> <dt>

**MessageOriented**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API de Win32 \_ \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP \_ Message \_ orientada")
</dt> </dl>

El protocolo está orientado a mensajes. Un protocolo orientado a mensajes usa paquetes de datos para transferir información. Por el contrario, los protocolos orientados a flujos transfieren los datos como una secuencia continua de bytes.

</dd> <dt>

**MinimumAddressSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets Structures \| Protocol \_ info \| iMinSockAddr"), [**unidades**](../wmisdk/standard-qualifiers.md) ("caracteres")
</dt> </dl>

Longitud mínima de una dirección de socket compatible con el protocolo.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API de Win32 \| Windows Sockets de la información de \| Protocolo \_ \| lpProtocol")
</dt> </dl>

Nombre del protocolo.

Ejemplo: "TCP/IP"

</dd> <dt>

**PseudoStreamOriented**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets Structures \| Protocolo \_ info \| dwServiceFlags \| XP \_ pseudo \_ Stream")
</dt> </dl>

Es un protocolo orientado a mensajes que puede recibir paquetes de datos de longitud variable o datos transmitidos para todas las operaciones de recepción. Esta capacidad opcional es útil cuando una aplicación no desea que el protocolo contenga el marco de mensajes y requiere características orientadas a flujos. Si es **true**, el protocolo está orientado a pseudo streaming.

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Cadena que indica el estado actual del objeto. Se puede definir un estado operativo y no operativo. El estado operativo puede ser "correcto", "degradado" y "Pred FAIL". "Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).

El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio". "Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

Los valores son los siguientes:

<dt>

<span id="OK"></span><span id="ok"></span>

**Aceptar** ("Aceptar")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("desconocido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred FAIL** ("Pred FAIL")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detener** ("detener")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servicio** ("servicio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

Con **estrés** ("acentuado")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Recover** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sin contacto** ("sin contacto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comunicación perdida** ("pérdida de comunicación")


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportsBroadcasting**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets Structures \| Protocol \_ info \| dwServiceFlags \| XP \_ Supports \_ ")
</dt> </dl>

El protocolo admite un mecanismo para difundir mensajes a través de la red.

</dd> <dt>

**SupportsConnectData**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets Structures \| Protocolo \_ info \| dwServiceFlags \| XP \_ Connect \_ Data")
</dt> </dl>

El protocolo permite que los datos se conecten a través de la red.

</dd> <dt>

**SupportsDisconnectData**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API de Win32 \_ \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP \_ Disconnect \_ Data")
</dt> </dl>

El protocolo permite que los datos se desconecten a través de la red.

</dd> <dt>

**SupportsEncryption**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API de Win32 de \_ \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP \_ cifrado")
</dt> </dl>

El protocolo admite el cifrado de datos.

</dd> <dt>

**SupportsExpeditedData**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP \_ datos acelerados \_ ")
</dt> </dl>

El protocolo admite datos inmediatos (también conocidos como datos urgentes) a través de la red. Los datos expedidos pueden omitir el control de flujo y recibir prioridad sobre los paquetes de datos normales.

</dd> <dt>

**SupportsFragmentation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| fragmentación de XP \_ ")
</dt> </dl>

El protocolo admite la transmisión de los datos en fragmentos. La unidad de transferencia máxima (MTU) de red física está oculta en las aplicaciones. Cada tipo de medio tiene un tamaño de fotograma máximo que no se puede superar. La capa de vínculo detecta la MTU y la notifica a los protocolos usados.

</dd> <dt>

**SupportsGracefulClosing**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API de Win32 de \_ \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP \_ \_ cierre correcto")
</dt> </dl>

El protocolo admite operaciones de cierre en dos fases, también conocidas como "operaciones de cierre correcto". En caso contrario, el protocolo solo admite operaciones de cierre de anulación.

</dd> <dt>

**SupportsGuaranteedBandwidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets Structures \| Protocolo \_ info \| dwServiceFlags \| XP \_ Bandwidth \_ Allocation")
</dt> </dl>

El protocolo tiene un mecanismo para establecer y mantener un ancho de banda.

</dd> <dt>

**SupportsMulticasting**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API de Win32 de \_ \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP \_ admite \_ multidifusión")
</dt> </dl>

El protocolo admite la multidifusión.

</dd> <dt>

**SupportsQualityofService**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| WSAPROTOCOL \_ info \| dwServiceFlags1 \| XP1 \_ QoS \_ Supported")
</dt> </dl>

El protocolo es capaz de admitir la calidad de servicio (QoS) por parte del proveedor de servicios superpuestos o del operador de transporte subyacente. QoS es una colección de componentes que permiten la diferenciación y el trato preferencial de los subconjuntos de datos transmitidos a través de la red. QoS significa que los subconjuntos de datos obtienen mayor prioridad o servicio garantizado al atravesar una red.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ NetworkProtocol de Win32** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se muestra cómo recuperar una lista de servicios en ejecución de instancias de **Win32 \_ NetworkProtocol**.


```VB
Set ProtocolSet = GetObject("winmgmts:").ExecQuery("select * from Win32_NetworkProtocol")

for each Protocol in ProtocolSet
 WScript.Echo Protocol.Name
next
```



El siguiente ejemplo de código Perl muestra cómo recuperar una lista de servicios en ejecución de instancias de **Win32 \_ NetworkProtocol**.


```
use strict;
use Win32::OLE;

my ( $ProtocolSet, $Protocol );

eval { $ProtocolSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkProtocol"); };
unless($@)
{
 print "\n";
 foreach $Protocol (in $ProtocolSet) 
 {
  print $Protocol->{Name}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_LOGICALELEMENT CIM**](cim-logicalelement.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
