---
description: Representa un trabajo de impresión generado por una Windows aplicación. Cualquier unidad de trabajo generada por el comando de impresión de una aplicación que se ejecuta en un equipo que se ejecuta en un sistema operativo Windows es un descendiente o miembro de esta clase.
ms.assetid: d884acba-e1b2-4d24-9b55-15d175a163d9
ms.tgt_platform: multiple
title: Win32_PrintJob clase
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
ms.openlocfilehash: 62a8f09d6b96e12d75b30c80e5553d3138bcb342f7ca06b53920d897aaa51c57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971855"
---
# <a name="win32_printjob-class"></a>Clase PrintJob de Win32 \_

La **clase \_ WMI PrintJob** [de](../wmisdk/retrieving-a-class.md) Win32 representa un trabajo de impresión generado por una Windows aplicación. Cualquier unidad de trabajo generada por el comando de impresión de una aplicación que se ejecuta en un equipo que se ejecuta en un sistema operativo Windows es un descendiente o miembro de esta clase.

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

La **clase \_ PrintJob de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ PrintJob de Win32** tiene estos métodos.



| Método                                                  | Descripción                       |
|:--------------------------------------------------------|:----------------------------------|
| [**Pausar**](pause-method-in-class-win32-printjob.md)   | Pausa un trabajo de impresión.<br/>    |
| [**Reanudar**](resume-method-in-class-win32-printjob.md) | Continúa un trabajo de impresión.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ PrintJob de Win32** tiene estas propiedades.

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

**Color**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que indica si el documento se imprime en color o monocromo. Algunas impresoras de color tienen la capacidad de imprimir con un color negro verdadero en lugar de una combinación de amarillo, cian y rojo. El negro verdadero suele crear texto más oscuro y más nítido para los documentos. Esta opción solo es útil para impresoras de color que admiten la impresión en negro verdadero.

Los valores son:

<dl><span id="_Color_"></span><span id="_color_"></span><span id="_COLOR_"></span><dt>

**"Color"**
</dt><span id="_Monochrome_"></span><span id="_monochrome_"></span><span id="_MONOCHROME_"></span><dt>

**"Monocromo"**
</dt> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Formato de los datos de este trabajo de impresión. Esto indica al controlador de impresora que traduzca los datos (texto genérico, PostScript o PCL) antes de imprimirlos, o imprimirlos en un formato sin formato (para gráficos e imágenes).

Ejemplo: "TEXT"

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

**Documento**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del trabajo de impresión. El usuario ve este nombre al ver documentos que están esperando ser impresos.

Ejemplo: "Microsoft Word - Review.doc"

</dd> <dt>

**DriverName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del controlador de impresora usado para el trabajo de impresión.

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Período de tiempo durante el que se ha estado ejecutando el trabajo.

Esta propiedad se hereda del [**trabajo \_ cim**](cim-job.md).

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

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Fecha de instalación")
</dt> </dl>

Indica cuándo se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**JobId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de identificador del trabajo. Lo usan otros métodos como identificador de un trabajo que se cola en la impresora.

</dd> <dt>

**Estado del trabajo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que representa el estado del trabajo.

Esta propiedad se hereda del [**trabajo \_ cim**](cim-job.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nombre")
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasifica, esta propiedad se puede invalidar para que sea una propiedad de clave.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Notificar**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Se notifica al usuario tras la finalización o el error del trabajo.

Esta propiedad se hereda del [**trabajo \_ cim**](cim-job.md).

</dd> <dt>

**Propietario**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Usuario que envió el trabajo.

Esta propiedad se hereda del [**trabajo \_ cim**](cim-job.md).

</dd> <dt>

**PagesPrinted**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de páginas que se imprimen. Este valor puede ser 0 (cero) si el trabajo de impresión no contiene información delimitada por páginas.

</dd> <dt>

**PaperLength**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
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

Tamaño del papel usado para imprimir el trabajo. El valor es uno de los posibles tamaños de papel para la impresora especificada en la **propiedad PaperSizesSupported** de [**la clase Printer \_ de Win32.**](win32-printer.md)

</dd> <dt>

**PaperWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
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

Parámetros opcionales que se enviarán al procesador de impresión. Para obtener más información, vea la **propiedad PrintProcessor.**

</dd> <dt>

**PrintProcessor**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Servicio de procesador de impresión que se usa para procesar el trabajo de impresión. Un procesador de impresora funciona junto con el controlador de impresora para proporcionar una traducción adicional de los datos de impresora para la impresora y también se puede usar para proporcionar opciones especiales, como una página de título para el trabajo.

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Importancia de la ejecución de un trabajo.

Esta propiedad se hereda del [**trabajo \_ cim**](cim-job.md).

</dd> <dt>

**Tamaño**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (bytes)
</dt> </dl>

Tamaño del trabajo de impresión.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora a la que comenzó el trabajo.

Esta propiedad se hereda del [**trabajo \_ cim**](cim-job.md).

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

**Máscara de estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Mapa de bits de los posibles estados relacionados con este trabajo de impresión.

<dt>

1 (0x1)
</dt> <dd>

En pausa

</dd> <dt>

2 (0x2)
</dt> <dd>

Error

</dd> <dt>

4 (0x4)
</dt> <dd>

Eliminando

</dd> <dt>

8 (0x8)
</dt> <dd>

Cola

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

Papeleo

</dd> <dt>

128 (0x80)
</dt> <dd>

Impreso

</dd> <dt>

256 (0x100)
</dt> <dd>

Deleted

</dd> <dt>

512 (0x200)
</dt> <dd>

Blocked \_ DevQ

</dd> <dt>

1024 (0x400)
</dt> <dd>

Solicitud de \_ \_ intervención del usuario

</dd> <dt>

2048 (0x800)
</dt> <dd>

Reiniciar

</dd> </dl>

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora a la que se envió el trabajo.

Esta propiedad se hereda del [**trabajo \_ cim**](cim-job.md).

</dd> <dt>

**TotalPages**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de páginas necesarias para completar el trabajo. Este valor puede ser 0 (cero) si el trabajo de impresión no contiene información delimitada por páginas.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora en la que el trabajo no es válido o se debe detener.

Esta propiedad se hereda del [**trabajo \_ cim**](cim-job.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ PrintJob de Win32** se deriva del [**trabajo \_ CIM**](cim-job.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se describe cómo recuperar estadísticas de trabajos de impresora de instancias de **\_ PrintJob de Win32.**


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



En el siguiente ejemplo de código perl se describe cómo recuperar estadísticas de trabajos de impresora de instancias de **\_ PrintJob de Win32.**


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
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Trabajo \_ cim**](./cim-job.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
