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
# <a name="qualifiers-specific-to-the-view-provider"></a><span data-ttu-id="5ae8c-103">Calificadores específicos del proveedor de vistas</span><span class="sxs-lookup"><span data-stu-id="5ae8c-103">Qualifiers Specific to the View Provider</span></span>

<span data-ttu-id="5ae8c-104">A continuación se enumeran los calificadores que se usan para definir las clases de proveedor de vistas.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-104">The following lists the qualifiers use to define View Provider classes.</span></span>

> [!Note]  
> <span data-ttu-id="5ae8c-105">La clase de proveedor de vista solo admite nombres NetBIOS cuando se usan referencias remotas.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-105">The View provider class only supports NetBIOS names when using remote references.</span></span> <span data-ttu-id="5ae8c-106">Si usa una dirección IP o un nombre DNS en una referencia remota, la conexión produce un error 0x800706ba.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-106">If you use an IP address or a DNS name in a remote reference, then the connection fails with a 0x800706ba error.</span></span>

 

<dt>

<span data-ttu-id="5ae8c-107"><span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Directo**</span><span class="sxs-lookup"><span data-stu-id="5ae8c-107"><span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Direct**</span></span>
</dt> <dd>

<span data-ttu-id="5ae8c-108">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5ae8c-108">Data type: **boolean**</span></span>

<span data-ttu-id="5ae8c-109">Se utiliza con las propiedades de la Asociación de vista para evitar que las referencias de asociación se asignen a una referencia de vista.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-109">Used with view association properties to prevent association references from being mapped to a view reference.</span></span>

<span data-ttu-id="5ae8c-110">En el ejemplo siguiente se define la propiedad **GroupComponent** como una referencia de asociación que no está asignada en la referencia de la vista.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-110">The following example defines the property **GroupComponent** as an association reference that is not mapped in the view reference.</span></span>


```mof
[Direct, key, PropertySources
{"GroupComponent"}]
```



</dd> <dt>

<span data-ttu-id="5ae8c-111"><span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**</span><span class="sxs-lookup"><span data-stu-id="5ae8c-111"><span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**</span></span>
</dt> <dd>

<span data-ttu-id="5ae8c-112">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5ae8c-112">Data type: **boolean**</span></span>

<span data-ttu-id="5ae8c-113">Valor predeterminado para una propiedad de clase de vista basada en una propiedad de clase de origen con un valor predeterminado diferente.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-113">Default value for a view class property based on a source class property with a different default value.</span></span> <span data-ttu-id="5ae8c-114">La clase de origen subyacente está implícita en la vista.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-114">The underlying source class is implied by the view.</span></span>

<span data-ttu-id="5ae8c-115">Por ejemplo, la clase de origen [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) tiene una propiedad [booleana](boolean.md) **RunRepeatedly** que indica si el trabajo se va a llevar a cabo periódicamente o solo una vez.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-115">For example, the source class [**Win32\_ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) has a [boolean](boolean.md) property **RunRepeatedly** that indicates whether the job is to be carried out periodically or one time only.</span></span> <span data-ttu-id="5ae8c-116">El valor predeterminado de **RunRepeatedly** no es true para **Win32 \_ ScheduledJob**, pero es true para la clase de vista.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-116">The default value of **RunRepeatedly** is not True for **Win32\_ScheduledJob**, but is True for the view class.</span></span>


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

<span data-ttu-id="5ae8c-117"><span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**Joinon**</span><span class="sxs-lookup"><span data-stu-id="5ae8c-117"><span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**JoinOn**</span></span>
</dt> <dd>

<span data-ttu-id="5ae8c-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5ae8c-118">Data type: **string**</span></span>

<span data-ttu-id="5ae8c-119">Define cómo se unen las instancias de clase de origen en las clases de vista de combinación.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-119">Defines how source class instances are joined in join view classes.</span></span> <span data-ttu-id="5ae8c-120">En el ejemplo siguiente se muestra cómo utilizar el calificador **join** para combinar dos clases de origen.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-120">The following example shows how to use the **JoinOn** qualifier to join two source classes.</span></span>


```mof
JoinOn("Win32Perf_RawProcess.IDProcess = Win32Perf_RawThread.IDProcess")
```



</dd> <dt>

<span data-ttu-id="5ae8c-121"><span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**</span><span class="sxs-lookup"><span data-stu-id="5ae8c-121"><span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**</span></span>
</dt> <dd>

<span data-ttu-id="5ae8c-122">Tipo de datos: **matriz de cadenas**</span><span class="sxs-lookup"><span data-stu-id="5ae8c-122">Data type: **string array**</span></span>

