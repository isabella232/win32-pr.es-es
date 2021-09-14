---
title: Tipo complejo ImportChannelType
description: Identifica un canal definido por otro proveedor o en un manifiesto que contiene una sección de metadatos.
ms.assetid: da14d837-0ed8-4d85-9820-46c77753768d
keywords:
- EventLog de tipo complejo ImportChannelType
topic_type:
- apiref
api_name:
- ImportChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7500d52179c3282c7f15dcdd5dd5a32620bbc076
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241094"
---
# <a name="importchanneltype-complex-type"></a>Tipo complejo ImportChannelType

Identifica un canal definido por otro proveedor o en un manifiesto que contiene una sección de metadatos.

``` syntax
<xs:complexType name="ImportChannelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="chid"
                type="token"
                use="optional"
             />
            <xs:attribute name="name"
                type="anyURI"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nombre   | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                            |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| chid   | token                                                             | Identificador que identifica de forma única el canal en la lista de canales que el proveedor define o importa. Use este valor al hacer referencia a este canal en una definición de evento. Si no especifica un identificador de canal, use el nombre del canal para hacer referencia a este canal en una definición de evento.<br/>  |
| name   | anyURI                                                            | Nombre del canal que se importará.<br/>                                                                                                                                                                                                                                                                          |
| símbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Símbolo que se usará para hacer referencia al canal en la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) usa el símbolo para crear una constante para el canal en el archivo de encabezado que genera el compilador. Si no especifica un símbolo, el compilador genera uno automáticamente.<br/> |



## <a name="remarks"></a>Observaciones

El manifiesto que definió el canal importado debe instalarse antes de que el proveedor escriba eventos; De lo contrario, los eventos no se pueden escribir en el canal (la operación de escritura se realiza correctamente, los eventos simplemente no se escriben en el canal).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





