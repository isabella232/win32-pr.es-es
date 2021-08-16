---
description: La acción RegisterTypeLibraries registra bibliotecas de tipos con el sistema. Esta acción se aplica a cada archivo al que se hace referencia en la tabla TypeLib que está programada para su instalación.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: Acción RegisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac42c831c8413f297d3df2302523a2372b11d1efcffe82ce0d3a82da722832cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626768"
---
# <a name="registertypelibraries-action"></a>Acción RegisterTypeLibraries

La acción RegisterTypeLibraries registra bibliotecas de tipos con el sistema. Esta acción se aplica a cada archivo al que se hace referencia en la [tabla TypeLib](typelib-table.md) que está programada para su instalación.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RegisterTypeLibraries debe ir después de [la acción InstallFiles.](installfiles-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                   |
|-------|----------------------------------------------|
| \[1\] | [GUID](guid.md) de la biblioteca de tipos registrados. |



 

## <a name="remarks"></a>Comentarios

La acción RegisterTypeLibraries requiere que el lenguaje de biblioteca de tipos se cree correctamente en el campo Idioma de la tabla TypeLib. La creación incorrecta del campo Idioma puede hacer que el instalador no pueda registrar una biblioteca de tipos válida de otro modo.

 

 



