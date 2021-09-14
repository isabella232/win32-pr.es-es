---
description: Define un proveedor y los contadores que proporciona.
ms.assetid: 85299b01-5679-40f8-8aec-5c2ff8d7cfc8
title: provider Complex Type (Tipo complejo de proveedor)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94654c538cc0637e6c90e0b14d3433b979762b00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250611"
---
# <a name="provider-complex-type"></a>provider Complex Type (Tipo complejo de proveedor)

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
| **counterSet** | [**man:counterSet**](performance-counters-counterset-complex-type.md) | Identifica el conjunto de contadores que contiene uno o varios contadores relacionados lógicamente.<br/> |



## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>Nombre del archivo binario que contiene las cadenas de recursos localizadas, ya sea un archivo .exe o .dll (no incluya la ruta de acceso al archivo binario).<br/> La Lodctr.exe utiliza la ruta de acceso del parámetro opcional [<em>path</em>] para buscar el archivo binario. Por ejemplo, <strong>lodctr</strong> [<strong>/m:</strong><em>manifest</em> [<em>path</em>]]. Si no incluye el parámetro [<em>path</em>], Lodctr.exe busca en la carpeta que contiene el manifiesto.<br/></td>
</tr>
<tr class="even">
<td>devolución de llamada</td>

<td>Este atributo indica que desea recibir una notificación cuando un consumidor realiza determinadas acciones. <br/> Si incluye este atributo, la herramienta CTRPP usa la firma de función <a href="counterinitialize.md"><strong>CounterInitialize</strong></a> alternativa, que se usa para pasar el nombre de la función que implementa la función de devolución de llamada <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback.</strong></a><br/> Como alternativa a la especificación de este atributo, puede usar el <strong>argumento -NotificationCallback</strong><a href="ctrpp.md">CTRPP.</a><br/> <strong>Windows Vista:</strong> El único valor válido para este atributo es &quot; &quot; personalizado. La <a href="ctrpp.md">utilidad CTRPP</a> genera la plantilla para una función de devolución de llamada <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback.</strong></a> La plantilla se incluye en el archivo .c generado por CTRPP. <br/> <br/></td>
</tr>
<tr class="odd">
<td>providerGuid</td>
<td><a href="performance-counters-guidtype-simple-type.md"><strong>man:GUIDType</strong></a></td>
<td>GUID de cadena que identifica de forma única el proveedor en el manifiesto. El GUID debe ser único dentro del manifiesto.<br/> Solo debe proporcionar un nuevo GUID cuando cambie la versión de la aplicación (si admite instalaciones en paralelo).<br/></td>
</tr>
<tr class="even">
<td>providerName</td>
<td><strong>xs:string</strong></td>
<td>Nombre que se usa para crear el nombre de clase wmi Win32_PerfRawData clase. Si no especifica un nombre, &quot; se usa Counters &quot; como nombre de la clase.<br/></td>
</tr>
<tr class="odd">
<td>providerType</td>

<td>Identifica si el proveedor es un proveedor de modo de usuario, un proveedor en modo kernel o un proveedor de controladores. Los valores posibles son los siguientes.<br/> 
<table>
<thead>
<tr class="header">
<th>Término</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>userMode<br/></td>
<td>Especifique este modo para un componente de modo de usuario, como una aplicación, un archivo DLL o un controlador en modo de usuario. Las extensiones típicas para los componentes en modo de usuario se .exe o .dll. Este es el valor predeterminado.<br/></td>
</tr>
<tr class="even">
<td><span id="kernel"></span><span id="KERNEL"></span>Núcleo<br/></td>
<td>Especifique este modo para un componente en modo kernel, como un controlador WDM o WDF. La extensión típica para los componentes en modo kernel es .sys.<br/> <strong>Windows Vista y Windows Server 2008:</strong> Este valor no se admite hasta Windows 7 y Windows Server 2008 R2.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>resourceBase</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></td>
<td><p>Define el valor inicial del índice de recursos que <a href="ctrpp.md">CTRPP</a> usa para generar los identificadores de recursos.</p></td>
</tr>
<tr class="odd">
<td>símbolo</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></td>
<td><p>Nombre simbólico que identifica el proveedor. La <a href="ctrpp.md">herramienta CTRPP</a> crea una variable HANDLE que puede usar al llamar a funciones que requieren un identificador para el proveedor (por ejemplo, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue).</strong></a> El nombre simbólico es el nombre de la variable.</p>
<p>Si incluye el <strong>argumento -prefix</strong> al llamar a <a href="ctrpp.md">CTRPP</a>, la cadena de prefijo se agrega al principio del nombre simbólico.</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