<span data-ttu-id="5ae8c-123">Método de origen que se va a ejecutar para el método de vista.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-123">Source method to execute for the view method.</span></span> <span data-ttu-id="5ae8c-124">Para obtener una sintaxis similar, vea [calificador PropertySources](propertysources-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="5ae8c-124">For similar syntax, see [PropertySources Qualifier](propertysources-qualifier.md).</span></span> <span data-ttu-id="5ae8c-125">La Signatura del método debe coincidir exactamente con la signatura de la clase de origen.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-125">The signature of the method must match the signature of the source class exactly.</span></span> <span data-ttu-id="5ae8c-126">Copie la firma del método del archivo MOF que define la clase de origen.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-126">Copy the method signature from the MOF file that defines the source class.</span></span> <span data-ttu-id="5ae8c-127">En el ejemplo siguiente se define un método del método [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) de [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="5ae8c-127">The example below defines a method from the [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) method of [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):</span></span>


```mof
[implemented, MethodSource
{"ClearEventlog"}]
  uint32   VClearEventlog([in] string ArchiveFileName);
```



<span data-ttu-id="5ae8c-128">Este calificador solo es válido cuando se usa con vistas Union.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-128">This qualifier is only valid when it is used with union views.</span></span>

</dd> <dt>

<span data-ttu-id="5ae8c-129"><span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="5ae8c-129"><span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="5ae8c-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5ae8c-130">Data type: **string**</span></span>

<span data-ttu-id="5ae8c-131">Consulta WQL para filtrar las instancias una vez Unidas en una clase de combinación.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-131">WQL query to filter instances after they have been joined in a join class.</span></span>

</dd> <dt>

<span data-ttu-id="5ae8c-132"><span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="5ae8c-132"><span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="5ae8c-133">Tipo de datos: **matriz de cadenas**</span><span class="sxs-lookup"><span data-stu-id="5ae8c-133">Data type: **string array**</span></span>

<span data-ttu-id="5ae8c-134">Propiedades de origen desde las que una propiedad de clase de vista obtiene datos.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-134">Source properties from which a view class property gets data.</span></span>

</dd> <dt>

<span data-ttu-id="5ae8c-135"><span id="Union"></span><span id="union"></span><span id="UNION"></span>**Unión**</span><span class="sxs-lookup"><span data-stu-id="5ae8c-135"><span id="Union"></span><span id="union"></span><span id="UNION"></span>**Union**</span></span>
</dt> <dd>

<span data-ttu-id="5ae8c-136">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5ae8c-136">Data type: **boolean**</span></span>

<span data-ttu-id="5ae8c-137">Indica si se está definiendo una clase Union.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-137">Indicates whether you are defining a union class.</span></span> <span data-ttu-id="5ae8c-138">Las vistas Union contienen instancias basadas en la Unión de instancias de origen.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-138">Union views contain instances based on the union of source instances.</span></span> <span data-ttu-id="5ae8c-139">Por ejemplo, podría declarar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5ae8c-139">For example, you might declare the following:</span></span>


```mof
Union, ViewSources{"SELECT Handle, Name, CreationDate FROM Win32_Process", 
                   "SELECT Caption, Name, ProcessHandle FROM Win32_Thread"}.
```



</dd> <dt>

<span data-ttu-id="5ae8c-140"><span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="5ae8c-140"><span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="5ae8c-141">Tipo de datos: **matriz de cadenas**</span><span class="sxs-lookup"><span data-stu-id="5ae8c-141">Data type: **string array**</span></span>

<span data-ttu-id="5ae8c-142">Conjunto de consultas de lenguaje de consulta de WMI (WQL) que definen las instancias de origen y las propiedades utilizadas en una clase de vista específica.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-142">Set of WMI Query Language (WQL) queries that define the source instances and properties used in a specific view class.</span></span> <span data-ttu-id="5ae8c-143">La correspondencia posicional de todos los calificadores de matriz es importante.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-143">Positional correspondence of all the array qualifiers is important.</span></span>

</dd> <dt>

<span data-ttu-id="5ae8c-144"><span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="5ae8c-144"><span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="5ae8c-145">Tipo de datos: **matriz de cadenas**</span><span class="sxs-lookup"><span data-stu-id="5ae8c-145">Data type: **string array**</span></span>

<span data-ttu-id="5ae8c-146">Espacios de nombres donde se encuentran las instancias de origen.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-146">Namespaces where the source instances are located.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ae8c-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ae8c-147">Requirements</span></span>



| <span data-ttu-id="5ae8c-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ae8c-148">Requirement</span></span> | <span data-ttu-id="5ae8c-149">Value</span><span class="sxs-lookup"><span data-stu-id="5ae8c-149">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5ae8c-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ae8c-150">Minimum supported client</span></span><br/> | <span data-ttu-id="5ae8c-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ae8c-151">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5ae8c-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ae8c-152">Minimum supported server</span></span><br/> | <span data-ttu-id="5ae8c-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ae8c-153">Windows Server 2008</span></span><br/> |



 

