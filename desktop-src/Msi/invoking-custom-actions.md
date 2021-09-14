---
description: Las acciones personalizadas se invocan de la misma manera que las acciones estándar, ya sea mediante invocación explícita o durante la ejecución de una tabla de secuencia.
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: Invocación de acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f1e9a575d32cbb8fe22323d4a741eb7936ef9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072000"
---
# <a name="invoking-custom-actions"></a>Invocación de acciones personalizadas

Las acciones personalizadas se invocan de la misma manera que las acciones estándar, ya sea mediante invocación explícita o durante la ejecución de una tabla de secuencia. Hay dos métodos para llamar a acciones:

-   La acción especificada se llama directamente con la [**función MsiDoAction.**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)
-   Una acción de nivel superior llama a la tabla de secuencia que contiene la acción personalizada. Para obtener más información sobre cómo programar una acción personalizada en una tabla de secuencias, vea [Secuenciación de acciones personalizadas.](sequencing-custom-actions.md)

Cuando el instalador obtiene un nombre de acción de la función [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o de una tabla de secuencia, primero busca una acción estándar de ese nombre. Si no encuentra la acción estándar, el instalador consulta la tabla [CustomAction](customaction-table.md) para comprobar si la acción especificada es una acción personalizada. Si la acción especificada no es una acción personalizada, el instalador consulta un cuadro de diálogo en la tabla dialog. [](dialog-table.md)

 

 



