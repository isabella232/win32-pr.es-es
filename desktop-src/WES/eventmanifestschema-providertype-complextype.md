---
title: Tipo complejo ProviderType
description: Define un proveedor y los metadatos que usa para definir sus eventos. | Tipo complejo ProviderType
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- Tipo complejo ProviderType EventLog
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c258b3ff48cdd2f00f632fdce770b58182a531c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242744"
---
# <a name="providertype-complex-type"></a>Tipo complejo ProviderType

Define un proveedor y los metadatos que usa para definir sus eventos.

``` syntax
<xs:complexType name="ProviderType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
         />
        <xs:element name="keywords"
            type="KeywordListType"
         />
        <xs:element name="maps"
            type="MapType"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
         />
        <xs:element name="templates"
            type="TemplateListType"
         />
        <xs:element name="events"
            type="DefinitionType"
         />
        <xs:element name="filters"
            type="FilterListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="guid"
        type="GUIDType"
        use="required"
     />
    <xs:attribute name="resourceFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="messageFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="parameterFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="helpLink"
        type="anyURI"
        use="optional"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="required"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:attribute name="source"
        use="optional"
        default="Xml"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="Xml"
                 />
                <xs:enumeration
                    value="Wbem"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="warnOnApplicationCompatibilityError"
        type="xs:boolean"
        use="optional"
        default="false"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                       | Tipo                                                                         | Descripción                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**channels**](eventmanifestschema-channels-providertype-element.md)         | [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md)   | Define una lista de canales en los que los proveedores pueden registrar eventos.<br/>                                                                                                                                                                                      |
| [**events**](eventmanifestschema-events-providertype-element.md)             | [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md)     | Define una lista de definiciones de eventos de los eventos que el proveedor puede registrar.<br/>                                                                                                                                                                       |
| **Filtros**                                                                   | [**FilterListType**](eventmanifestschema-filterlisttype-complextype.md)     | Define una lista de filtros que admite el proveedor. Puede usar los filtros, como haría con las palabras clave y , para determinar si desea escribir un evento. <br/> **Windows Server 2008 y Windows Vista:** No se admite hasta Windows 7.<br/> |
| [**Palabras clave**](eventmanifestschema-keywords-providertype-element.md)         | [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md)   | Define una lista de palabras clave que clasifican eventos.<br/>                                                                                                                                                                                                 |
| [**Niveles**](eventmanifestschema-levels-providertype-element.md)             | [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)       | Define una lista de niveles que especifican la gravedad de un evento.<br/>                                                                                                                                                                                    |
| [**Mapas**](eventmanifestschema-maps-providertype-element.md)                 | [**MapType**](eventmanifestschema-maptype-complextype.md)                   | Define una lista de pares nombre-valor a los que puede hacer referencia en la sección de plantilla del manifiesto.<br/>                                                                                                                                                 |
| [**namedQueries**](eventmanifestschema-namedqueries-providertype-element.md) | [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)     | No se usa. Define una lista de consultas con nombre que consultan la cadena del mensaje de evento para obtener un valor y realizan una acción especificada si se encuentran.<br/>                                                                                                                 |
| [**Opcodes**](eventmanifestschema-opcodes-providertype-element.md)           | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)     | Define una lista de códigos de operación que puede usar para agrupar eventos dentro de una tarea.<br/>                                                                                                                                                                          |
| [**Tareas**](eventmanifestschema-tasks-providertype-element.md)               | [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)         | Define una lista de tareas que un proveedor puede usar para agrupar eventos. Normalmente, se usan tareas para agrupar eventos para una característica o componente del proveedor.<br/>                                                                                              |
| [**Plantillas**](eventmanifestschema-templates-providertype-element.md)       | [**TemplateListType**](eventmanifestschema-templatelisttype-complextype.md) | Define una lista de plantillas que especifican los datos que se incluirán con los eventos.<br/>                                                                                                                                                                      |



## <a name="attributes"></a>Atributos



| Nombre                                | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| guid                                | [**GUIDType**](eventmanifestschema-guidtype-simpletype.md)       | GUID que identifica de forma única el proveedor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| helpLink                            | anyURI                                                            | La dirección URL o el vínculo de ayuda de MS al contenido que proporciona información sobre los eventos que genera el proveedor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| message                             | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nombre para mostrar localizado del proveedor. La cadena de mensaje hace referencia a una cadena localizada en la [**sección stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto. <br/>                                                                                                                                                                                                                                                                                                                           |
| messageFileName                     | [**filePath**](eventmanifestschema-filepath-simpletype.md)       | Ruta de acceso completa al archivo que contiene los recursos de mensaje localizados del proveedor. El archivo puede ser un archivo ejecutable o un archivo DLL.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| name                                | anyURI                                                            | Nombre del proveedor. El nombre debe tener el formato Componente - *de producto de* la - *empresa*.<br/> El nombre no puede tener más de 255 caracteres y no puede contener los caracteres: ">", "<", "&", "", \| "", ", \\ ", ", ":", "", "?", "" o caracteres con códigos menores \* que 31. Además, el nombre debe seguir las restricciones generales en los nombres de clave de archivo y registro. Estas restricciones se pueden encontrar en [Asignación de](/windows/desktop/FileIO/naming-a-file)nombres a un archivo y Límites [de tamaño de elemento del Registro.](/windows/desktop/SysInfo/registry-element-size-limits)<br/> |
| parameterFileName                   | [**filePath**](eventmanifestschema-filepath-simpletype.md)       | Ruta de acceso completa al archivo que contiene los recursos de cadena de parámetros del proveedor. El archivo puede ser un archivo ejecutable o un archivo DLL. Puede especificar más de un archivo de parámetros separados por punto y coma. Se busca en el archivo cuando la cadena de mensaje de un evento contiene una cadena de parámetro. Los parámetros permiten proporcionar cadenas de inserción localizables. Vea Comentarios para obtener más información.<br/>                                                                                                                                                |
| resourceFileName                    | [**Filepath**](eventmanifestschema-filepath-simpletype.md)       | Ruta de acceso completa al archivo que contiene los recursos de metadatos del proveedor. El archivo puede ser un archivo ejecutable o un archivo DLL.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| source                              |                                                                   | Solo para uso interno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| símbolo                              | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Símbolo que se va a usar para hacer referencia al GUID del proveedor en la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) usa el símbolo para crear una constante para el GUID del proveedor en el archivo de encabezado que genera el compilador.<br/>                                                                                                                                                                                                                                                                           |
| warnOnApplicationCompatibilityError | **xs:boolean**                                                    | Solo para uso interno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a>Observaciones

El Windows Visor de eventos (Eventvwr.exe) usará la cadena de mensaje localizada si está disponible; de lo contrario, usa la cadena del atributo name.

Las rutas de acceso de resourceFileName, messageFileName y parameterFileName pueden contener variables de entorno. Si define una nueva variable de entorno que se usará en la ruta de acceso, debe reiniciar el equipo para que el servicio de registro de eventos pueda seleccionar la nueva variable. De lo contrario, el servicio no podrá encontrar los recursos del proveedor.

La cadena de mensaje de un evento puede contener cadenas de inserción y cadenas de parámetros. Una cadena de inserción tiene el formato %*n*, donde *n* es un índice basado en uno que identifica un elemento de datos de la plantilla de datos del evento que desea insertar en el mensaje. Una cadena de parámetro (vea el atributo **parameterFileName)** tiene el formato %%*n*, donde n es el identificador de un mensaje en la tabla de mensajes. Si la cadena de mensaje del evento contenía "%1 %%11 = %2 %%12" y los valores del elemento de datos para %1 y %2 eran 8 y 2, respectivamente, y las cadenas de parámetro para %%11 y %%12 eran "cuartos" y "cuartos", respectivamente, la cadena con formato sería "8 cuarciones = 2ns".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

