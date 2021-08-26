---
title: Tipo complejo ChannelLoggingType
description: Define las propiedades del archivo de registro que hace una copia de seguridad del canal, como su capacidad y si es secuencial o circular. | Tipo complejo ChannelLoggingType
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- ChannelLoggingType, tipo complejo EventLog
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e696837b1132a0b82ad428e7404892ae73de88e4435325d988b7936b3a6ba534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032285"
---
# <a name="channelloggingtype-complex-type"></a>Tipo complejo ChannelLoggingType

Define las propiedades del archivo de registro que hace una copia de seguridad del canal, como su capacidad y si es secuencial o circular.

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
| [**Autobackup**](eventmanifestschema-autobackup-channelloggingtype-element.md) | boolean                                                           | Determina si se va a crear un nuevo archivo de registro cuando el archivo de registro actual alcance su tamaño máximo. Establezca en **true** para solicitar que el servicio cree un nuevo archivo cuando el archivo de registro alcance su tamaño máximo; de lo contrario, **false**. Puede establecer [**autoBackup en**](eventmanifestschema-autobackup-channelloggingtype-element.md) **true solo** si [**retention**](eventmanifestschema-retention-channelloggingtype-element.md) está establecido en **true.** El valor predeterminado es **false**.<br/> No hay ningún límite en el número de archivos de copia de seguridad que el servicio puede crear (limitado solo por el espacio disponible en disco). Los nombres de archivo de copia de seguridad tienen el formato Archive-*channelName* timestamp .evtx y se encuentran en la carpeta - %windir% \\ System32 \\ winevt \\ Logs.<br/> |
| [**Maxsize**](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [**UInt64Type**](eventmanifestschema-hexint64type-simpletype.md) | Tamaño máximo, en bytes, del archivo de registro. El valor predeterminado (y mínimo) es 1 MB. Si el tamaño del registro físico es menor que el tamaño máximo configurado y se requiere espacio adicional en el registro para almacenar eventos, el servicio asignará otro bloque de espacio incluso si el tamaño físico resultante del registro será mayor que el tamaño máximo configurado. El servicio asigna bloques de 1 MB para que el tamaño físico pueda crecer hasta 1 MB más que el tamaño máximo configurado. <br/>                                                                                                                                                                                                                                                      |
| [**Retención**](eventmanifestschema-retention-channelloggingtype-element.md)   | boolean                                                           | Determina si el archivo de registro es un archivo de registro secuencial o circular. Se establece **en true para** un archivo de registro secuencial y false **para** un archivo de registro circular. El valor predeterminado es **false para** los tipos de canal administrador y operativo y **true** para los tipos de canal analítico y de depuración.<br/> Para consultar un registro circular, primero debe deshabilitar el canal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Comentarios

Puede especificar el atributo **maxSize** para cualquier tipo de canal.

Solo puede especificar el **atributo autoBackup** para los tipos de canal Administrador y Operativo.

Puede establecer el atributo **de retención** en false (registro circular) para los tipos de canal Admin y Operational. Puede establecer  el atributo de retención en false (registro circular) para los tipos de canal Analítico y Depurar, pero para ver los eventos en el Windows Visor de eventos, primero debe deshabilitar el canal. Tenga en cuenta que al habilitar el canal de nuevo, los eventos se quitan del canal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





