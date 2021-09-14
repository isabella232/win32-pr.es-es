---
description: La acción SetODBCFolders comprueba si hay controladores ODBC existentes en el sistema y establece el directorio de destino de cada nuevo controlador en la ubicación de un controlador existente.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: Acción SetODBCFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b229d127e976ddb37096c5f3a21605ba8d05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272412"
---
# <a name="setodbcfolders-action"></a>Acción SetODBCFolders

La acción SetODBCFolders comprueba si hay controladores ODBC existentes en el sistema y establece el directorio de destino de cada nuevo controlador en la ubicación de un controlador existente.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción SetODBCFolders debe ir después de la acción [CostFinalize](costfinalize-action.md) y antes de [la acción InstallValidate](installvalidate-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                                                          |
|-------|-------------------------------------------------------------------------------------|
| \[1\] | Descripción del controlador. Clave del controlador ODBC.                                            |
| \[2\] | Ubicación de la carpeta original del nuevo controlador.                                         |
| \[3\] | Nueva ubicación de carpeta para el nuevo controlador. Esta es la ubicación de un controlador existente. |



 

## <a name="remarks"></a>Observaciones

Esta acción coloca un nuevo controlador en el mismo directorio que el controlador existente que se va a reemplazar. La acción SetODBCFolders usa la [tabla Directory](directory-table.md) para establecer las ubicaciones de los controladores existentes que se van a reemplazar.

 

 



