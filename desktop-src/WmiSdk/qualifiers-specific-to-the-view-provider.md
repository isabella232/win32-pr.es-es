---
description: A continuación se enumeran los calificadores que se usan para definir las clases de proveedor de vistas.
ms.assetid: 31a6af2d-33da-44f2-86d7-c467dd2f3e00
ms.tgt_platform: multiple
title: Calificadores específicos del proveedor de vistas
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 76f28e4ba3433c168e1d0bf86887ee93df953444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278205"
---
# <a name="qualifiers-specific-to-the-view-provider"></a>Calificadores específicos del proveedor de vistas

A continuación se enumeran los calificadores que se usan para definir las clases de proveedor de vistas.

> [!Note]  
> La clase de proveedor de vista solo admite nombres NetBIOS cuando se usan referencias remotas. Si usa una dirección IP o un nombre DNS en una referencia remota, la conexión produce un error 0x800706ba.

 

<dt>

<span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Directo**
</dt> <dd>

Tipo de datos: **booleano**

Se utiliza con las propiedades de la Asociación de vista para evitar que las referencias de asociación se asignen a una referencia de vista.

En el ejemplo siguiente se define la propiedad **GroupComponent** como una referencia de asociación que no está asignada en la referencia de la vista.


```mof
[Direct, key, PropertySources
{"GroupComponent"}]
```



</dd> <dt>

<span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**
</dt> <dd>

Tipo de datos: **booleano**

Valor predeterminado para una propiedad de clase de vista basada en una propiedad de clase de origen con un valor predeterminado diferente. La clase de origen subyacente está implícita en la vista.

Por ejemplo, la clase de origen [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) tiene una propiedad [booleana](boolean.md) **RunRepeatedly** que indica si el trabajo se va a llevar a cabo periódicamente o solo una vez. El valor predeterminado de **RunRepeatedly** no es true para **Win32 \_ ScheduledJob**, pero es true para la clase de vista.


```mof
#pragma namespace("\\\\.\\root\\ns_view")
[Union,
ViewSources{"select * from Win32_ScheduledJob where RunRepeatedly=True"},
ViewSpaces{"\\\\.\\root\\cimv2"},
dynamic,provider("MS_VIEW_INSTANCE_PROVIDER")]
Class View_PeriodicJob
{
 [key, PropertySources{"JobId"}]
 uint32 JobId;
 [PropertySources{"Command"}]
 string Command;
 [HiddenDefault,PropertySources{"RunRepeatedly"}]
 boolean Repeat = True;
};
```



</dd> <dt>

<span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**Joinon**
</dt> <dd>

Tipo de datos: **cadena**

Define cómo se unen las instancias de clase de origen en las clases de vista de combinación. En el ejemplo siguiente se muestra cómo utilizar el calificador **join** para combinar dos clases de origen.


```mof
JoinOn("Win32Perf_RawProcess.IDProcess = Win32Perf_RawThread.IDProcess")
```



</dd> <dt>

<span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Método de origen que se va a ejecutar para el método de vista. Para obtener una sintaxis similar, vea [calificador PropertySources](propertysources-qualifier.md). La Signatura del método debe coincidir exactamente con la signatura de la clase de origen. Copie la firma del método del archivo MOF que define la clase de origen. En el ejemplo siguiente se define un método del método [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) de [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):


```mof
[implemented, MethodSource
{"ClearEventlog"}]
  uint32   VClearEventlog([in] string ArchiveFileName);
```



Este calificador solo es válido cuando se usa con vistas Union.

</dd> <dt>

<span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)
</dt> <dd>

Tipo de datos: **cadena**

Consulta WQL para filtrar las instancias una vez Unidas en una clase de combinación.

</dd> <dt>

<span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Propiedades de origen desde las que una propiedad de clase de vista obtiene datos.

</dd> <dt>

<span id="Union"></span><span id="union"></span><span id="UNION"></span>**Unión**
</dt> <dd>

Tipo de datos: **booleano**

Indica si se está definiendo una clase Union. Las vistas Union contienen instancias basadas en la Unión de instancias de origen. Por ejemplo, podría declarar lo siguiente:


```mof
Union, ViewSources{"SELECT Handle, Name, CreationDate FROM Win32_Process", 
                   "SELECT Caption, Name, ProcessHandle FROM Win32_Thread"}.
```



</dd> <dt>

<span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Conjunto de consultas de lenguaje de consulta de WMI (WQL) que definen las instancias de origen y las propiedades utilizadas en una clase de vista específica. La correspondencia posicional de todos los calificadores de matriz es importante.

</dd> <dt>

<span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)
</dt> <dd>

Tipo de datos: **matriz de cadenas**

Espacios de nombres donde se encuentran las instancias de origen.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



 

