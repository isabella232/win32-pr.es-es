---
description: La acción RegisterTypeLibraries registra las bibliotecas de tipos con el sistema. Esta acción se aplica a cada archivo al que se hace referencia en la tabla TypeLib que está programada para instalarse.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: Acción RegisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469cc18fc2842a3258804fc012c48a49085f1598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677759"
---
# <a name="registertypelibraries-action"></a>Acción RegisterTypeLibraries

La acción RegisterTypeLibraries registra las bibliotecas de tipos con el sistema. Esta acción se aplica a cada archivo al que se hace referencia en la [tabla typelib](typelib-table.md) que está programada para instalarse.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RegisterTypeLibraries debe aparecer después de la acción [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                   |
|-------|----------------------------------------------|
| \[1\] | [GUID](guid.md) de la biblioteca de tipos registrados. |



 

## <a name="remarks"></a>Observaciones

La acción RegisterTypeLibraries requiere que el idioma de la biblioteca de tipos se cree correctamente en el campo Language de la tabla TypeLib. La creación incorrecta del campo de idioma puede hacer que el instalador no pueda registrar una biblioteca de tipos válida de otro modo.

 

 



