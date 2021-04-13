---
description: Especifica si el cargador de topología enumera los tipos de medios proporcionados por el origen de medios.
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015042bbf9994f81058c621239224196e6ec9ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360261"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a>\_Enumeración de topología MF \_ atributo de \_ tipos de origen \_

Especifica si el cargador de topología enumera los tipos de medios proporcionados por el origen de medios.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Use uno de los siguientes valores.



| Value                                                                                                                                    | Significado                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | No enumere los tipos de medios de origen.<br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | Enumera los tipos de medios de origen.<br/>        |



 

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Observaciones

Cada secuencia de un origen multimedia puede ofrecer más de un tipo de medio. La lista de tipos se enumera a través de la interfaz [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) en el descriptor de flujo.

El orden en el que el cargador de topología intenta los tipos de medios de un origen multimedia se controla mediante dos atributos:

-   El \_ atributo MF Topology \_ enumerar \_ \_ tipos de origen en la topología.
-   El atributo de [**\_ método de \_ conexión \_ MF TOPONODE**](mf-toponode-connect-method-attribute.md) en el nodo de origen.

Si el \_ atributo MF Topology \_ enumerar \_ tipos de origen \_ es **false** o no está establecido, el cargador de topología usa el tipo de medio actual de la secuencia. No enumera la lista de tipos posibles. Si el tipo de medio actual es incompatible con el nodo de la topología de bajada y no se puede encontrar una combinación de descodificadores/convertidores, se produce un error en la resolución de topología.

Si el \_ atributo MF Topology \_ enumerar \_ tipos de origen \_ es **true**, el cargador de topología enumera los tipos de medios del origen hasta que encuentra un tipo compatible. En ese caso, el orden exacto de las operaciones depende de si el atributo de [**\_ método de \_ conexión \_ MF TOPONODE**](mf-toponode-connect-method-attribute.md) en el nodo de origen incluye la marca **MF \_ Connect \_ Resolve \_ independiente de \_ OUTPUTTYPES** .

Si \_ \_ los tipos de origen de la enumeración MF \_ \_ son **true** y se establece la marca **MF \_ Connect de \_ \_ \_ OUTPUTTYPES independiente** , el cargador de topología agotará cada tipo de medio antes de pasar al siguiente, como se indica a continuación:

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

Si \_ la enumeración de la topología MF \_ \_ \_ es **true** , pero no se establece **MF \_ Connect \_ Resolve \_ Independent \_ OUTPUTTYPES** , el cargador de topología probará una conexión directa con cada tipo de medio y, a continuación, probará cada tipo de medio con convertidores y, por último, probará cada tipo de medio con descodificadores:

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

Si \_ \_ se enumeran \_ \_ los tipos de origen de la topología MF es **false**, se omite la marca **MF \_ Connect \_ Resolve \_ Independent \_ OUTPUTTYPES** .

El valor predeterminado de MF \_ Topology \_ Enumerate \_ \_ Types de origen es **false**, por compatibilidad con las aplicaciones existentes.

La constante GUID para este atributo se exporta desde mfuuid. lib.

### <a name="example"></a>Ejemplo

Este es un ejemplo en el que se muestra la marca **MF \_ Connect \_ Resolve \_ Independent \_ OUTPUTTYPES** . Supongamos que la topología tiene el \_ atributo MF Topology \_ enumerar \_ \_ tipos de origen establecido en **true**.

El origen de medios ofrece los siguientes tipos:

-   T1, T2, T3

El receptor de medios acepta los siguientes tipos:

-   T3, T4

Caso 1: se establece la marca **MF \_ Connect \_ \_ \_ OUTPUTTYPES independiente** .

1.  El cargador de topología intenta una conexión directa con T1. El receptor rechaza T1.
2.  El cargador de topología inserta un descodificador que acepta T1 y salidas T4. El receptor acepta T4.
3.  La topología final contiene: origen de medios → descodificador → receptor de medios.

Caso 2: no se ha establecido la marca.

1.  El cargador de topología intenta una conexión directa con T1. El receptor rechaza T1.
2.  El cargador de topología intenta una conexión directa con T2. El receptor rechaza T2.
3.  El cargador de topología intenta una conexión directa con T3. El receptor acepta T3.
4.  La topología final contiene: origen de medios → receptor de medios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> </dl>

 

 




