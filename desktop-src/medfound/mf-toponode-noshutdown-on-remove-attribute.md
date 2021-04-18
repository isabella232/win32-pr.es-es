---
description: Especifica cómo la sesión multimedia apaga un objeto en la topología.
ms.assetid: 53b4faba-860f-4d6c-a145-09ea4ae63b8b
title: MF_TOPONODE_NOSHUTDOWN_ON_REMOVE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bec06d2190491167d978250270503e5e6506d58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705795"
---
# <a name="mf_toponode_noshutdown_on_remove-attribute"></a>MF \_ TOPONODE \_ noshutdown \_ en el \_ atributo Remove

Especifica cómo la sesión multimedia apaga un objeto en la topología.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los siguientes tipos de nodo topología:

-   Nodos de salida
-   Cualquier nodo de transformación que contenga una transformación de Media Foundation *asincrónica* (MFT).

El atributo puede tener los valores siguientes:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>TRUE</strong></td>
<td>Cuando la sesión multimedia cambia a una nueva topología o borra la topología actual, no cierra el objeto que pertenece a este nodo de topología.</td>
</tr>
<tr class="even">
<td><strong>FALSE</strong></td>
<td>Cuando la sesión multimedia cambia a una nueva topología o borra la topología actual, cierra el objeto de nodo, como se indica a continuación:
<ul>
<li>Nodos de salida: la sesión llama a <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink:: Shutdown</strong></a> en el receptor de medios.</li>
<li>Transformar nodos: la sesión llama a <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown:: Shutdown</strong></a> en la MFT.</li>
</ul></td>
</tr>
</tbody>
</table>



 

El valor predeterminado es **true**.

Si la aplicación pone en cola varias topologías, es una buena idea establecer este atributo en **false**. De lo contrario, es posible que los objetos de la topología no se cierren correctamente.

Este atributo no se aplica cuando la aplicación cierra la sesión multimedia mediante una llamada a [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown). Cuando se cierra la sesión multimedia, siempre cierra los receptores de medios y MFTs asincrónicos en la topología actual.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs asincrónico](asynchronous-mfts.md)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




