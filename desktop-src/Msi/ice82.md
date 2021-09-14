---
description: ICE82 valida que la acción RegisterProduct, la acción RegisterUser, la acción PublishProduct y la acción PublishFeatures están presentes en la tabla InstallExecuteSequence. El paquete se valida si todas las acciones están presentes.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa6ba2e0bd07af06bf90c604c333966b5581ba3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074529"
---
# <a name="ice82"></a>ICE82

ICE82 valida que las acciones [RegisterProduct,](registerproduct-action.md) [RegisterUser](registeruser-action.md), [PublishProduct y](publishproduct-action.md) [PublishFeatures están](publishfeatures-action.md) presentes en la tabla [InstallExecuteSequence](installexecutesequence-table.md). El paquete se valida si todas las acciones están presentes.

ICE82 envía una advertencia si hay dos acciones con el mismo número de secuencia enumerado en las tablas InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence o AdvtExecuteSequence .

## <a name="result"></a>Resultado

ICE82 publica las siguientes advertencias.



| Advertencia de ICE82                                                                                                                                                                                                                 | Descripción                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La tabla InstallExecuteSequence no contiene el conjunto de acciones que se mencionan a continuación: Acciones que faltan:<br/> Publicar características<br/> Publicar producto<br/> Registro del producto<br/> Registrar usuario<br/> | La acción personalizada ICE82 envía una advertencia si las cuatro acciones no están presentes.                                                                                                                                         |
| Esta acción \[ 1 \] tiene el número de secuencia duplicado \[ 2 en la tabla \] \[ \] 3.                                                                                                                                                     | ICE82 envía una advertencia si hay dos acciones con el mismo número de secuencia enumerado en las tablas InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence o AdvtExecuteSequence. |



 

ICE82 publica los siguientes errores.



| Error ice82                                                                                                                                                                                                                                        | Descripción                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| InstallExecuteSequence debe contener todas las acciones mencionadas a continuación o ninguna de ellas Acciones presentes<br/> <List of actions present> <br/> Acciones que faltan:<br/> <List of actions missing> <br/> | ICE82 publica un error si algunas de las cuatro acciones están presentes y otras están ausentes. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




