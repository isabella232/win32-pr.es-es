---
title: Tipo complejo de LevelType
description: Define un valor de gravedad que determina el nivel de detalle de los eventos que se registran.
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- LevelType tipo complejo EventLog
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 237b38890283769e9aac20c9b3a3703ff4b72d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149920"
---
# <a name="leveltype-complex-type"></a>Tipo complejo de LevelType

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
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | El nombre para mostrar adaptado para el nivel. La cadena de mensaje hace referencia a una cadena localizada en la sección [**stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto. <br/>                                                                                                    |
| name    | **QName**                                                         | Nombre que se va a asignar a este nivel. Este nombre debe ser único dentro del ámbito del proveedor.<br/>                                                                                                                                                                                                            |
| símbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Símbolo que se va a usar para hacer referencia al nivel de la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para el nivel en el archivo de encabezado que genera el compilador. Si no especifica un símbolo, el compilador genera uno automáticamente.<br/> |
| value   | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valor de nivel. Puede especificar valores comprendidos entre 16 y 255. Para los valores de nivel predefinidos, vea la sección Comentarios.<br/>                                                                                                                                                                                               |



## <a name="remarks"></a>Observaciones

A continuación se muestran los valores de nivel predefinidos que puede usar. Estos valores se definen en el archivo Winmeta.xml que se incluye en el Windows SDK.



| Nombre              | Value | Símbolo                    | Descripción                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| win:Critical      | 1     | \_nivel \_ crítico de WINEVENT | Identifica un evento de salida o finalización anormal.<br/>            |
| win:Error         | 2     | \_error de nivel de WINEVENT \_    | Identifica un evento de error grave.<br/>                             |
| win:Warning       | 3     | \_Advertencia de nivel de WINEVENT \_  | Identifica un evento de advertencia, como un error de asignación.<br/>    |
| win:Informational | 4     | \_información de nivel de WINEVENT \_     | Identifica un evento que no es un error, como una entrada o un evento de salida.<br/> |
| win:Verbose       | 5     | \_nivel \_ detallado de WINEVENT  | Identifica un evento de seguimiento detallado.<br/>                           |



 

Los números más altos implican también la obtención de niveles inferiores. Por ejemplo, si especifica Win: Warning, recibirá todos los eventos de advertencia, error y crítico.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





