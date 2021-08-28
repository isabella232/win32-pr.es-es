---
description: ICE82 valida que la acción RegisterProduct, la acción RegisterUser, la acción PublishProduct y la acción PublishFeatures están presentes en la tabla InstallExecuteSequence. El paquete se valida si todas las acciones están presentes.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf620bd58ca59315796941c6e8d9d3e4c12cdca9064d2be79058c89201a91bad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105235"
---
# <a name="ice82"></a>ICE82

ICE82 valida que la acción [RegisterProduct,](registerproduct-action.md)la acción [RegisterUser,](registeruser-action.md)la acción [PublishProduct](publishproduct-action.md)y la acción [PublishFeatures](publishfeatures-action.md) están presentes en la tabla [InstallExecuteSequence](installexecutesequence-table.md). El paquete se valida si todas las acciones están presentes.

ICE82 envía una advertencia si hay dos acciones con el mismo número de secuencia enumerado en las tablas InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence o AdvtExecuteSequence .

## <a name="result"></a>Resultado

ICE82 publica las advertencias siguientes.



| Advertencia de ICE82                                                                                                                                                                                                                 | Descripción                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La tabla InstallExecuteSequence no contiene el conjunto de acciones que se mencionan a continuación: Acciones que faltan:<br/> Publicar características<br/> Publicar producto<br/> Registrar producto<br/> Registrar usuario<br/> | La acción personalizada ICE82 envía una advertencia si las cuatro acciones no están presentes.                                                                                                                                         |
| Esta acción \[ 1 \] tiene el número de secuencia duplicado \[ 2 en la tabla \] \[ 3 \] .                                                                                                                                                     | ICE82 envía una advertencia si hay dos acciones con el mismo número de secuencia enumerado en las tablas InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence o AdvtExecuteSequence. |



 

ICE82 publica los siguientes errores.



| Error ice82                                                                                                                                                                                                                                        | Descripción                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| InstallExecuteSequence debe contener todas las acciones mencionadas a continuación o ninguna de ellas Acciones presentes<br/> <List of actions present> <br/> Acciones que faltan:<br/> <List of actions missing> <br/> | ICE82 publica un error si algunas de las cuatro acciones están presentes y otras están ausentes. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




