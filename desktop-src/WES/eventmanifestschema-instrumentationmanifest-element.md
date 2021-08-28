---
title: elemento instrumentationManifest
description: Nodo raíz del manifiesto.
ms.assetid: cb7b5201-be11-48f9-bcca-4606904f0c1d
keywords:
- elemento instrumentationManifest EventLog
topic_type:
- apiref
api_name:
- instrumentationManifest
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7dac9ab8c8aa2a6caeacf43023c4995be69f293affd5dd5a904d7fb96d710266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343736"
---
# <a name="instrumentationmanifest-element"></a>elemento instrumentationManifest

Nodo raíz del manifiesto.

``` syntax
<xs:element name="instrumentationManifest">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="InstrumentationManifestType"
            >
                <xs:choice
                    maxOccurs="3"
                >
                    <xs:choice>
                        <xs:element name="metadata"
                            type="MetadataType"
                         />
                        <xs:element name="instrumentation"
                            type="InstrumentationType"
                         />
                    </xs:choice>
                    <xs:element name="localization"
                        type="LocalizationType"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:choice>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                        | Tipo                                                                               | Descripción                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Instrumentación**](eventmanifestschema-instrumentation-instrumentationmanifest-element.md) | [**InstrumentationType**](eventmanifestschema-instrumentationtype-complextype.md) | En esta sección se definen uno o varios proveedores de eventos y los eventos que registra.<br/>                                                                                                                                                                                                                     |
| [**Localización**](eventmanifestschema-localization-instrumentationmanifest-element.md)       | [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md)       | En esta sección se definen las cadenas de mensaje localizadas que los consumidores usan para mostrar. Por ejemplo, esta sección contendrá la cadena de mensaje localizada para el nombre del proveedor, los eventos que defina y los atributos de evento que defina, como canales, tareas y códigos de operación.<br/> |
| [**Metadatos**](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)               | En esta sección se definen los tipos de metadatos que pueden usar otros manifiestos. Para obtener un ejemplo, consulte el archivo Winmeta.xml incluido en la \\ carpeta Include del SDK Windows.<br/>                                                                                                                                    |



## <a name="remarks"></a>Comentarios

El **elemento instrumentationManifest** debe contener los siguientes espacios de nombres:

<dl> xmlns=" https://schemas.microsoft.com/win/2004/08/events "  
xmlns:win=" https://manifests.microsoft.com/win/2004/08/windows/events "  
xmlns:xs=" https://www.w3.org/2001/XMLSchema "  
</dl>

Un manifiesto debe contener una sección de instrumentación y una sección de localización. La sección de instrumentación y la sección de metadatos son mutuamente excluyentes (no se pueden definir ambos en el mismo manifiesto). Aunque puede crear un manifiesto que contenga una sección de metadatos, el servicio no lo usará; los únicos metadatos que el servicio reconoce son los metadatos que se encuentran en el Winmeta.xml archivo.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el esqueleto de un manifiesto de instrumentación totalmente definido.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChanel .../>
                    <channel .../>
                </channels>
                <levels>
                <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <namedQueries>
                    <patternMap ...>
                        <map .../>
                    </patternMap>  
                </namedQueries>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





