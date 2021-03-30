---
description: En el fragmento de código siguiente se muestra cómo solicitar y establecer una dirección de multidifusión para una conferencia.
ms.assetid: faff57a9-88b3-45ce-bf9e-3f7087dfd1fd
title: Adquisición de una dirección de multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb451bb403002a4b2dc347abf51e587d8ea02a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154052"
---
# <a name="acquiring-a-multicast-address"></a>Adquisición de una dirección de multidifusión

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

En el fragmento de código siguiente se muestra cómo solicitar y establecer una dirección de multidifusión para una conferencia.

Por motivos de simplicidad, este fragmento muestra la asignación de una dirección de multidifusión a un elemento multimedia. En realidad, la selección de un ámbito, la solicitud de dirección de multidifusión y la asignación se realizarán para cada elemento multimedia implicado en la Conferencia.

Este fragmento supone que ya se ha realizado la [conexión a un servidor ILS](connecting-to-an-ils-server.md) . Las operaciones que se muestran aquí se realizarían en la sección "modificar la configuración si es necesario" de [creación de un anuncio de conferencia](creating-a-conference-announcement.md).


```C++
// If ( hr != S_OK ) process the error here.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces COM multidifusión](multicast-com-interfaces.md)
</dt> <dt>

[**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)
</dt> <dt>

[**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)
</dt> <dt>

[**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)
</dt> <dt>

[**IEnumMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)
</dt> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> <dt>

[**IEnumBstr**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr)
</dt> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

 



