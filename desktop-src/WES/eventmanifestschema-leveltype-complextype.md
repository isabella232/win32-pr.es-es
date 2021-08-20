---
title: Tipo complejo LevelType
description: Define un valor de gravedad que determina el nivel de detalle de los eventos que se registran.
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- EventLog de tipo complejo LevelType
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b80e034f6b77f869207ecb785edbb935841eed2dba6bde73ad88c441dabf15cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055943"
---
# <a name="leveltype-complex-type"></a>Tipo complejo LevelType

Define un valor de gravedad que determina el nivel de detalle de los eventos que se registran.

``` syntax
<xs:complexType name="LevelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nombre    | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                        |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nombre para mostrar localizado del nivel. La cadena de mensaje hace referencia a una cadena localizada en la [**sección stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto. <br/>                                                                                                    |
| name    | **QName**                                                         | Nombre que se va a asignar a este nivel. Este nombre debe ser único dentro del ámbito del proveedor.<br/>                                                                                                                                                                                                            |
| símbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Símbolo que se usará para hacer referencia al nivel de la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) usa el símbolo para crear una constante para el nivel en el archivo de encabezado que genera el compilador. Si no especifica un símbolo, el compilador genera uno automáticamente.<br/> |
| value   | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valor de nivel. Puede especificar valores en el intervalo de 16 a 255. Para obtener valores de nivel predefinidos, vea Comentarios.<br/>                                                                                                                                                                                               |



## <a name="remarks"></a>Comentarios

Estos son los valores de nivel predefinidos que puede usar. Estos valores se definen en el archivo Winmeta.xml que se incluye en Windows SDK.



| Nombre              | Valor | Símbolo                    | Descripción                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| win:Critical      | 1     | NIVEL CRÍTICO DE WINEVENT \_ \_ | Identifica un evento de salida o finalización anómalo.<br/>            |
| win:Error         | 2     | ERROR DE \_ NIVEL DE WINEVENT \_    | Identifica un evento de error grave.<br/>                             |
| win:Warning       | 3     | ADVERTENCIA DE \_ NIVEL DE \_ WINEVENT  | Identifica un evento de advertencia, como un error de asignación.<br/>    |
| win:Informational | 4     | INFORMACIÓN DE NIVEL \_ DE \_ WINEVENT     | Identifica un evento que no es de error, como un evento de entrada o salida.<br/> |
| win:Verbose       | 5     | NIVEL DE \_ WINEVENT \_ DETALLADO  | Identifica un evento de seguimiento detallado.<br/>                           |



 

Los números más altos implican que también se obtienen niveles más bajos. Por ejemplo, si especifica win:Warning, recibirá todos los eventos de advertencia, error y críticos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





