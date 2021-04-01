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
# <a name="provider-complex-type"></a>Tipo complejo de proveedor

Define un proveedor y los contadores que proporciona.

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

## <a name="child-elements"></a>Elementos secundarios



| Elemento        | Tipo                                                                   | Descripción                                                                                 |
|----------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **counterSet** | [**Man: counterSet**](performance-counters-counterset-complex-type.md) | Identifica el conjunto de contadores que contiene uno o más contadores relacionados lógicamente.<br/> |



## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre</th>
<th>Tipo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>applicationIdentity</td>
<td><strong>xs:string</strong></td>
<td>Nombre del archivo binario que contiene las cadenas de recursos localizadas, ya sea un archivo. exe o. dll (no incluya la ruta de acceso al archivo binario).<br/> La utilidad Lodctr.exe usa la ruta de acceso del parámetro opcional [<em>path</em>] para buscar el archivo binario. Por ejemplo, <strong>LODCTR</strong> [<strong>/m:</strong><em>manifest</em> [<em>rutaDeAcceso</em>]]. Si no incluye el parámetro [<em>path</em>], Lodctr.exe busca en la carpeta que contiene el manifiesto.<br/></td>
</tr>
<tr class="even">
<td>devolución de llamada</td>

<td>Este atributo indica que desea recibir una notificación cuando un consumidor realiza ciertas acciones. <br/> Si incluye este atributo, la herramienta CTRPP utiliza la firma de la función de <a href="counterinitialize.md"><strong>Contrainicialización</strong></a> alternativa, que se usa para pasar el nombre de la función que implementa la función de devolución de llamada <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> .<br/> Como alternativa a especificar este atributo, puede usar el argumento <strong>-NotificationCallback</strong><a href="ctrpp.md">CTRPP</a> .<br/> <strong>Windows Vista:</strong> El único valor válido para este atributo es &quot; Custom &quot; . La utilidad <a href="ctrpp.md">CTRPP</a> genera la plantilla para una función de devolución de llamada <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> . La plantilla se incluye en el archivo. c que CTRPP generó. <br/> <br/></td>
</tr>
<tr class="odd">
<td>providerGuid</td>
<td><a href="performance-counters-guidtype-simple-type.md"><strong>Man: GUIDType</strong></a></td>
<td>GUID de cadena que identifica de forma única el proveedor en el manifiesto. El GUID debe ser único dentro del manifiesto.<br/> Solo tiene que proporcionar un nuevo GUID cuando la versión de la aplicación cambia (si admite instalaciones en paralelo).<br/></td>
</tr>
<tr class="even">
<td>providerName</td>
<td><strong>xs:string</strong></td>
<td>Nombre que se utiliza para crear el nombre de la clase de Win32_PerfRawData WMI. Si no especifica un nombre, los &quot; contadores &quot; se usan como el nombre de la clase.<br/></td>
</tr>
<tr class="odd">
<td>providerType</td>

<td>Identifica si el proveedor es un proveedor de modo de usuario, un proveedor de modo kernel o un proveedor de controladores. Los valores posibles son los siguientes.<br/> 
<table>
<thead>
<tr class="header">
<th>Término</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>En modo usuario<br/></td>
<td>Especifique este modo para un componente de modo de usuario, como una aplicación, un archivo DLL o un controlador de modo de usuario. Las extensiones típicas para los componentes de modo de usuario son. exe o. dll. Este es el valor predeterminado.<br/></td>
</tr>
<tr class="even">
<td><span id="kernel"></span><span id="KERNEL"></span>Cronología<br/></td>
<td>Especifique este modo para un componente de modo kernel como un controlador WDM o WDF. La extensión típica para los componentes de modo kernel es. sys.<br/> <strong>Windows Vista y Windows Server 2008:</strong> Este valor no se admite hasta Windows 7 y Windows Server 2008 R2.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>resourceBase</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32Type</strong></a></td>
<td><p>Define el valor de índice del recurso inicial que <a href="ctrpp.md">CTRPP</a> usa para generar los identificadores de recursos.</p></td>
</tr>
<tr class="odd">
<td>símbolo</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>Man: CSymbolType</strong></a></td>
<td><p>Nombre simbólico que identifica el proveedor. La herramienta <a href="ctrpp.md">CTRPP</a> crea una variable de identificador que se puede usar al llamar a funciones que requieren un identificador al proveedor (por ejemplo, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>). El nombre simbólico es el nombre de la variable.</p>
<p>Si incluye el argumento <strong>-prefix</strong> al llamar a <a href="ctrpp.md">CTRPP</a>, la cadena de prefijo se agrega al principio del nombre simbólico.</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




