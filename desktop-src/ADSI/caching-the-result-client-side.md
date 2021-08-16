---
title: Almacenamiento en caché del resultado (lado cliente)
description: El almacenamiento en caché del lado cliente almacena el conjunto de resultados en la memoria del cliente, lo que proporciona mejoras de rendimiento para el lado cliente.
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- Almacenamiento en caché del ADSI de resultados (cliente)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c2394c4f9e3213261bc52e15ada6fa9416703706fedeccaf144493821133e1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840505"
---
# <a name="caching-the-result-client-side"></a>Almacenamiento en caché del resultado (lado cliente)

El almacenamiento en caché del lado cliente almacena el conjunto de resultados en la memoria del cliente, lo que proporciona mejoras de rendimiento para el lado cliente. Un cliente puede volver a visitar un objeto repetidamente sin varios viajes al servidor. De forma predeterminada, ADSI almacena en caché el conjunto de resultados para los clientes. Esto permite que ADSI proporcione a los clientes SQL compatibilidad con cursores de tipo "me gusta". Puede recorrer en iteración un conjunto de resultados determinado varias veces.

ADSI también permite a los clientes desactivar la memoria caché para reducir los requisitos de memoria. Si el almacenamiento en caché del lado cliente está deshabilitado, el cliente no mantiene el conjunto de resultados en memoria. Cada fila se libera después de que la aplicación la recupere. Deshabilitar el almacenamiento en caché del lado cliente puede ser útil para reducir los requisitos de memoria del lado cliente en casos como cuando se pretende realizar un solo paso a través del conjunto de resultados. Sin embargo, cuando los clientes deciden no almacenar en caché el resultado, se da por hecho la compatibilidad con cursores.

Para obtener más información sobre el almacenamiento en caché de resultados con una interfaz de búsqueda específica, vea:

-   [Almacenamiento en caché de resultados con IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [Buscar con objetos ActiveX datos](searching-with-activex-data-objects-ado.md)
-   [Búsqueda con OLE DB](searching-with-ole-db.md)

 

 




