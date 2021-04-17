---
description: El objeto SWbemDateTime es un objeto auxiliar para analizar y establecer valores de fecha y hora de Modelo de información común (CIM).
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.tgt_platform: multiple
title: Objeto SWbemDateTime (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime
- ISWbemDateTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 65f3f9836b52693e3f74bac5cfd94553e02d7bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706457"
---
# <a name="swbemdatetime-object"></a>Objeto SWbemDateTime

El objeto **SWbemDateTime** es un objeto auxiliar para analizar y establecer valores de [fecha y hora](datetime.md) de modelo de información común (CIM). Desempeña un papel similar a [**SWbemObjectPath**](swbemobjectpath.md), que proporciona ayuda para dar formato e interpretar las rutas de acceso a los objetos. Puede usar la llamada [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript para crear el objeto **SWbemDateTime** .

Un objeto **SWbemDateTime** se puede inicializar a partir de y debe tener el formato de los valores **VT \_ Date** o **FILETIME** mediante métodos en el objeto. Con las propiedades del objeto, el valor se puede analizar en el año del componente, mes, día, hora, minutos, segundos o microsegundos. Se puede dar formato al objeto **SWbemDateTime** en valores locales o de hora universal coordinada (UTC). Para obtener más información, vea [formato de fecha y hora](date-and-time-format.md).

**SWbemDateTime** es el único objeto de scripting de instrumental de administración de Windows (WMI) que está marcado como seguro para la inicialización y los scripts que se ejecutan en páginas HTML en Internet Explorer.

## <a name="members"></a>Miembros

El objeto **SWbemDateTime** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **SWbemDateTime** tiene estos métodos.



| Método                                           | Descripción                                                                                                          |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**GetFileTime**](swbemdatetime-getfiletime.md) | Convierte una fecha y hora de **FILETIME** , expresadas como **BSTR**, en [un formato de fecha y](datetime.md) hora de WMI.<br/> |
| [**Getvardate (**](swbemdatetime-getvardate.md)   | Convierte un valor de fecha y hora con formato [DateTime](datetime.md) de WMI en una **\_ fecha de VT**.<br/>                  |
| [**SetFileTime**](swbemdatetime-setfiletime.md) | Convierte un formato [DateTime](datetime.md) de WMI en una fecha y hora de **FILETIME** , expresadas como **BSTR**.<br/>  |
| [**SetVarDate**](swbemdatetime-setvardate.md)   | Convierte una fecha y hora con formato de **\_ fecha VT** en un [valor DateTime](datetime.md)de WMI.<br/>                        |



 

### <a name="properties"></a>Propiedades

El objeto **SWbemDateTime** tiene estas propiedades.



| Propiedad                                                                        | Tipo de acceso           | Descripción                                                                                                                     |
|:--------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**Diariamente**](swbemdatetime-day.md)<br/>                                     | Lectura/escritura<br/> | El componente de día de un valor [DateTime](datetime.md) de CIM.<br/>                                                           |
| [**DaySpecified**](swbemdatetime-dayspecified.md)<br/>                   | Lectura/escritura<br/> | Indica si el día se especifica o se deja como carácter comodín.<br/>                                                        |
| [**Hours**](swbemdatetime-hours.md)<br/>                                 | Lectura/escritura<br/> | Horas del componente de día de un valor [DateTime](datetime.md) de CIM.<br/>                                              |
| [**HoursSpecified**](swbemdatetime-hoursspecified.md)<br/>               | Lectura/escritura<br/> | Indica si la hora se especifica o se deja como un carácter comodín.<br/>                                                       |
| [**IsInterval**](swbemdatetime-isinterval.md)<br/>                       | Lectura/escritura<br/> | Indica que al menos un componente de la [fecha y hora](datetime.md) de CIM representa un intervalo en lugar de una fecha.<br/> |
| [**Microsegundos**](swbemdatetime-microseconds.md)<br/>                   | Lectura/escritura<br/> | Componente de microsegundos de un valor [DateTime](datetime.md) de CIM.<br/>                                                  |
| [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)<br/> | Lectura/escritura<br/> | Indica si el componente de microsegundos se especifica o se deja como carácter comodín.<br/>                                     |
| [**Minutos**](swbemdatetime-minutes.md)<br/>                             | Lectura/escritura<br/> | El componente de minutos de un valor [DateTime](datetime.md) de CIM.<br/>                                                       |
| [**MinutesSpecified**](swbemdatetime-minutesspecified.md)<br/>           | Lectura/escritura<br/> | Indica si el componente de minutos se especifica o se deja como carácter comodín.<br/>                                          |
| [**Mensuales**](swbemdatetime-month.md)<br/>                                 | Lectura/escritura<br/> | El componente de mes de un valor [DateTime](datetime.md) de CIM.<br/>                                                         |
| [**MonthSpecified**](swbemdatetime-monthspecified.md)<br/>               | Lectura/escritura<br/> | Indica si el mes se especifica o se deja como carácter comodín.<br/>                                                      |
| [**Segundos**](swbemdatetime-seconds.md)<br/>                             | Lectura/escritura<br/> | Componente de segundos de un valor [DateTime](datetime.md) de CIM.<br/>                                                       |
| [**SecondsSpecified**](swbemdatetime-secondsspecified.md)<br/>           | Lectura/escritura<br/> | Indica si el componente de segundos se especifica o se deja como carácter comodín.<br/>                                          |
| [**UTC**](swbemdatetime-utc.md)<br/>                                     | Lectura/escritura<br/> | Componente UTC de un valor [DateTime](datetime.md) de CIM.<br/>                                                           |
| [**UTCSpecified**](swbemdatetime-utcspecified.md)<br/>                   | Lectura/escritura<br/> | Indica si el componente UTC se especifica o se deja como carácter comodín.<br/>                                              |
| [**Value**](swbemdatetime-value.md)<br/>                                 | Lectura/escritura<br/> | El valor de [fecha y hora](datetime.md) de CIM completo.<br/>                                                                         |
| [**Anual**](swbemdatetime-year.md)<br/>                                   | Lectura/escritura<br/> | Componente de año de un valor [DateTime](datetime.md) de CIM.<br/>                                                          |
| [**YearSpecified**](swbemdatetime-yearspecified.md)<br/>                 | Lectura/escritura<br/> | Indica si se ha especificado o no el año como carácter comodín.<br/>                                                |



 

## <a name="remarks"></a>Observaciones

WMI registra las marcas de tiempo en el formato de coordenadas de hora universal (UTC). UTC no es el formato que usan la mayoría de los desarrolladores y administradores de ti. Por lo tanto, un problema común es determinar cómo traducir la hora UTC a algo más legible. Para obtener más información sobre cómo trabajar con UTC, vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md) y [trabajar con fechas y horas mediante WMI](/previous-versions/tn-archive/ee198928(v=technet.10)). También puede leer la información [sobre la TI sobre el tiempo (Oh, y sobre las fechas)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) y [cómo se puede restar un número especificado de días a partir de un valor UTC](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) . entradas de blog para obtener información adicional.

