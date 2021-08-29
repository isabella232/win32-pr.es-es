---
title: Tipo complejo ChannelPublishingType
description: Define las propiedades de registro de la sesión que usa el canal. | Tipo complejo ChannelPublishingType
ms.assetid: 4b3980f4-8652-4070-97c0-99cd1a9fc85a
keywords:
- ChannelPublishingType, tipo complejo EventLog
topic_type:
- apiref
api_name:
- ChannelPublishingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 653f746fe7f60efc03b4f8e38f9a38cf6bbc7761b6e63e4263d913632e8ec719
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863695"
---
# <a name="channelpublishingtype-complex-type"></a>Tipo complejo ChannelPublishingType

Define las propiedades de registro de la sesión que usa el canal.

``` syntax
<xs:complexType name="ChannelPublishingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="level"
            type="UInt8Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="UInt64Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="controlGuid"
            type="GUIDType"
            minOccurs="0"
         />
        <xs:element name="bufferSize"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="minBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="fileMax"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="maxBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="latency"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="clockType"
            default="SystemTime"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="SystemTime"
                     />
                    <xs:enumeration
                        value="QPC"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="sidType"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="None"
                     />
                    <xs:enumeration
                        value="Publishing"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                              | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**bufferSize**](eventmanifestschema-buffersize-channelpublishingtype-element.md)   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Cantidad de memoria, en kilobytes, que se asignará para cada búfer. Si espera una tasa de eventos relativamente baja, el tamaño del búfer debe establecerse en el tamaño de página de memoria. Si se espera que la tasa de eventos sea relativamente alta, debe especificar un tamaño de búfer mayor y aumentar el número máximo de búferes.<br/> El tamaño del búfer afecta a la velocidad a la que se rellenan los búferes y se deben vaciar. Aunque un tamaño de búfer pequeño requiere menos memoria, aumenta la velocidad a la que se deben vaciar los búferes.<br/> El tamaño de búfer predeterminado para los canales analíticos y de depuración es de 4 KB y para administrador y operativo es de 64 KB.<br/>                                                                                                                |
| [**clockType**](eventmanifestschema-clocktype-channelpublishingtype-element.md)     |                                                                   | Resolución del reloj que se usará al registrar la marca de tiempo para cada evento. Puede especificar SystemTime o QPC. SystemTime proporciona una marca de tiempo de baja resolución (10 milisegundos), pero es comparativamente menos costosa de recuperar. El valor predeterminado es SystemTime. <br/> El contador de rendimiento de consultas (QPC) proporciona una marca de tiempo de alta resolución (100 nanosegundos), pero es comparativamente más costoso de recuperar. Debe QPC si tiene altas tasas de eventos o si el consumidor combina eventos de distintos búferes.<br/>                                                                                                                                                                                                                                 |
| [**controlGuid**](eventmanifestschema-controlguid-channelpublishingtype-element.md) | [**GUIDType**](eventmanifestschema-guidtype-simpletype.md)       | Identifica el GUID de sesión para una sesión ETW que contiene eventos WPP. Esta configuración solo se permite para canales de tipo Debug. Estos canales no se pueden habilitar completamente con palabras clave establecidas en cero (0x0000000000000000). Deben habilitarse con palabras clave establecidas en 0xffffffffffffffff.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **fileMax**                                                                          | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Número máximo de veces que desea que el servicio cree un nuevo archivo de registro cuando el canal está habilitado (incluye cuando se reinicia el equipo). Si el valor es 0 o 1, el servicio sobrescribirá el archivo de registro cada vez que se habilite el canal y se pierdan los eventos anteriores. Si el valor es mayor que 1, el servicio creará un nuevo archivo de registro cada vez que se habilite el canal para conservar los eventos. El valor predeterminado es 1 y el máximo que puede especificar es 16.<br/> El servicio anexa un número decimal de tres dígitos entre 0 y fileMax 1 a cada nombre de archivo. Por ejemplo, *filename*.etl.xxx, donde xxx es el número decimal de tres dígitos. Los archivos se encuentran en %windir% \\ System32 \\ winevt \\ Logs.<br/> |
| [**Palabras clave**](eventmanifestschema-keywords-channelpublishingtype-element.md)       | [**UInt64Type**](eventmanifestschema-hexint64type-simpletype.md) | Máscara de bits que determina la categoría de eventos que se escriben en el canal. Si el valor del **atributo keywords** es 0, todos los eventos que escribe el proveedor se escriben en el canal; De lo contrario, solo los eventos que han definido una palabra clave que se incluye en **la** máscara de bits de palabras clave se escriben en el canal. El valor predeterminado es 0.<br/> Los canales de depuración que tienen el atributo controlGuid establecido deben establecer **el atributo keywords** en 0xFFFFFFFFFFFFFFFF.<br/> La sesión pasa el valor de palabras clave al proveedor cuando habilita el proveedor.<br/>                                                                                                                                                                            |
| [**Latencia**](eventmanifestschema-latency-channelpublishingtype-element.md)         | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Tiempo de espera antes de vaciar los búferes, en milisegundos. Si es cero, ETW vacía los búferes en cuanto se llenan. Si es distinto de cero, ETW vacía todos los búferes que contienen eventos basados en el valor incluso si el búfer no está lleno. Normalmente, desea vaciar los búferes solo cuando se llenan. Forzar el vaciado de los búferes puede aumentar el tamaño del archivo de registro con espacio de búfer no rellenado. El valor predeterminado es 1 segundo para los registros administrativos y operativos y 5 segundos para los registros analíticos y de depuración.<br/>                                                                                                                                                                                                                               |
| [**Nivel**](eventmanifestschema-level-channelpublishingtype-element.md)             | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Nivel de gravedad de los eventos que se escriben en el canal. El servicio escribe eventos en el canal que tienen un valor de nivel menor o igual que el valor especificado. El valor predeterminado es 0, lo que significa registrar eventos con cualquier valor de nivel.<br/> La sesión pasa el valor de nivel al proveedor cuando habilita el proveedor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**maxBuffers**](eventmanifestschema-maxbuffers-channelpublishingtype-element.md)   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Número máximo de búferes que se asignarán para la sesión. Normalmente, este valor es el número mínimo de búferes más veinte. Este valor debe ser mayor o igual que el valor especificado para minBuffers.<br/> El número máximo predeterminado de búferes para los canales analíticos y de depuración es de 10 KB y para administrador y operativo es de 64 KB.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**minBuffers**](eventmanifestschema-minbuffers-channelpublishingtype-element.md)   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Número mínimo de búferes que se asignarán para la sesión. El valor predeterminado es cero.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**sidType**](eventmanifestschema-sidtype-channelpublishingtype-element.md)         |                                                                   | Determina si se debe incluir un identificador de seguridad (SID) de la entidad de seguridad con cada evento escrito en el canal. Para incluir el SID con el evento , establezca este atributo en "Publishing". El SID se establece en función de la identidad del subproceso en el momento en que se escribe el evento. Si no desea incluir el SID con el evento , establezca este atributo en "None". El valor predeterminado es "Publishing".<br/>                                                                                                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Comentarios

Puede especificar esta información de publicación para los tipos de canal analítico y de depuración o para cualquier canal que especifique aislamiento personalizado.

Aunque puede especificar el nivel y las palabras clave, debe tener en cuenta que estos serán los únicos eventos que recibirá del proveedor para ese canal.

Cuando un búfer está lleno, ETW vacía el búfer en el archivo de registro. Si los búferes se rellenan más rápido de lo que se pueden vaciar, se asignan nuevos búferes y se agregan al grupo de búferes de la sesión, hasta el número máximo especificado. Más allá de este límite, la sesión descarta los eventos entrantes hasta que un búfer esté disponible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





