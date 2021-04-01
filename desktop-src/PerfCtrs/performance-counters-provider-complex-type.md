---
description: Define un proveedor y los contadores que proporciona.
ms.assetid: 85299b01-5679-40f8-8aec-5c2ff8d7cfc8
title: Tipo complejo de proveedor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eec52139710d0ffafe06f22504a735e59312818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909714"
---
# <a name="provider-complex-type"></a><span data-ttu-id="85b6a-103">Tipo complejo de proveedor</span><span class="sxs-lookup"><span data-stu-id="85b6a-103">provider Complex Type</span></span>

<span data-ttu-id="85b6a-104">Define un proveedor y los contadores que proporciona.</span><span class="sxs-lookup"><span data-stu-id="85b6a-104">Defines a provider and the counters that it provides.</span></span>

``` syntax
<xs:complexType name="provider">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="counterSet"
            type="man:counterSet"
        >
            <xs:key name="uniqueCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@id"
                 />
            </xs:key>
            <xs:unique name="uniqueCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:unique>
            <xs:keyref name="existBaseID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@baseID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfTimeID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfTimeID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfFreqID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfFreqID"
                 />
            </xs:keyref>
            <xs:keyref name="existMultiCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@multiCounterID"
                 />
            </xs:keyref>
            <xs:key name="uniqueStructNames">
                <xs:selector
                    xpath="./man:structs/man:struct"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
            <xs:keyref name="existCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@struct"
                 />
            </xs:keyref>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="callback"
        use="optional"
        default="default"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="custom"
                 />
                <xs:enumeration
                    value="default"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerGuid"
        type="man:GUIDType"
        use="required"
     />
    <xs:attribute name="applicationIdentity"
        type="xs:string"
        use="required"
     />
    <xs:attribute name="providerType"
        use="optional"
        default="userMode"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="userMode"
                 />
                <xs:enumeration
                    value="kernelMode"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerName"
        type="xs:string"
        use="optional"
        default="Counters"
     />
    <xs:attribute name="resourceBase"
        type="man:UInt32Type"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="85b6a-105">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="85b6a-105">Child elements</span></span>



| <span data-ttu-id="85b6a-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="85b6a-106">Element</span></span>        | <span data-ttu-id="85b6a-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="85b6a-107">Type</span></span>                                                                   | <span data-ttu-id="85b6a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="85b6a-108">Description</span></span>                                                                                 |
|----------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="85b6a-109">**counterSet**</span><span class="sxs-lookup"><span data-stu-id="85b6a-109">**counterSet**</span></span> | [<span data-ttu-id="85b6a-110">**Man: counterSet**</span><span class="sxs-lookup"><span data-stu-id="85b6a-110">**man:counterSet**</span></span>](performance-counters-counterset-complex-type.md) | <span data-ttu-id="85b6a-111">Identifica el conjunto de contadores que contiene uno o más contadores relacionados lógicamente.</span><span class="sxs-lookup"><span data-stu-id="85b6a-111">Identifies the counter set that contains one or more logically related counters.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="85b6a-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="85b6a-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85b6a-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="85b6a-113">Name</span></span></th>
<th><span data-ttu-id="85b6a-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="85b6a-114">Type</span></span></th>
<th><span data-ttu-id="85b6a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="85b6a-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="85b6a-116">applicationIdentity</span><span class="sxs-lookup"><span data-stu-id="85b6a-116">applicationIdentity</span></span></td>
<td><span data-ttu-id="85b6a-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="85b6a-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="85b6a-118">Nombre del archivo binario que contiene las cadenas de recursos localizadas, ya sea un archivo. exe o. dll (no incluya la ruta de acceso al archivo binario).</span><span class="sxs-lookup"><span data-stu-id="85b6a-118">The name of the binary file that contains the localized resource strings, either an .exe or .dll file (do not include the path to the binary).</span></span><br/> <span data-ttu-id="85b6a-119">La utilidad Lodctr.exe usa la ruta de acceso del parámetro opcional [<em>path</em>] para buscar el archivo binario.</span><span class="sxs-lookup"><span data-stu-id="85b6a-119">The Lodctr.exe utility uses the path from the optional [<em>path</em>] parameter to search for the binary file.</span></span> <span data-ttu-id="85b6a-120">Por ejemplo, <strong>LODCTR</strong> [<strong>/m:</strong><em>manifest</em> [<em>rutaDeAcceso</em>]].</span><span class="sxs-lookup"><span data-stu-id="85b6a-120">For example, <strong>lodctr</strong> [<strong>/m:</strong><em>manifest</em> [<em>path</em>]].</span></span> <span data-ttu-id="85b6a-121">Si no incluye el parámetro [<em>path</em>], Lodctr.exe busca en la carpeta que contiene el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="85b6a-121">If you do not include the [<em>path</em>] parameter, Lodctr.exe searches the folder that contains the manifest.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b6a-122">devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="85b6a-122">callback</span></span></td>

<td><span data-ttu-id="85b6a-123">Este atributo indica que desea recibir una notificación cuando un consumidor realiza ciertas acciones.</span><span class="sxs-lookup"><span data-stu-id="85b6a-123">This attribute indicates that you want to receive notification when a consumer performs certain actions.</span></span> <br/> <span data-ttu-id="85b6a-124">Si incluye este atributo, la herramienta CTRPP utiliza la firma de la función de <a href="counterinitialize.md"><strong>Contrainicialización</strong></a> alternativa, que se usa para pasar el nombre de la función que implementa la función de devolución de llamada <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85b6a-124">If you include this attribute, the CTRPP tool uses the alternate <a href="counterinitialize.md"><strong>CounterInitialize</strong></a> function signature, which you use to pass in the name of your function that implements the <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> callback function.</span></span><br/> <span data-ttu-id="85b6a-125">Como alternativa a especificar este atributo, puede usar el argumento <strong>-NotificationCallback</strong><a href="ctrpp.md">CTRPP</a> .</span><span class="sxs-lookup"><span data-stu-id="85b6a-125">As an alternative to specifying this attribute, you can use the <strong>-NotificationCallback</strong><a href="ctrpp.md">CTRPP</a> argument.</span></span><br/> <span data-ttu-id="85b6a-126"><strong>Windows Vista:</strong> El único valor válido para este atributo es &quot; Custom &quot; .</span><span class="sxs-lookup"><span data-stu-id="85b6a-126"><strong>Windows Vista:</strong> The only valid value for this attribute is &quot;custom&quot;.</span></span> <span data-ttu-id="85b6a-127">La utilidad <a href="ctrpp.md">CTRPP</a> genera la plantilla para una función de devolución de llamada <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85b6a-127">The <a href="ctrpp.md">CTRPP</a> utility generates the template for a <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> callback function.</span></span> <span data-ttu-id="85b6a-128">La plantilla se incluye en el archivo. c que CTRPP generó.</span><span class="sxs-lookup"><span data-stu-id="85b6a-128">The template is included in the .c file that CTRPP generated.</span></span> <br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b6a-129">providerGuid</span><span class="sxs-lookup"><span data-stu-id="85b6a-129">providerGuid</span></span></td>
<td><span data-ttu-id="85b6a-130"><a href="performance-counters-guidtype-simple-type.md"><strong>Man: GUIDType</strong></a></span><span class="sxs-lookup"><span data-stu-id="85b6a-130"><a href="performance-counters-guidtype-simple-type.md"><strong>man:GUIDType</strong></a></span></span></td>
<td><span data-ttu-id="85b6a-131">GUID de cadena que identifica de forma única el proveedor en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="85b6a-131">String GUID that uniquely identifies the provider in the manifest.</span></span> <span data-ttu-id="85b6a-132">El GUID debe ser único dentro del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="85b6a-132">The GUID must be unique within the manifest.</span></span><br/> <span data-ttu-id="85b6a-133">Solo tiene que proporcionar un nuevo GUID cuando la versión de la aplicación cambia (si admite instalaciones en paralelo).</span><span class="sxs-lookup"><span data-stu-id="85b6a-133">You need to provide a new GUID only when the version of the application changes (if you support side-by-side installations).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b6a-134">providerName</span><span class="sxs-lookup"><span data-stu-id="85b6a-134">providerName</span></span></td>
<td><span data-ttu-id="85b6a-135"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="85b6a-135"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="85b6a-136">Nombre que se utiliza para crear el nombre de la clase de Win32_PerfRawData WMI.</span><span class="sxs-lookup"><span data-stu-id="85b6a-136">The name that is used to create the WMI Win32_PerfRawData class name.</span></span> <span data-ttu-id="85b6a-137">Si no especifica un nombre, los &quot; contadores &quot; se usan como el nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="85b6a-137">If you do not specify a name, &quot;Counters&quot; is used as the name of the class.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b6a-138">providerType</span><span class="sxs-lookup"><span data-stu-id="85b6a-138">providerType</span></span></td>

<td><span data-ttu-id="85b6a-139">Identifica si el proveedor es un proveedor de modo de usuario, un proveedor de modo kernel o un proveedor de controladores.</span><span class="sxs-lookup"><span data-stu-id="85b6a-139">Identifies whether the provider is a user-mode provider, kernel-mode provider, or driver provider.</span></span> <span data-ttu-id="85b6a-140">Los valores posibles son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="85b6a-140">Possible values are as follows.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="85b6a-141">Término</span><span class="sxs-lookup"><span data-stu-id="85b6a-141">Term</span></span></th>
<th><span data-ttu-id="85b6a-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="85b6a-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="85b6a-143"><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>En modo usuario</span><span class="sxs-lookup"><span data-stu-id="85b6a-143"><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>userMode</span></span><br/></td>
<td><span data-ttu-id="85b6a-144">Especifique este modo para un componente de modo de usuario, como una aplicación, un archivo DLL o un controlador de modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="85b6a-144">Specify this mode for a user-mode component such as an application, a DLL, or a user-mode driver.</span></span> <span data-ttu-id="85b6a-145">Las extensiones típicas para los componentes de modo de usuario son. exe o. dll.</span><span class="sxs-lookup"><span data-stu-id="85b6a-145">The typical extensions for user-mode components are .exe or .dll.</span></span> <span data-ttu-id="85b6a-146">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="85b6a-146">This is the default.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b6a-147"><span id="kernel"></span><span id="KERNEL"></span>Cronología</span><span class="sxs-lookup"><span data-stu-id="85b6a-147"><span id="kernel"></span><span id="KERNEL"></span>kernel</span></span><br/></td>
<td><span data-ttu-id="85b6a-148">Especifique este modo para un componente de modo kernel como un controlador WDM o WDF.</span><span class="sxs-lookup"><span data-stu-id="85b6a-148">Specify this mode for a kernel-mode component such as a WDM or WDF driver.</span></span> <span data-ttu-id="85b6a-149">La extensión típica para los componentes de modo kernel es. sys.</span><span class="sxs-lookup"><span data-stu-id="85b6a-149">The typical extension for kernel-mode components is .sys.</span></span><br/> <span data-ttu-id="85b6a-150"><strong>Windows Vista y Windows Server 2008:</strong> Este valor no se admite hasta Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="85b6a-150"><strong>Windows Vista and Windows Server 2008:</strong> This value is not supported until Windows 7 and Windows Server 2008 R2.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b6a-151">resourceBase</span><span class="sxs-lookup"><span data-stu-id="85b6a-151">resourceBase</span></span></td>
<td><span data-ttu-id="85b6a-152"><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="85b6a-152"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><p><span data-ttu-id="85b6a-153">Define el valor de índice del recurso inicial que <a href="ctrpp.md">CTRPP</a> usa para generar los identificadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="85b6a-153">Defines the starting resource index value that <a href="ctrpp.md">CTRPP</a> uses to generate the resource identifiers.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b6a-154">símbolo</span><span class="sxs-lookup"><span data-stu-id="85b6a-154">symbol</span></span></td>
<td><span data-ttu-id="85b6a-155"><a href="performance-counters-csymboltype-simple-type.md"><strong>Man: CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="85b6a-155"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><p><span data-ttu-id="85b6a-156">Nombre simbólico que identifica el proveedor.</span><span class="sxs-lookup"><span data-stu-id="85b6a-156">A symbolic name that identifies the provider.</span></span> <span data-ttu-id="85b6a-157">La herramienta <a href="ctrpp.md">CTRPP</a> crea una variable de identificador que se puede usar al llamar a funciones que requieren un identificador al proveedor (por ejemplo, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="85b6a-157">The <a href="ctrpp.md">CTRPP</a> tool creates a HANDLE variable that you can use when calling functions that require a handle to the provider (for example, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>).</span></span> <span data-ttu-id="85b6a-158">El nombre simbólico es el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="85b6a-158">The symbolic name is the name of the variable.</span></span></p>
<p><span data-ttu-id="85b6a-159">Si incluye el argumento <strong>-prefix</strong> al llamar a <a href="ctrpp.md">CTRPP</a>, la cadena de prefijo se agrega al principio del nombre simbólico.</span><span class="sxs-lookup"><span data-stu-id="85b6a-159">If you include the <strong>-prefix</strong> argument when calling <a href="ctrpp.md">CTRPP</a>, the prefix string is added to the beginning of the symbolic name.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="85b6a-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85b6a-160">Requirements</span></span>



| <span data-ttu-id="85b6a-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="85b6a-161">Requirement</span></span> | <span data-ttu-id="85b6a-162">Value</span><span class="sxs-lookup"><span data-stu-id="85b6a-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="85b6a-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85b6a-163">Minimum supported client</span></span><br/> | <span data-ttu-id="85b6a-164">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="85b6a-164">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="85b6a-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85b6a-165">Minimum supported server</span></span><br/> | <span data-ttu-id="85b6a-166">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="85b6a-166">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




