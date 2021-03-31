---
description: ICE82 valida que la acción RegisterProduct, la acción RegisterUser, la acción PublishProduct y la acción PublishFeatures están presentes en la tabla InstallExecuteSequence. El paquete se valida si todas las acciones están presentes.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa6ba2e0bd07af06bf90c604c333966b5581ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816243"
---
# <a name="ice82"></a>ICE82

ICE82 valida que la acción [RegisterProduct](registerproduct-action.md), la acción [RegisterUser](registeruser-action.md), la [acción PublishProduct](publishproduct-action.md)y la [acción PublishFeatures](publishfeatures-action.md) están presentes en la [tabla InstallExecuteSequence](installexecutesequence-table.md). El paquete se valida si todas las acciones están presentes.

ICE82 publica una advertencia si hay dos acciones con el mismo número de secuencia enumeradas en las tablas InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence o AdvtExecuteSequence.

## <a name="result"></a>Resultado

ICE82 expone las siguientes advertencias.



| ADVERTENCIA de ICE82                                                                                                                                                                                                                 | Descripción                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La tabla InstallExecuteSequence no contiene el conjunto de acciones que se mencionan a continuación: faltan acciones:<br/> Publicar características<br/> Publicar producto<br/> Registrar producto<br/> Registrar usuario<br/> | La acción personalizada ICE82 publica una advertencia si las cuatro acciones están ausentes.                                                                                                                                         |
| Esta acción \[ 1 \] tiene el número de secuencia 2 duplicado \[ \] en la tabla \[ 3 \] .                                                                                                                                                     | ICE82 publica una advertencia si hay dos acciones con el mismo número de secuencia enumeradas en las tablas InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence o AdvtExecuteSequence. |



 

ICE82 expone los siguientes errores.



| Error ICE82                                                                                                                                                                                                                                        | Descripción                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| InstallExecuteSequence debe contener todas las acciones que se mencionan a continuación o ninguna de ellas.<br/> <List of actions present> <br/> Faltan acciones:<br/> <List of actions missing> <br/> | ICE82 publica un error si algunas de las cuatro acciones están presentes y otras están ausentes. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