Cualquier campo numérico puede tener un valor comodín si la propiedad [**IsInterval**](swbemdatetime-isinterval.md) está establecida en **false**. Los campos con valores comodín contienen asteriscos en todo el campo.

Cada propiedad, por ejemplo [**Day**](swbemdatetime-day.md), tiene un valor booleano especificado correspondiente, como [**DaySpecified**](swbemdatetime-dayspecified.md). Cuando **DaySpecified** es **false**, el valor se interpreta como un intervalo en lugar de un número entre 01 y 31. Si se usa un intervalo en cualquier parte del valor [DateTime](datetime.md) de CIM, [**IsInterval**](swbemdatetime-isinterval.md) también se establece en **true**. El valor predeterminado es que un valor DateTime de CIM contenga una fecha en lugar de uno o más intervalos.

Por ejemplo, si [**SWbemDateTime. DaySpecified**](swbemdatetime-dayspecified.md) es **true**, [**SWbemDateTime. Value**](swbemdatetime-value.md) incluye el valor actual de [**SWbemDateTime. Day**](swbemdatetime-day.md); de lo contrario, es un valor comodín. La propiedad [**IsInterval**](swbemdatetime-isinterval.md) es **false** en cualquier caso.

## <a name="examples"></a>Ejemplos

En el ejemplo de código de script siguiente se muestra cómo usar un objeto **SWbemDateTime** para analizar un valor de propiedad DateTime leído del repositorio WMI, la propiedad **InstallDate** en el sistema [**\_ operativo Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).


```VB
' Create a new datetime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")

' Retrieve a WMI object that contains a datetime value.
for each os in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

    ' The InstallDate property is a CIM_DATETIME. 
    MsgBox os.InstallDate
    dateTime.Value = os.InstallDate

    ' Display the year of installation.
    MsgBox "This OS was installed in the year " & dateTime.Year

    ' Display the installation date using the VT_DATE format.
    MsgBox "Full installation date (VT_DATE format) is " _
    & dateTime.GetVarDate

    ' Display the installation date using the FILETIME format.
    MsgBox "Full installation date (FILETIME format) is " _
    & dateTime.GetFileTime 
next
Set datetime = Nothing
```



En el ejemplo siguiente se muestra cómo crear un objeto **SWbemDateTime** , cómo almacenar un valor de fecha en el objeto, cómo mostrar la fecha como hora universal coordinada (UTC) y cómo almacenar el valor en una clase y propiedad recién creadas. Para obtener más información sobre la constante **wbemCimtypeDatetime**, vea [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).


