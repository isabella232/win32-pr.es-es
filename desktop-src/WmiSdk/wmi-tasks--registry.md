---
description: Tareas de WMI para el registro crear y modificar claves y valores del registro. Para ver otros ejemplos, vea el ScriptCenter de TechNet en https://www.microsoft.com/technet .
ms.assetid: 0785189e-9638-4776-8414-1414d7b02524
ms.tgt_platform: multiple
title: 'Tareas WMI: registro'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df6ae73d41c9cbfd6cd303b72e1b9207f3191c85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659947"
---
# <a name="wmi-tasks-registry"></a><span data-ttu-id="02dc0-104">Tareas WMI: registro</span><span class="sxs-lookup"><span data-stu-id="02dc0-104">WMI Tasks: Registry</span></span>

<span data-ttu-id="02dc0-105">Tareas de WMI para el registro crear y modificar claves y valores del registro.</span><span class="sxs-lookup"><span data-stu-id="02dc0-105">WMI tasks for the registry create and modify registry keys and values.</span></span> <span data-ttu-id="02dc0-106">Para ver otros ejemplos, vea el ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="02dc0-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="02dc0-107">Los ejemplos de scripts que se muestran en este tema obtienen datos solo del equipo local.</span><span class="sxs-lookup"><span data-stu-id="02dc0-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="02dc0-108">Para obtener más información acerca de cómo usar el script para obtener datos de equipos remotos, consulte [conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="02dc0-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="02dc0-109">En el procedimiento siguiente se describe cómo ejecutar un script.</span><span class="sxs-lookup"><span data-stu-id="02dc0-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="02dc0-110">**Para ejecutar un script**</span><span class="sxs-lookup"><span data-stu-id="02dc0-110">**To run a script**</span></span>

1.  <span data-ttu-id="02dc0-111">Copie el código y guárdelo en un archivo con la extensión. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="02dc0-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="02dc0-112">Asegúrese de que el editor de texto no agrega una extensión. txt al archivo.</span><span class="sxs-lookup"><span data-stu-id="02dc0-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="02dc0-113">Abra una ventana del símbolo del sistema y navegue hasta el directorio en el que guardó el archivo.</span><span class="sxs-lookup"><span data-stu-id="02dc0-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="02dc0-114">Escriba **cscript filename.vbs** en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="02dc0-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="02dc0-115">Si no puede obtener acceso a un registro de eventos, compruebe si está ejecutando desde un símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="02dc0-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="02dc0-116">Algunos registros de eventos, como el registro de eventos de seguridad, pueden estar protegidos por controles de acceso de usuario (UAC).</span><span class="sxs-lookup"><span data-stu-id="02dc0-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="02dc0-117">De forma predeterminada, cscript muestra la salida de un script en la ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="02dc0-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="02dc0-118">Dado que los scripts de WMI pueden generar grandes cantidades de resultados, es posible que desee redirigir la salida a un archivo.</span><span class="sxs-lookup"><span data-stu-id="02dc0-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="02dc0-119">Escriba **cscript filename.vbs > outfile.txt** en el símbolo del sistema para redirigir la salida del script de *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="02dc0-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="02dc0-120">En la tabla siguiente se enumeran ejemplos de scripts que se pueden usar para obtener distintos tipos de datos del equipo local.</span><span class="sxs-lookup"><span data-stu-id="02dc0-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-121">Cómo...</span><span class="sxs-lookup"><span data-stu-id="02dc0-121">How do I...</span></span></th>
<th><span data-ttu-id="02dc0-122">Clases o métodos WMI</span><span class="sxs-lookup"><span data-stu-id="02dc0-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02dc0-123">... ¿leer los valores de clave del registro mediante WMI?</span><span class="sxs-lookup"><span data-stu-id="02dc0-123">...read registry key values using WMI?</span></span></td>
<td><span data-ttu-id="02dc0-124">Use la clase <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , que se encuentra en el espacio de nombres root\default.</span><span class="sxs-lookup"><span data-stu-id="02dc0-124">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace.</span></span> <span data-ttu-id="02dc0-125">No puede obtener ninguna instancia de esta clase porque el <a href="/previous-versions/windows/desktop/regprov/system-registry-provider">proveedor del registro del sistema</a> es solo un método y un proveedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="02dc0-125">You cannot get any instances of this class because the <a href="/previous-versions/windows/desktop/regprov/system-registry-provider">System Registry Provider</a> is a method and event provider only.</span></span> <span data-ttu-id="02dc0-126">Sin embargo, puede obtener datos del registro a través de métodos como <a href="/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov"><strong>EnumKey</strong></a> o <a href="/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov"><strong>EnumValue</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="02dc0-126">However, you can get registry data through methods such as <a href="/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov"><strong>EnumKey</strong></a> or <a href="/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov"><strong>EnumValue</strong></a>.</span></span> <span data-ttu-id="02dc0-127">El <a href="/windows/desktop/CIMWin32Prov/win32-registry"><strong>Win32_Registry</strong></a>, que se encuentra en el espacio de nombres root\cimv2, obtiene datos sobre el registro en su conjunto, como su tamaño.</span><span class="sxs-lookup"><span data-stu-id="02dc0-127">The <a href="/windows/desktop/CIMWin32Prov/win32-registry"><strong>Win32_Registry</strong></a>, located in root\cimv2 namespace, gets data about the registry as a whole, such as how large it is.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-128">VB</span><span class="sxs-lookup"><span data-stu-id="02dc0-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_CURRENT_USER = &H80000001
strComputer = &quot;.&quot;
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
strKeyPath = &quot;Console&quot;
strValueName = &quot;HistoryBufferSize&quot;
oReg.GetDWORDValue HKEY_CURRENT_USER,strKeyPath,strValueName,dwValue
WScript.Echo &quot;Current History Buffer Size: &quot; & dwValue</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="02dc0-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_CURRENT_USER =2147483649
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key = &quot;Console&quot;
$Value = &quot;HistoryBufferSize&quot;
$results = $reg.GetDWORDValue($HKEY_CURRENT_USER, $Key, $value)
&quot;Current History Buffer Size: {0}&quot; -f $results.uValue</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="02dc0-130">... ¿crear una nueva clave del registro?</span><span class="sxs-lookup"><span data-stu-id="02dc0-130">...create a new registry key?</span></span></td>
<td><p><span data-ttu-id="02dc0-131">Use la clase <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , que se encuentra en el espacio de nombres root\default y el método <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="02dc0-131">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace, and the <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-132">VB</span><span class="sxs-lookup"><span data-stu-id="02dc0-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strComputer = &quot;.&quot;
Set objReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)

