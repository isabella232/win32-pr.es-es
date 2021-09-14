---
description: Win32 \_ TCPIPPrinterPort&\# 32; La clase WMI representa un punto de acceso de servicio TCP/IP.
ms.assetid: b1be18b6-47de-461c-a90b-c7e0537130ef
ms.tgt_platform: multiple
title: Win32_TCPIPPrinterPort clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TCPIPPrinterPort
- Win32_TCPIPPrinterPort.Caption
- Win32_TCPIPPrinterPort.Description
- Win32_TCPIPPrinterPort.InstallDate
- Win32_TCPIPPrinterPort.Status
- Win32_TCPIPPrinterPort.CreationClassName
- Win32_TCPIPPrinterPort.Name
- Win32_TCPIPPrinterPort.SystemCreationClassName
- Win32_TCPIPPrinterPort.SystemName
- Win32_TCPIPPrinterPort.Type
- Win32_TCPIPPrinterPort.ByteCount
- Win32_TCPIPPrinterPort.HostAddress
- Win32_TCPIPPrinterPort.PortNumber
- Win32_TCPIPPrinterPort.Protocol
- Win32_TCPIPPrinterPort.Queue
- Win32_TCPIPPrinterPort.SNMPCommunity
- Win32_TCPIPPrinterPort.SNMPDevIndex
- Win32_TCPIPPrinterPort.SNMPEnabled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a0b0f0cb73cc60ff117399a636b0ab8542fac6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061421"
---
# <a name="win32_tcpipprinterport-class"></a>Clase TCPIPPrinterPort de Win32 \_

La **clase WMI \_ TCPIPPrinterPort** [de](../wmisdk/retrieving-a-class.md) Win32 representa un punto de acceso de servicio TCP/IP.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_TCPIPPrinterPort : CIM_ServiceAccessPoint
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
  boolean  ByteCount;
  string   HostAddress;
  uint32   PortNumber;
  uint32   Protocol;
  string   Queue;
  string   SNMPCommunity;
  uint32   SNMPDevIndex;
  boolean  SNMPEnabled;
};
```

## <a name="members"></a>Members

La **clase \_ TCPIPPrinterPort de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ TCPIPPrinterPort de Win32** tiene estas propiedades.

<dl> <dt>

**ByteCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el equipo cuenta los bytes de un documento antes de enviarlos a la impresora y la impresora informa del número de bytes leídos realmente. Esta funcionalidad se usa para los diagnósticos cuando se detectan bytes que faltan en la salida de impresión.

</dd> <dt>

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

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**\_ clave CIM,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nombre de la clase o subclase usada en la creación de una instancia de . Cuando se usa con otras propiedades clave de la clase , esta propiedad permite identificar de forma única todas las instancias de la clase y sus subclases.

Esta propiedad se hereda de [**CIM \_ ServiceAccessPoint.**](cim-serviceaccesspoint.md)

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

**HostAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección del dispositivo o servidor de impresión.

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

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identifica de forma única el punto de acceso de servicio y proporciona una indicación de la funcionalidad que se administra. Esta funcionalidad se describe con más detalle en la propiedad Description del objeto.

Esta propiedad se hereda de [**CIM \_ ServiceAccessPoint.**](cim-serviceaccesspoint.md)

</dd> <dt>

**Númerodepuerto**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de puertos TCP utilizados por el monitor de puertos para comunicarse con el dispositivo.

</dd> <dt>

**Protocolo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Protocolo de impresión utilizado. Algunas impresoras solo admiten LPR.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

RAW

Imprimir directamente en un dispositivo o servidor de impresión.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

LPR

Protocolo heredado, que finalmente se reemplaza por RAW.

</dd> </dl>

</dd> <dt>

**Cola**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la cola de impresión en el servidor cuando se usa con el protocolo LPR.

</dd> <dt>

**SNMPCommunity**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de nivel de seguridad para el dispositivo.

Ejemplo: "public""

</dd> <dt>

**SNMPDevIndex**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de índice SNMP de este dispositivo para el agente SNMP.

</dd> <dt>

**SNMPEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** esta impresora admite [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Protocolo simple de administración de redes) y puede proporcionar información de estado enriquección del dispositivo.

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

El estado no operativo puede incluir "Error", "Starting", "Stopping" y "Service". El "servicio" se puede aplicar durante la resilvering del reflejo del disco, volver a cargar una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "correcto" ni está en uno de los demás estados.

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

**Desconocido** ("Desconocido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Error de pred** ("error previo")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**A partir** de ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detención** ("Deteniendo")


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

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Propagados**](../wmisdk/standard-qualifiers.md) ("[**Sistema CIM \_**](cim-system.md).**CreationClassName**"), [**\_ clave CIM,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nombre de clase de creación del sistema de ámbito.

Esta propiedad se hereda de [**CIM \_ ServiceAccessPoint.**](cim-serviceaccesspoint.md)

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Propagados**](../wmisdk/standard-qualifiers.md) ("[**Sistema CIM \_**](cim-system.md).**Name**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nombre del sistema de ámbito.

Esta propiedad se hereda de [**CIM \_ ServiceAccessPoint.**](cim-serviceaccesspoint.md)

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Esquema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Tipo de SAP, como asociado o redirigido.

Esta propiedad se hereda de [**CIM \_ ServiceAccessPoint.**](cim-serviceaccesspoint.md)

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

**Escritura** (1)


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

**Lectura** (2)


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

**Redirigido** (4)


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

**Net \_ Conectado** (8)


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

**unknown** (16)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ TCPIPPrinterPort de Win32** se deriva de [**CIM \_ ServiceAccessPoint,**](cim-serviceaccesspoint.md) que deriva de [**CIM \_ LogicalElement**](cim-logicalelement.md).

El **privilegio SeLoadDriverPrivilege** es necesario para eliminar una instancia de esta clase WMI. El siguiente fragmento de script muestra cómo realizar una conexión a WMI que usa este privilegio.

`Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate, (LoadDriver)}")`

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de PowerShell quita una impresora y el puerto de impresora TCPIP asociado.


```PowerShell
function Remove-PrinterAndPort{
    Param( $printername )
   $printer=gwmi win32_Printer -filter "name='HPDJ600'"
   $printer.Delete()
   $port=gwmi win32_tcpipprinterport -filter "name='$($printer.portname)'" -enableall
   $port.Delete()
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Servicio \_ CIMAccessPoint**](cim-serviceaccesspoint.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
