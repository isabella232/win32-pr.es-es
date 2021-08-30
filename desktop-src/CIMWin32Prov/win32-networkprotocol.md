---
description: La aplicación \_ NetworkProtocol de Win32&\# 8194; La clase WMI representa un protocolo y sus características de red en un sistema de equipo Win32.
ms.assetid: c864a694-d507-4629-91c5-bd26ccf397f7
ms.tgt_platform: multiple
title: Win32_NetworkProtocol clase
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
ms.openlocfilehash: 1e11fcfefb817a2ecc94914cccd96335100e2e2ae1c072af3bd9bf879f4d1e46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972652"
---
# <a name="win32_networkprotocol-class"></a>Clase NetworkProtocol de Win32 \_

La clase  [WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkProtocol de Win32** representa un protocolo y sus características de red en un sistema de equipo Win32.

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

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descripción textual del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**ConnectionlessService**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIN32 \_ API Windows \| \| Sockets PROTOCOL INFO \_ \| dwServiceFlags \| XP1 \_ CONNECTIONLESS")
</dt> </dl>

El protocolo admite el servicio sin conexión. Un servicio sin conexión (datagrama) describe un protocolo de comunicaciones o transporte en el que los paquetes de datos se enrutan de forma independiente entre sí y pueden seguir rutas diferentes y llegar en un orden diferente al que se enviaron. Por el contrario, un servicio orientado a la conexión proporciona un circuito virtual a través del cual los paquetes de datos se reciben en el mismo orden en que se transmitieron. Si se produce un error en la conexión entre equipos, se notifica a la aplicación.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descripción textual del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**GuaranteesDelivery**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API Windows \| \| Sockets PROTOCOL INFO \_ \| dwServiceFlags \| XP GUARANTEED \_ \_ DELIVERY")
</dt> </dl>

El protocolo admite la entrega de paquetes de datos. Si esta marca es **FALSE,** no está seguro de que todos los datos enviados lleguen al destino previsto.

</dd> <dt>

**GuaranteesSequencing**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API Windows \| \| Sockets PROTOCOL INFO \_ \| dwServiceFlags \| XP GUARANTEED \_ \_ ORDER")
</dt> </dl>

El protocolo garantiza que los datos lleguen en el orden en que se enviaron. Tenga en cuenta que esta característica no garantiza la entrega de los datos, solo su pedido.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Fecha de instalación")
</dt> </dl>

Indica cuándo se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**MaximumAddressSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API Windows \| Sockets PROTOCOL INFO \| \_ \| iMaxSockAddr"), [**unidades**](../wmisdk/standard-qualifiers.md) ("caracteres")
</dt> </dl>

Longitud máxima de una dirección de socket admitida por el protocolo. Las direcciones de socket pueden ser elementos como una dirección URL ( `www.microsoft.com` ) o una dirección IP ( `130.215.24.1` ).

</dd> <dt>

**MaximumMessageSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API Windows \| Sockets PROTOCOL INFO \| \_ \| dwMessageSize"), [**unidades**](../wmisdk/standard-qualifiers.md) ("caracteres")
</dt> </dl>

Tamaño máximo del mensaje admitido por el protocolo. Este es el tamaño máximo de un mensaje que el host puede enviar o recibir. Para los protocolos que no admiten tramas de mensajes, el tamaño máximo real de un mensaje que se puede enviar a una dirección determinada puede ser menor que este valor.

</dd> <dt>

**MessageOriented**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) \_ ("WIN32 API \| Windows \| Sockets PROTOCOL INFO \_ \| dwServiceFlags \| XP MESSAGE \_ \_ ORIENTED")
</dt> </dl>

El protocolo está orientado a mensajes. Un protocolo orientado a mensajes usa paquetes de datos para transferir información. Por el contrario, los protocolos orientados a secuencias transfieren datos como una secuencia continua de bytes.

</dd> <dt>

**MinimumAddressSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) \_ ("Win32 API \| Windows Sockets PROTOCOL INFO \| \_ \| iMinSockAddr "), [**unidades**](../wmisdk/standard-qualifiers.md) ("caracteres")
</dt> </dl>

Longitud mínima de una dirección de socket admitida por el protocolo.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API Windows \| Sockets Structures PROTOCOL INFO \| \_ \| lpProtocol")
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

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIN32 \_ API Windows \| \| Sockets PROTOCOL INFO \_ \| dwServiceFlags \| XP PSEUDO \_ \_ STREAM")
</dt> </dl>

Protocol es un protocolo orientado a mensajes que puede recibir paquetes de datos de longitud variable o datos transmitidos para todas las operaciones de recepción. Esta capacidad opcional es útil cuando una aplicación no quiere que el protocolo enmarca los mensajes y requiere características orientadas a secuencias. Si **es TRUE,** el protocolo está pseudo orientado a secuencias.

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Cadena que indica el estado actual del objeto. Se puede definir el estado operativo y no operativo. El estado operativo puede incluir "Ok", "Degraded" y "Pred Fail". "Error previo" indica que un elemento funciona correctamente, pero predice un error (por ejemplo, una unidad de disco duro habilitada para SMART).