strKeyPath = &quot;SOFTWARE\NewKey&quot;
objReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
WScript.Echo &quot;Created registry key HKEY_LOCAL_MACHINE\SOFTWARE\NewKey&quot;</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="02dc0-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key     = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.CreateKey($HKEY_LOCAL_MACHINE, $Key)
If ($results.Returnvalue -eq 0) {&quot;Key created&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02dc0-134">... ¿crear un nuevo valor del registro en una clave?</span><span class="sxs-lookup"><span data-stu-id="02dc0-134">...create a new registry value under a key?</span></span></td>
<td><p><span data-ttu-id="02dc0-135">Use la clase <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , que se encuentra en el espacio de nombres root\default, y el método <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="02dc0-135">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in the root\default namespace, and the <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> method.</span></span> <span data-ttu-id="02dc0-136">A continuación, use uno de los métodos set, dependiendo del tipo de elemento del registro en el que se encuentra el valor, como <a href="/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov"><strong>SetDWORDValue</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="02dc0-136">Then use one of the Set methods, depending on what registry datatype the value is, such as the <a href="/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov"><strong>SetDWORDValue</strong></a>.</span></span> <span data-ttu-id="02dc0-137">Los métodos set crean un valor si aún no existe.</span><span class="sxs-lookup"><span data-stu-id="02dc0-137">The Set methods create a value if it does not already exist.</span></span> <span data-ttu-id="02dc0-138">Para obtener más información, vea <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">asignar un tipo de datos del registro a un tipo de datos de WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="02dc0-138">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-139">VB</span><span class="sxs-lookup"><span data-stu-id="02dc0-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
Set objReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
strValueName = &quot;Example_Expanded_String_Value&quot;
strValue = &quot;%PATHEXT%&quot;
objReg.SetExpandedStringValue HKEY_LOCAL_MACHINE,strKeyPath,strValueName,strValue
WScript.Echo &quot;Example expanded_String_Value at &quot; & &quot;HKEY_LOCAL_MACHINE\SOFTWARE\NewKey&quot;</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="02dc0-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$ValueName = &quot;Example_Expanded_String_Value&quot;
$Value     = &quot;%PATHEXT%&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.SetExpandedStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName, $Value)
If ($results.Returnvalue -eq 0) {&quot;Value created&quot;}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02dc0-141">... ¿desea evitar obtener un error de clase no válida al intentar escribir un script para leer el registro?</span><span class="sxs-lookup"><span data-stu-id="02dc0-141">...avoid getting an Invalid Class error when trying to write a script to read the registry?</span></span></td>
<td><p><span data-ttu-id="02dc0-142">Use el espacio de nombres root\default al tener acceso a la clase <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="02dc0-142">Use the root\default namespace when accessing the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class.</span></span> <span data-ttu-id="02dc0-143"><strong>StdRegProv</strong> no forma parte del espacio de nombres de cimv2, que es el motivo por el que &quot; se genera un error de clase no válido &quot; si se intenta conectarse a &quot; Root\cimv2: StdRegProv &quot; .</span><span class="sxs-lookup"><span data-stu-id="02dc0-143"><strong>StdRegProv</strong> is not part of the cimv2 namespace, which is why an &quot;Invalid Class&quot; error is generated if you try to connect to &quot;root\cimv2:StdRegProv&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-144">VB</span><span class="sxs-lookup"><span data-stu-id="02dc0-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HKEY_CURRENT_USER = &H80000001
strComputer = &quot;.&quot;
Set oReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;) 
strKeyPath = &quot;Console&quot;
strValueName = &quot;HistoryBufferSize&quot;
oReg.GetDWORDValue HKEY_CURRENT_USER, strKeyPath, strValueName, dwValue
Wscript.Echo &quot;Current History Buffer Size: &quot; & dwValue</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02dc0-145">... ¿comprobar la seguridad en una clave del registro específica?</span><span class="sxs-lookup"><span data-stu-id="02dc0-145">...check security on a specific registry key?</span></span></td>
<td><p><span data-ttu-id="02dc0-146">Use la clase <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , que se encuentra en el espacio de nombres root\default y el método <a href="/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov"><strong>checkAccess</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="02dc0-146">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov"><strong>CheckAccess</strong></a> method.</span></span> <span data-ttu-id="02dc0-147">Solo puede comprobar los derechos de acceso del usuario actual que está ejecutando el script o la aplicación.</span><span class="sxs-lookup"><span data-stu-id="02dc0-147">You can only check the access rights for the current user that is running the script or application.</span></span> <span data-ttu-id="02dc0-148">No puede comprobar los derechos de acceso de otro usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="02dc0-148">You cannot check the access rights for another specified user.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02dc0-149">... ¿leer y escribir valores de registro binarios?</span><span class="sxs-lookup"><span data-stu-id="02dc0-149">...read and write binary registry values?</span></span></td>
<td><p><span data-ttu-id="02dc0-150">Use la clase <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , que se encuentra en &quot; &quot; el espacio de nombres Root\Default y los métodos <a href="/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov"><strong>GetBinaryValue</strong></a> y <a href="/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov"><strong>SetBinaryValue</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="02dc0-150">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in &quot;Root\Default&quot; namespace and the <a href="/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov"><strong>GetBinaryValue</strong></a> and <a href="/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov"><strong>SetBinaryValue</strong></a> methods.</span></span> <span data-ttu-id="02dc0-151">Los valores del registro que aparecen en la utilidad RegEdt32 como una serie de valores hexadecimales de bytes están en el formato de datos <strong>REG_BINARY</strong> .</span><span class="sxs-lookup"><span data-stu-id="02dc0-151">Registry values that appear in the RegEdt32 utility as a series of byte hexadecimal values are in the <strong>REG_BINARY</strong> data format.</span></span> <span data-ttu-id="02dc0-152">Para obtener más información, vea <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">asignar un tipo de datos del registro a un tipo de datos de WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="02dc0-152">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span> <span data-ttu-id="02dc0-153">En el ejemplo de código de VBScript siguiente se crea una nueva clave con un valor binario.</span><span class="sxs-lookup"><span data-stu-id="02dc0-153">The following VBScript code example creates a new key with a binary value.</span></span> <span data-ttu-id="02dc0-154">El valor binario se proporciona en la matriz de bytes <em>iValues</em> especificada en hex.</span><span class="sxs-lookup"><span data-stu-id="02dc0-154">The binary value is supplied in the <em>iValues</em> byte array specified in Hex.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-155">VB</span><span class="sxs-lookup"><span data-stu-id="02dc0-155">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
iValues = Array(&H01,&Ha2,&H10)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
strKeyPath = &quot;SOFTWARE\NewKey&quot;
BinaryValueName = &quot;Example Binary Value&quot;

