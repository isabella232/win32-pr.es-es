---
description: La acción ProcessComponents registra y anula el registro de los componentes, sus rutas de acceso de clave y los clientes de componentes.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: Acción ProcessComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e866c6003052922dfc0e1fca5bd4ff8ea63d207eeb03c5ada22cf5f2d3e7b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259285"
---
# <a name="processcomponents-action"></a>Acción ProcessComponents

La acción ProcessComponents registra y anula el registro de los componentes, sus rutas de acceso de clave y los clientes de componentes. La acción ProcessComponents consulta la columna KeyPath de la [tabla Component](component-table.md) para determinar keypaths. [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) usa este registro para devolver la ruta de acceso de un componente para un cliente de producto.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción ProcessComponents debe ir después de [la acción InstallInitialize.](installinitialize-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData

Para cada componente que se va a registrar.



| Campo | Descripción de los datos de acción      |
|-------|---------------------------------|
| \[1\] | ProductId                       |
| \[2\] | Componentid                     |
| \[3\] | Ruta de acceso de clave para el componente. |



 

Para cada componente que se va a anular el registro.



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | ProductId                  |
| \[2\] | Componentid                |



 

 

 



