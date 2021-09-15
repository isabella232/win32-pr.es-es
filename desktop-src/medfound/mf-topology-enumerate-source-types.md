---
description: Especifica si el cargador de topología enumera los tipos de medios proporcionados por el origen de medios.
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015042bbf9994f81058c621239224196e6ec9ac8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360456"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a>ATRIBUTO \_ ENUMERATE SOURCE TYPES DE LA TOPOLOGÍA \_ \_ \_ DE MF

Especifica si el cargador de topología enumera los tipos de medios proporcionados por el origen de medios.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Use uno de los siguientes valores.



| Value                                                                                                                                    | Significado                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE**</dt> </dl> | No enumere los tipos de medios de origen.<br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE**</dt> </dl>    | Enumerar los tipos de medios de origen.<br/>        |



 

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Observaciones

Cada secuencia de un origen multimedia puede ofrecer más de un tipo de medio. La lista de tipos se enumera a través de la [**interfaz IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) en el descriptor de secuencia.

El orden en que el cargador de topologías intenta los tipos de medios de un origen multimedia se controla mediante dos atributos:

-   El atributo \_ TOPOLOGY DE MF \_ ENUMERATE \_ SOURCE TYPES en \_ la topología.
-   Atributo [**MF \_ TOPONODE \_ CONNECT \_ METHOD**](mf-toponode-connect-method-attribute.md) en el nodo de origen.

Si el atributo ENUMERATE SOURCE TYPES de MF TOPOLOGY es FALSE o no está establecido, el cargador de topologías usa el tipo de medio actual \_ \_ de la \_ \_ secuencia.  No enumera la lista de tipos posibles. Si el tipo de medio actual no es compatible con el nodo de topología de bajada y no se encuentra ninguna combinación de descodificadores o convertidores, se produce un error en la resolución de la topología.

Si el atributo ENUMERATE SOURCE TYPES de MF TOPOLOGY es TRUE, el cargador de topologías enumera los tipos de medios del origen hasta que encuentra \_ \_ un tipo \_ \_ compatible.  En ese caso, el orden exacto de las operaciones depende de si el atributo [**MF \_ TOPONODE \_ CONNECT \_ METHOD**](mf-toponode-connect-method-attribute.md) del nodo de origen incluye la marca **MF CONNECT RESOLVE INDEPENDENT \_ \_ \_ \_ OUTPUTTYPES.**

Si ENUMERATE SOURCE TYPES de MF TOPOLOGY es TRUE y la marca \_ MF CONNECT RESOLVE INDEPENDENT \_ \_ \_ **\_ \_ \_ \_ OUTPUTTYPES** está establecida,  el cargador de topología agota cada tipo de medio antes de pasar al siguiente, como se muestra a continuación:

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

Si ENUMERATE SOURCE TYPES de MF TOPOLOGY es TRUE pero \_ MF CONNECT RESOLVE INDEPENDENT \_ \_ \_ **\_ \_ \_ \_ OUTPUTTYPES**  no está establecido, el cargador de topologías intenta una conexión directa con cada tipo de medio, prueba cada tipo de medio con convertidores y, por último, prueba cada tipo de medio con descodificadores:

``` syntax
foreach media type T
    connect directly using T
if failed,
    foreach media type T
        connect with converters using T
if failed
    foreach media type T
        connect with decoders using T
```

Si MF TOPOLOGY ENUMERATE SOURCE TYPES es FALSE , se omite la marca \_ MF CONNECT RESOLVE \_ INDEPENDENT \_ \_ **\_ \_ \_ \_ OUTPUTTYPES.** 

El valor predeterminado de MF \_ TOPOLOGY \_ ENUMERATE \_ SOURCE TYPES es \_ **FALSE,** por compatibilidad con las aplicaciones existentes.

La constante GUID para este atributo se exporta desde mfuuid.lib.

### <a name="example"></a>Ejemplo

Este es un ejemplo que muestra la marca **MF CONNECT RESOLVE INDEPENDENT \_ \_ \_ \_ OUTPUTTYPES.** Suponga que la topología tiene el atributo ENUMERATE SOURCE TYPES de MF \_ TOPOLOGY \_ establecido en \_ \_ **TRUE.**

El origen de medios ofrece los siguientes tipos:

-   T1, T2, T3

El receptor de medios acepta los siguientes tipos:

-   T3, T4

Caso 1: se establece la marca **MF CONNECT RESOLVE INDEPENDENT \_ \_ \_ \_ OUTPUTTYPES.**

1.  El cargador de topologías intenta una conexión directa con T1. El receptor rechaza T1.
2.  El cargador de topología inserta un descodificador que acepta T1 y genera la salida T4. El receptor acepta T4.
3.  La topología final contiene: origen de medios → descodificador → receptor multimedia.

Caso 2: la marca no está establecida.

1.  El cargador de topologías intenta una conexión directa con T1. El receptor rechaza T1.
2.  El cargador de topologías intenta una conexión directa con T2. El receptor rechaza T2.
3.  El cargador de topologías intenta una conexión directa con T3. El receptor acepta T3.
4.  La topología final contiene: origen de medios → receptor multimedia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> </dl>

 

 