oReg.SetBinaryValue HKEY_LOCAL_MACHINE,strKeyPath,BinaryValueName,iValues</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="02dc0-156">El siguiente script lee el valor binario.</span><span class="sxs-lookup"><span data-stu-id="02dc0-156">The following script reads the binary value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-157">VB</span><span class="sxs-lookup"><span data-stu-id="02dc0-157">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002 
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strValueName = &quot;Example Binary Value&quot;
strComputer = &quot;.&quot;
dim iValues(3)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.GetBinaryValue HKEY_LOCAL_MACHINE,strKeyPath,strValueName,iValues
For i = lBound(iValues) to uBound(iValues)
Wscript.Echo iValues(i)
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-158">PowerShell</span><span class="sxs-lookup"><span data-stu-id="02dc0-158">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$ValueName = &quot;Example Binary Value&quot;
$Values     = @(0x54, 0x46, 0x4C)
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.GetBinaryValue($HKEY_LOCAL_MACHINE, $Key, $ValueName)
Foreach ($byte in $results.uvalue) {&quot;{0}&quot; -f $byte.tostring(&quot;x&quot;)}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02dc0-159">... leer y escribir valores del registro que contienen varias cadenas</span><span class="sxs-lookup"><span data-stu-id="02dc0-159">...read and write registry values that contain multiple strings?</span></span></td>
<td><p><span data-ttu-id="02dc0-160">Use la clase <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , que se encuentra en el espacio de nombres root\default y los métodos <a href="/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov"><strong>GetMultiStringValue</strong></a> y <a href="/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov"><strong>SetMultiStringValue</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="02dc0-160">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov"><strong>GetMultiStringValue</strong></a> and <a href="/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov"><strong>SetMultiStringValue</strong></a> methods.</span></span> <span data-ttu-id="02dc0-161">Las claves del registro que aparecen en la utilidad RegEdt32 como una serie de cadenas separadas por espacios se encuentran en el formato de datos <strong>REG_MULTI_SZ</strong> .</span><span class="sxs-lookup"><span data-stu-id="02dc0-161">Registry keys that appear in the RegEdt32 utility as a series of strings separated by spaces are in the <strong>REG_MULTI_SZ</strong> data format.</span></span> <span data-ttu-id="02dc0-162">Para obtener más información, vea <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">asignar un tipo de datos del registro a un tipo de datos de WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="02dc0-162">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span> <span data-ttu-id="02dc0-163">En el ejemplo de código de VBScript siguiente se crea una nueva clave y un nuevo valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="02dc0-163">The following VBScript code example creates a new key and a new multistring value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-164">VB</span><span class="sxs-lookup"><span data-stu-id="02dc0-164">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
MultValueName = &quot;Example Multistring Value&quot;
strComputer = &quot;.&quot;
iValues = Array(&quot;string1&quot;, &quot;string2&quot;)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
oReg.SetMultiStringValue HKEY_LOCAL_MACHINE,strKeyPath,MultValueName,iValues</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-165">PowerShell</span><span class="sxs-lookup"><span data-stu-id="02dc0-165">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$ValueName = &quot;Example MultiString Value&quot;
$Values     = @(&quot;Thomas&quot;, &quot;Susan&quot;, &quot;Rebecca&quot;)
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName, $Values)
If ($results.Returnvalue -eq 0) {&quot;Value Set&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="02dc0-166">El siguiente script lee el valor de multistring.</span><span class="sxs-lookup"><span data-stu-id="02dc0-166">The following script reads the multistring value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-167">VB</span><span class="sxs-lookup"><span data-stu-id="02dc0-167">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
iValues = Array(&quot;string1&quot;, &quot;string2&quot;)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
MultValueName = &quot;Example Multistring Value&quot;
oReg.GetMultiStringValue HKEY_LOCAL_MACHINE,strKeyPath,MultValueName,iValues
For Each strValue In iValues
WScript.echo strValue
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-168">PowerShell</span><span class="sxs-lookup"><span data-stu-id="02dc0-168">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Define Constants
$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$ValueName = &quot;Example MultiString Value&quot;
$results   = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName)
$results.svalue</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02dc0-169">... ¿quitar una clave del registro?</span><span class="sxs-lookup"><span data-stu-id="02dc0-169">...remove a registry key?</span></span></td>
<td><p><span data-ttu-id="02dc0-170">Use la clase <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , que se encuentra en el espacio de nombres root\default y los métodos <a href="/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov"><strong>DeleteKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="02dc0-170">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov"><strong>DeleteKey</strong></a> methods.</span></span></p>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dc0-171">PowerShell</span><span class="sxs-lookup"><span data-stu-id="02dc0-171">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key     = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.DeleteKey($HKEY_LOCAL_MACHINE, $Key)
If ($results.Returnvalue -eq 0) {&quot;Key Removed&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="02dc0-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02dc0-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02dc0-173">Tareas de WMI para scripts y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="02dc0-173">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="02dc0-174">Ejemplos de aplicaciones de C++ de WMI</span><span class="sxs-lookup"><span data-stu-id="02dc0-174">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="02dc0-175">ScriptCenter de TechNet</span><span class="sxs-lookup"><span data-stu-id="02dc0-175">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> <dt>

[<span data-ttu-id="02dc0-176">Modificar el registro del sistema</span><span class="sxs-lookup"><span data-stu-id="02dc0-176">Modifying the System Registry</span></span>](modifying-the-system-registry.md)
</dt> <dt>

[<span data-ttu-id="02dc0-177">**StdRegProv**</span><span class="sxs-lookup"><span data-stu-id="02dc0-177">**StdRegProv**</span></span>](/previous-versions/windows/desktop/regprov/stdregprov)
</dt> </dl>
