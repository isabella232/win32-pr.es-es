---
description: Al seleccionar una tarjeta de interfaz de red (NIC) registrada en un equipo local, puede usar un BLOB en filtro para omitir las NIC que no le interesan.
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: Especificación de un BLOB en filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8754b8f7ea5388b730fd2dfb65e26e24a906d648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686880"
---
# <a name="specifying-a-filter-blob"></a>Especificación de un BLOB en filtro

Al seleccionar una tarjeta de interfaz de red (NIC) registrada en un equipo local, puede usar un [*BLOB en filtro*](f.md) para omitir las NIC que no le interesan. Por ejemplo, puede restringir la búsqueda de un tipo específico de tarjeta (como ETHERNET) o una dirección MAC específica.

Durante la búsqueda de una NIC, cada entrada del BLOB en filtro debe coincidir con una entrada equivalente en el BLOB NPP que representa la NIC. Los blobs de filtro también pueden ser [*blobs especiales*](s.md).

Cuando se llama a la función [**GetNPPBlobFromUI**](getnppblobfromui.md) , el BLOB de filtro restringe las NIC que se muestran en el cuadro de diálogo **seleccionar una red** . Cuando se llama a la función [**GetNPPBlobTable**](getnppblobtable.md) , el BLOB de filtro restringe las NIC devueltas en la tabla de blobs.

Para usar el filtro, debe crear un BLOB de filtro, establecer los valores de las propiedades que desea filtrar (incluidas las entradas de BLOBs especiales) y, a continuación, especificar el filtro de BLOBs y una llamada a la función [**GetNPPBlobTable**](getnppblobtable.md) o [**GetNPPBlobFromUI**](getnppblobfromui.md) .



| Para obtener información acerca de                                 | Vea                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Cómo seleccionar una NIC registrada en un equipo local | [Selección de una NIC registrada](selecting-a-registered-nic.md)                                         |
| Recuperación de una tabla BLOB de NPP                       | [Selección de una NIC de una tabla BLOB NPP devuelta](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