El estado no operativo puede incluir "Error", "Starting", "Stopping" y "Service". "Servicio" se puede aplicar durante la resilvering de reflejo del disco, volver a cargar una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "Correcto" ni está en uno de los demás estados.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Los valores son los siguientes:

<dt>

<span id="OK"></span><span id="ok"></span>

**Ok** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("Error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("Degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unknown** ("Unknown")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Error de pred** ("error previo")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Starting** ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detención** ("Detención")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servicio** ("Servicio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Estresado** ("estresado")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sin contacto** ("Sin contacto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comm perdido** ("Comm perdido")


</dt> <dd></dd> </dl>

</dd> <dt>

**Admite la difusión por difusión**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIN32 \_ API Windows \| \| Sockets PROTOCOL INFO \_ \| dwServiceFlags \| XP SUPPORTS \_ \_ BROADCAST")
</dt> </dl>

El protocolo admite un mecanismo para difundir mensajes a través de la red.

</dd> <dt>

**SupportsConnectData**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API Windows \| Sockets PROTOCOL INFO \| \_ \| dwServiceFlags \| XP CONNECT \_ \_ DATA")
</dt> </dl>

El protocolo permite que los datos se conecten a través de la red.

</dd> <dt>

**SupportsDisconnectData**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API Windows \| Sockets PROTOCOL INFO \| \_ \| dwServiceFlags \| XP DISCONNECT \_ \_ DATA")
</dt> </dl>

El protocolo permite desconectar los datos a través de la red.

</dd> <dt>

**SupportsEncryption**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIN32 \_ API Windows \| \| Sockets PROTOCOL INFO \_ \| dwServiceFlags \| XP \_ ENCRYPTS")
</dt> </dl>

El protocolo admite el cifrado de datos.

</dd> <dt>

**SupportsExpeditedData**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIN32 \_ API Windows \| \| Sockets PROTOCOL INFO \_ \| dwServiceFlags \| XP \_ EXPEDITED \_ DATA")
</dt> </dl>

El protocolo admite datos rápidos (también conocidos como datos urgentes) en toda la red. Los datos acelerados pueden omitir el control de flujo y recibir prioridad sobre los paquetes de datos normales.

</dd> <dt>

**SupportsFragmentation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIN32 \_ API Windows \| \| Sockets PROTOCOL INFO \_ \| dwServiceFlags \| XP \_ FRAGMENTATION")
</dt> </dl>

El protocolo admite la transmisión de los datos en fragmentos. La unidad de transferencia máxima de red física (MTU) está oculta en las aplicaciones. Cada tipo de medio tiene un tamaño máximo de fotograma que no se puede superar. La capa de vínculo detecta la MTU y la notifica a los protocolos usados.

</dd> <dt>

**SupportsGracefulClosing**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API Windows \| \| Sockets PROTOCOL INFO \_ \| dwServiceFlags \| XP GRACEFUL \_ \_ CLOSE")
</dt> </dl>

El protocolo admite operaciones de cierre en dos fases, también conocidas como "operaciones de cierre correcto". Si no es así, el protocolo solo admite operaciones de cierre abortivas.

</dd> <dt>

**SupportsGuaranteedBandwidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API win32 \_ Windows \| \| sockets PROTOCOL INFO \_ \| dwServiceFlags \| XP BANDWIDTH \_ \_ ALLOCATION")
</dt> </dl>

El protocolo tiene un mecanismo para establecer y mantener un ancho de banda.

</dd> <dt>

**Admite multicasting**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API Windows \| \| Sockets PROTOCOL INFO \_ \| dwServiceFlags \| XP SUPPORTS \_ \_ MULTICAST")
</dt> </dl>

El protocolo admite la multidifusión.

</dd> <dt>

**SupportsQualityofService**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIN32 \_ API Windows \| Sockets Structures \| WSAPROTOCOL \_ INFO \| dwServiceFlags1 \| XP1 \_ QOS \_ SUPPORTED")
</dt> </dl>

El protocolo es capaz de admitir calidad de servicio (QoS) por el proveedor de servicios en capas subyacente o el transportista de transporte. QoS es una colección de componentes que permiten diferenciar y tratar preferentemente los subconjuntos de datos transmitidos a través de la red. QoS significa que los subconjuntos de datos obtienen una prioridad más alta o un servicio garantizado al atravesar una red.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ NetworkProtocol de Win32** se deriva de [**\_ LOGICALElement de CIM.**](cim-logicalelement.md)

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se muestra cómo recuperar una lista de servicios en ejecución de instancias de **\_ NetworkProtocol de Win32.**


```VB
Set ProtocolSet = GetObject("winmgmts:").ExecQuery("select * from Win32_NetworkProtocol")

for each Protocol in ProtocolSet
 WScript.Echo Protocol.Name
next
```



En el ejemplo de código perl siguiente se muestra cómo recuperar una lista de servicios en ejecución de instancias de **\_ NetworkProtocol de Win32.**


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
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento \_ lógico CIM**](cim-logicalelement.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
