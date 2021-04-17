---
description: Las acciones personalizadas se invocan de la misma manera que las acciones estándar, ya sea mediante invocación explícita o durante la ejecución de una tabla de secuencia.
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: Invocar acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f1e9a575d32cbb8fe22323d4a741eb7936ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688542"
---
# <a name="invoking-custom-actions"></a>Invocar acciones personalizadas

Las acciones personalizadas se invocan de la misma manera que las acciones estándar, ya sea mediante invocación explícita o durante la ejecución de una tabla de secuencia. Hay dos métodos para llamar a las acciones:

-   Llame a la acción especificada directamente con la función [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) .
-   Una acción de nivel superior llama a la tabla de secuencias que contiene la acción personalizada. Para obtener más información sobre la programación de una acción personalizada en una tabla de secuencia, consulte [secuenciación de acciones personalizadas](sequencing-custom-actions.md).

Cuando el instalador obtiene un nombre de acción de la función [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) , o de una tabla de secuencia, busca primero una acción estándar de ese nombre. Si no encuentra la acción estándar, el instalador consulta la [tabla CustomAction](customaction-table.md) para comprobar si la acción especificada es una acción personalizada. Si la acción especificada no es una acción personalizada, el instalador consulta la [tabla de diálogo](dialog-table.md) de un cuadro de diálogo.

 

 



