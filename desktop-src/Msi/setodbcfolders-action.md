---
description: La acción SetODBCFolders comprueba los controladores ODBC existentes en el sistema y establece el directorio de destino de cada nuevo controlador en la ubicación de un controlador existente.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: Acción SetODBCFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceaefc2e9722b82ab0753c46b9e1e85a0ab3628a83b9f3abe66cf183c543fbe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628645"
---
# <a name="setodbcfolders-action"></a>Acción SetODBCFolders

La acción SetODBCFolders comprueba los controladores ODBC existentes en el sistema y establece el directorio de destino de cada nuevo controlador en la ubicación de un controlador existente.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción SetODBCFolders debe ir después de la acción [CostFinalize](costfinalize-action.md) y antes de [la acción InstallValidate](installvalidate-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                                                          |
|-------|-------------------------------------------------------------------------------------|
| \[1\] | Descripción del controlador. Clave del controlador ODBC.                                            |
| \[2\] | Ubicación de la carpeta original del nuevo controlador.                                         |
| \[3\] | Nueva ubicación de carpeta para el nuevo controlador. Esta es la ubicación de un controlador existente. |



 

## <a name="remarks"></a>Comentarios

Esta acción coloca un nuevo controlador en el mismo directorio que el controlador existente que se va a reemplazar. La acción SetODBCFolders usa la [tabla Directory](directory-table.md) para establecer las ubicaciones de los controladores existentes que se van a reemplazar.

 

 



