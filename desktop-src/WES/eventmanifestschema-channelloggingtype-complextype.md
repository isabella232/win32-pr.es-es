---
title: Tipo complejo de ChannelLoggingType
description: Define las propiedades del archivo de registro que respalda el canal, como su capacidad y si son secuenciales o circulares. | Tipo complejo de ChannelLoggingType
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- ChannelLoggingType tipo complejo EventLog
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cfaf6dfa225799befcd0c7fb068c0f779ea33eb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104157116"
---
# <a name="channelloggingtype-complex-type"></a>Tipo complejo de ChannelLoggingType

Define las propiedades del archivo de registro que respalda el canal, como su capacidad y si son secuenciales o circulares.

``` syntax
<xs:complexType name="ChannelLoggingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="autoBackup"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="retention"
            type="boolean"
            default="0"
            minOccurs="0"
         />
        <xs:element name="maxSize"
            type="UInt64Type"
            default="1048576"
            minOccurs="0"
         />
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



| Elemento                                                                         | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Seguridad automatizada**](eventmanifestschema-autobackup-channelloggingtype-element.md) | boolean                                                           | Determina si se debe crear un nuevo archivo de registro cuando el archivo de registro actual alcanza su tamaño máximo. Establézcalo en **true** para solicitar que el servicio cree un nuevo archivo cuando el archivo de registro alcance su tamaño máximo; en caso contrario, **false**. Puede establecer [**AutoBackup**](eventmanifestschema-autobackup-channelloggingtype-element.md) en **true** solo si la [**retención**](eventmanifestschema-retention-channelloggingtype-element.md) está establecida en **true**. El valor predeterminado es **false**.<br/> No hay ningún límite en cuanto al número de archivos de copia de seguridad que puede crear el servicio (limitado solo por el espacio en disco disponible). Los nombres de archivo de copia de seguridad tienen el formato Archive-*channelName* - *timestamp*. evtx y se encuentran en la carpeta% WINDIR% \\ system32 \\ winevt \\ logs.<br/> |
| [**Tamañomáximo**](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [**UInt64Type**](eventmanifestschema-hexint64type-simpletype.md) | Tamaño máximo, en bytes, del archivo de registro. El valor predeterminado (y el mínimo) es 1 MB. Si el tamaño de registro físico es menor que el tamaño máximo configurado y se requiere espacio adicional en el registro para almacenar los eventos, el servicio asignará otro bloque de espacio aunque el tamaño físico resultante del registro sea mayor que el tamaño máximo configurado. El servicio asigna bloques de 1 MB para que el tamaño físico pueda crecer hasta un máximo de 1 MB mayor que el tamaño máximo configurado. <br/>                                                                                                                                                                                                                                                      |
| [**políticas**](eventmanifestschema-retention-channelloggingtype-element.md)   | boolean                                                           | Determina si el archivo de registro es un archivo de registro secuencial o circular. Establézcalo en **true** para un archivo de registro secuencial y en **false** para un archivo de registro circular. El valor predeterminado es **false** para los tipos de canal operativo y de administración y **true** para los tipos de canal de depuración y análisis.<br/> Para consultar un registro circular, primero debe deshabilitar el canal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Observaciones

Puede especificar el atributo **MaxSize** para cualquier tipo de canal.

Solo puede especificar el atributo **AutoBackup** para los tipos de canal operativo y de administración.

Puede establecer el atributo de **retención** en falso (registro circular) para los tipos de canal operativo y de administración. Puede establecer el atributo de **retención** en false (registro circular) para los tipos de canal analítico y de depuración, pero para ver los eventos en el visor de eventos de Windows, deberá deshabilitar primero el canal. Tenga en cuenta que cuando se vuelve a habilitar el canal, los eventos se quitan del canal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





