---
description: La acción RegisterTypeLibraries registra bibliotecas de tipos con el sistema. Esta acción se aplica a cada archivo al que se hace referencia en la tabla TypeLib que está programada para su instalación.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: Acción RegisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469cc18fc2842a3258804fc012c48a49085f1598
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069685"
---
# <a name="registertypelibraries-action"></a>Acción RegisterTypeLibraries

La acción RegisterTypeLibraries registra bibliotecas de tipos con el sistema. Esta acción se aplica a cada archivo al que se hace referencia en la [tabla TypeLib](typelib-table.md) que está programada para su instalación.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RegisterTypeLibraries debe ir después de [la acción InstallFiles.](installfiles-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                   |
|-------|----------------------------------------------|
| \[1\] | [GUID](guid.md) de la biblioteca de tipos registrados. |



 

## <a name="remarks"></a>Observaciones

La acción RegisterTypeLibraries requiere que el lenguaje de biblioteca de tipos se cree correctamente en el campo Idioma de la tabla TypeLib. La creación incorrecta del campo Idioma puede hacer que el instalador no pueda registrar una biblioteca de tipos válida de otro modo.

 

 



