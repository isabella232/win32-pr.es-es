---
description: Al seleccionar una tarjeta de interfaz de red (NIC) registrada en un equipo local, puede usar un BLOB de filtro para pasar por alto las NIC que no le interesan.
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: Especificar un blob en filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486a5dfe318da50a921560c92b82a3a3bf05a9434a4ac609b7f135afd7bf5a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555355"
---
# <a name="specifying-a-filter-blob"></a>Especificar un blob en filtros

Al seleccionar una tarjeta de interfaz de red (NIC) registrada en un equipo local, puede usar un [*BLOB*](f.md) de filtro para pasar por alto las NIC que no le interesan. Por ejemplo, puede restringir la búsqueda de un tipo específico de tarjeta (como ETHERNET) o una dirección MAC específica.

Durante la búsqueda de una NIC, cada entrada del blob de filtro debe coincidir con una entrada equivalente en el BLOB de NPP que representa la NIC. Los BLOB de filtro también pueden ser [*blobs especiales.*](s.md)

Cuando se llama **a** la función [**GetNPPBlobFromUI,**](getnppblobfromui.md) el blob de filtro restringe las NIC que se muestran en el cuadro de diálogo Seleccionar una red. Cuando se llama a la función [**GetNPPBlobTable,**](getnppblobtable.md) el blob de filtro restringe las NIC devueltas en la tabla BLOB.

Para usar el filtro, debe crear un BLOB de filtro, establecer los valores de las propiedades por las que desea filtrar (incluidas las entradas blob especiales) y, a continuación, especificar el filtro BLOB y una llamada a la función [**GetNPPBlobTable**](getnppblobtable.md) u [**GetNPPBlobFromUI.**](getnppblobfromui.md)



| Para obtener información acerca de                                 | Vea                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Selección de una NIC registrada en un equipo local | [Selección de una NIC registrada](selecting-a-registered-nic.md)                                         |
| Recuperación de una tabla BLOB de NPP                       | [Selección de una NIC de una tabla blob de NPP devuelta](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