```VB
' Create an SWbemDateTime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
' Set the value 
Const wbemCimTypeDatetime = 101

' Construct a datetime value using the intrinsic VBScript CDate
' function interpreting this as a local date/time in
' the Pacific time zone (-8 hrs GMT). Convert to CIM datetime
' using SetVarDate method. The year defaults to current year.
dateTime.SetVarDate (CDate ("January 20 11:56:32"))

' The value in dateTime displays as 
' 20000120195632.000000-480. This is the equivalent time
' in GMT with the specified offset for PST of -8 hrs.
MsgBox "CIM datetime " & dateTime

' The value now displays as B=0/2000 11:56:32 AM because the
' parameter contains the default TRUE value causing the value to be
' interpreted as a local time.
MsgBox "Local datetime " & dateTime.GetVarDate ()

' The value now displays as B=0/2000 7:56:32 PM because the
' parameter value is FALSE, which indicates a GMT time.
' non-local time.
MsgBox "Datetime in GMT " & dateTime.GetVarDate (false)

' Create a new class and add a DateTime property value.
' SWbemServices.Get returns an empty SWbemObject
' which can become a new class. SWbemObject.Path_ returns an
' SWbemObjectPath object. 
set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "NewClass"

' Add a new property named "InterestingDate" to the NewObject class
' and define its datatype as a CIM datetime value.
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value of the SWbemDateTime object in the InterestingDate
' property.
NewObject.InterestingDate = dateTime.Value
MsgBox "Datetime in new object " & NewObject.InterestingDate

' Write the new class (named "NewClass") containing
' the SWbemDateTime object to the repository.
NewObject.Put_
WScript.Echo "NewClass is now in WMI repository"

' Clean up the example by deleting the new class from the repository
NewObject.Delete_
```



En el ejemplo de código de script siguiente se muestra cómo usar un objeto **SWbemDateTime** para modificar un valor de intervalo en una propiedad que se lee desde el repositorio WMI.


```VB
' Construct an interval value of 100 days, 1 hour, and 3 seconds.
dateTime.IsInterval = true 
dateTime.Day = 100
dateTime.Hours = 1
dateTime.Seconds = 3

' The datetime displays as 00000100010003.000000:000.
MsgBox "Constructed interval value " & datetime

' Retrieve an empty WMI object and add a datetime property. 
Const wbemCimTypeDatetime = 101
Set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "Empty"
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value in the property and update. 
NewObject.InterestingDate = dateTime.Value
MsgBox "NewObject.InterestingDate = " & NewObject.InterestingDate

' Write the new SWbemDateTime object to the repository.
NewObject.Put_

' Delete the object.
NewObject.Delete_
```



En el ejemplo de código de script siguiente se muestra cómo usar un objeto **SWbemDate** para leer un valor de **FILETIME** .


```VB
' Create a new datetime object.
Set datetime = CreateObject("WbemScripting.SWbemDateTime")

' Set from a FILETIME value (non-local).
' Assume a timezone -7 hrs. GMT.
MsgBox "FILETIME value " & "126036951652030000"
datetime.SetFileTime "126036951652030000", false

' Displays as 5/24/2000 7:26:05 PM.
MsgBox "GMT time " & dateTime.GetVarDate   

' Set from a FILETIME value (local).
datetime.SetFileTime "126036951652030000"

' Displays as 5/25/2000 2:26:05 AM.
MsgBox "Same value in local time " & dateTime.GetVarDate
Set datetime = Nothing
```



El siguiente código de PowerShell crea una instancia de un objeto SWbemDateTime, recupera la fecha de instalación del sistema operativo y convierte la fecha a un formato diferente.


```PowerShell
# Create swbemdatetime object
$datetime = New-Object -ComObject WbemScripting.SWbemDateTime

#  Get OS installation time and assign to datetime object
$os = Get-WmiObject -Class Win32_OperatingSystem
$dateTime.Value = $os.InstallDate

# Now display the time
"This OS was installed in the year {0}"           -f $dateTime.Year
"Full installation date (VT_DATE format) is {0}"  -f $dateTime.GetVarDate()
"Full installation date (FILETIME format) is {0}" -f $dateTime.GetFileTime() 
```



El siguiente código de PowerShell convierte el código en un formato listo para que lo consuma un proveedor CIM.


```PowerShell
 $time = (Get-Date)
 $objScriptTime = New-Object -ComObject WbemScripting.SWbemDateTime
 $objScriptTime.SetVarDate($time)
 $cimTime = $objScriptTime.Value
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | \_ISWBEMDATETIME IID<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dt>

[DATETIME](datetime.md)
</dt> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> </dl>

 

