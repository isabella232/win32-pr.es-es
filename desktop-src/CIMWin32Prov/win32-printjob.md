---
description: Representa un trabajo de impresión generado por una aplicación de Windows. Cualquier unidad de trabajo generada por el comando de impresión de una aplicación que se ejecuta en un equipo que ejecuta en un sistema operativo Windows es un descendiente o un miembro de esta clase.
ms.assetid: d884acba-e1b2-4d24-9b55-15d175a163d9
ms.tgt_platform: multiple
title: Win32_PrintJob (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob
- Win32_PrintJob.Caption
- Win32_PrintJob.Description
- Win32_PrintJob.InstallDate
- Win32_PrintJob.Name
- Win32_PrintJob.Status
- Win32_PrintJob.ElapsedTime
- Win32_PrintJob.JobStatus
- Win32_PrintJob.Notify
- Win32_PrintJob.Owner
- Win32_PrintJob.Priority
- Win32_PrintJob.StartTime
- Win32_PrintJob.TimeSubmitted
- Win32_PrintJob.UntilTime
- Win32_PrintJob.Color
- Win32_PrintJob.DataType
- Win32_PrintJob.Document
- Win32_PrintJob.DriverName
- Win32_PrintJob.HostPrintQueue
- Win32_PrintJob.JobId
- Win32_PrintJob.PagesPrinted
- Win32_PrintJob.PaperLength
- Win32_PrintJob.PaperSize
- Win32_PrintJob.PaperWidth
- Win32_PrintJob.Parameters
- Win32_PrintJob.PrintProcessor
- Win32_PrintJob.Size
- Win32_PrintJob.StatusMask
- Win32_PrintJob.TotalPages
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10f56034161a9313eed1b7d302ab790d153c0ee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659671"
---
# <a name="win32_printjob-class"></a>\_Clase PrintJob de Win32

La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PrintJob de Win32** representa un trabajo de impresión generado por una aplicación de Windows. Cualquier unidad de trabajo generada por el comando de impresión de una aplicación que se ejecuta en un equipo que ejecuta en un sistema operativo Windows es un descendiente o un miembro de esta clase.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_PrintJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   JobStatus;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime StartTime;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Color;
  string   DataType;
  string   Document;
  string   DriverName;
  string   HostPrintQueue;
  uint32   JobId;
  uint32   PagesPrinted;
  uint32   PaperLength;
  string   PaperSize;
  uint32   PaperWidth;
  string   Parameters;
  string   PrintProcessor;
  uint32   Size;
  uint32   StatusMask;
  uint32   TotalPages;
};
```

## <a name="members"></a>Miembros

La clase de **Win32 \_ PrintJob** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase de **Win32 \_ PrintJob** tiene estos métodos.



| Método                                                  | Descripción                       |
|:--------------------------------------------------------|:----------------------------------|
| [**Pausar**](pause-method-in-class-win32-printjob.md)   | Pausa un trabajo de impresión.<br/>    |
| [**Reanudar**](resume-method-in-class-win32-printjob.md) | Continúa un trabajo de impresión.<br/> |



 

### <a name="properties"></a>Propiedades

La clase de **Win32 \_ PrintJob** tiene estas propiedades.

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

**Color**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que indica si el documento se imprime en color o monocromo. Algunas impresoras de color tienen la capacidad de imprimir con verdadero negro en lugar de una combinación de amarillo, aguamarina y magenta. True Black normalmente crea texto más oscuro y más nítido para los documentos. Esta opción solo es útil para las impresoras de color que admiten la impresión en negro real.

Los valores son:

<dl><span id="_Color_"></span><span id="_color_"></span><span id="_COLOR_"></span><dt>

**Color**
</dt><span id="_Monochrome_"></span><span id="_monochrome_"></span><span id="_MONOCHROME_"></span><dt>

**Monocromática**
</dt> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Formato de los datos de este trabajo de impresión. Esto indica al controlador de impresora que traduzca los datos (texto genérico, PostScript o PCL) antes de imprimir o imprime en formato sin procesar (para gráficos e imágenes).

Ejemplo: "TEXT"

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

**Documento**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del trabajo de impresión. El usuario verá este nombre al ver los documentos que están a la espera de ser impresos.

Ejemplo: "Microsoft Word-Review.doc"

</dd> <dt>

**DriverName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del controlador de impresora utilizado para el trabajo de impresión.

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Período de tiempo durante el que se ha estado ejecutando el trabajo.

Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).

</dd> <dt>

**HostPrintQueue**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo en el que se crea el trabajo de impresión.

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

**JobId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de identificación del trabajo. Lo utilizan otros métodos como identificador de un trabajo que se pone en cola en la impresora.

</dd> <dt>

**Estado del trabajo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que representa el estado del trabajo.

Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**Notificar**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Se notifica al usuario sobre la finalización o el error del trabajo.

Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).

</dd> <dt>

**Propietario**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Usuario que envió el trabajo.

Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).

</dd> <dt>

**PagesPrinted**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de páginas que se imprimen. Este valor puede ser 0 (cero) si el trabajo de impresión no contiene información de delimitación de página.

</dd> <dt>

**PaperLength**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (décimas de milímetro).
</dt> </dl>

Longitud del papel.

Ejemplo: 2794

</dd> <dt>

**PaperSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño del papel que se usa para imprimir el trabajo. El valor es uno de los tamaños de papel posibles para la impresora especificada en la propiedad **PaperSizesSupported** de la clase [**\_ Printer de Win32**](win32-printer.md) .

</dd> <dt>

**PaperWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (décimas de milímetro).
</dt> </dl>

Ancho del papel.

Ejemplo: 2159

</dd> <dt>

**Parámetros**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Parámetros opcionales que se van a enviar al procesador de impresión. Para obtener más información, vea la propiedad **PrintProcessor** .

</dd> <dt>

**PrintProcessor**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Servicio de procesador de impresión usado para procesar el trabajo de impresión. Un procesador de impresora funciona junto con el controlador de impresora para proporcionar una traducción adicional de los datos de la impresora y también se puede usar para proporcionar opciones especiales, como una página de título para el trabajo.

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Importancia de la ejecución de un trabajo.

Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).

</dd> <dt>

**Tamaño**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (bytes)
</dt> </dl>

Tamaño del trabajo de impresión.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora a la que comenzó el trabajo.

Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).

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

**StatusMask**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Mapa de bits de los posibles estados relacionados con este trabajo de impresión.

<dt>

1 (0x1)
</dt> <dd>

En pausa

</dd> <dt>

2 (0X2)
</dt> <dd>

Error

</dd> <dt>

4 (0x4)
</dt> <dd>

Eliminando

</dd> <dt>

8 (0x8)
</dt> <dd>

En cola

</dd> <dt>

16 (0x10)
</dt> <dd>

Impresión

</dd> <dt>

32 (0x20)
</dt> <dd>

Sin conexión

</dd> <dt>

64 (0x40)
</dt> <dd>

Paperout

</dd> <dt>

128 (0x80)
</dt> <dd>

Imprimir

</dd> <dt>

256 (0x100)
</dt> <dd>

Deleted

</dd> <dt>

512 (0x200)
</dt> <dd>

\_DevQ bloqueado

</dd> <dt>

1024 (0x400)
</dt> <dd>

\_Solicitud de intervención del usuario \_

</dd> <dt>

2048 (0x800)
</dt> <dd>

Reiniciar

</dd> </dl>

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora a la que se envió el trabajo.

Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).

</dd> <dt>

**TotalPages**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de páginas necesarias para completar el trabajo. Este valor puede ser 0 (cero) si el trabajo de impresión no contiene información de delimitación de página.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora en la que el trabajo no es válido o debe detenerse.

Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase de **Win32 \_ PrintJob** se deriva del [**\_ trabajo de CIM**](cim-job.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se describe cómo recuperar estadísticas de trabajos de impresora desde instancias de **\_ PrintJob de Win32**.


```VB
Set PrintJobSet = GetObject("winmgmts:").InstancesOf ("Win32_PrintJob")

If (PrintJobSet.Count = 0) Then WScript.Echo "No print jobs!"
for each PrintJob in PrintJobSet
 WScript.Echo PrintJob.Name
 WScript.Echo PrintJob.JobId
 WScript.Echo PrintJob.Status
 WScript.Echo PrintJob.TotalPages
 Wscript.Echo ""
next
```



El siguiente ejemplo de código Perl describe cómo recuperar estadísticas de trabajos de impresora de instancias **de \_ PrintJob de Win32**.


```
use strict;
use Win32::OLE;

close (STDERR);

my ($PrintJobset, $PrintJob);
eval {$PrintJobset = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 InstancesOf ("Win32_PrintJob") };
if (!$@ && defined $PrintJobset)
{
 if ($PrintJobset->{Count} == 0 ) 
 {
  print "\nNo print jobs!\n";
 }

 foreach $PrintJob (in $PrintJobset)
 {
  print $PrintJob->{Name} , "\n";
  print $PrintJob->{JobId} , "\n";
  print $PrintJob->{Status} , "\n";
  print $PrintJob->{TotalPages} , "\n";
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ printer. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Trabajo de CIM \_**](./cim-job.md)
</dt> <dt>

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
