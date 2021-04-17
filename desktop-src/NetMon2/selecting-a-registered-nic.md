---
description: Para seleccionar una de las NIC registradas en el equipo local, llame a la función GetNPPBlobFromUI.
ms.assetid: ca1fb07f-7eee-419f-b25d-49718d02fc7d
title: Selección de una NIC registrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b7047d5bbb46797210e18782c672cfd81b9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677639"
---
# <a name="selecting-a-registered-nic"></a>Selección de una NIC registrada

Para seleccionar una de las NIC registradas en el equipo local, llame a la función [**GetNPPBlobFromUI**](getnppblobfromui.md) . Esta función usa la interfaz de usuario de Monitor de red para mostrar las NIC registradas y devuelve el BLOB NPP que representa la NIC seleccionada. Puede mostrar todas las NIC registradas en el equipo local o un conjunto más pequeño de NIC filtradas. Para filtrar las NIC que se muestran, proporcione un [*BLOB de filtro*](f.md) cuando se realice la llamada.

> [!Note]  
> Cuando se llama a la función [**GetNPPBlobFromUI**](getnppblobfromui.md) , el [*buscador de NPP*](n.md) se comunica con los archivos dll de NPP para obtener las estructuras de blobs NPP que representan las NIC registradas. Para obtener más información y un procedimiento sobre cómo usar la interfaz de usuario de Monitor de red directamente, vea el tema "seleccionar un cuadro de diálogo de red" en la ayuda en pantalla de Monitor de red.

 

Cuando se llama a la función [**GetNPPBlobFromUI**](getnppblobfromui.md) , aparece el cuadro de diálogo **seleccionar una red** . En ella, puede ver los detalles de los NPPs registrados en el equipo local. Esta información incluye NPPs locales y NPPs remoto. En el cuadro de diálogo, puede seleccionar una NIC específica y ver los detalles de su estructura de BLOBs NPP asociada.

En la ilustración siguiente se muestra la configuración típica de un NPP de NDIS proporcionado por Monitor de red.

![configuración típica de un NPP de NDIS proporcionado por el monitor de red](images/networkdb.png)

En la tabla siguiente se enumeran los temas que describen cada método de selección de NIC.



| Para información acerca de                                                                          | Vea                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Cómo especificar un filtro que limite las NIC que se muestran en el cuadro de diálogo **seleccionar una red** . | [Especificación de un BLOB en filtro](specifying-a-filter-blob.md)                                             |
| Cómo seleccionar una NIC mediante una llamada a la función [**GetNPPBlobFromUI**](getnppblobfromui.md) .      | [Selección de una NIC mediante GetNPPBlobFromUI](getnppblobfromui.md)                                       |
| Cómo seleccionar una NIC de una tabla BLOB de NPP proporcionada.                                            | [Selección de una NIC de una tabla BLOB de NPP proporcionada](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



