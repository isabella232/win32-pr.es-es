---
description: La acción ProcessComponents registra y anula el registro de componentes, sus rutas de acceso clave y los clientes de componentes.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: Acción ProcessComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aef1f71e9a50b714a12848fc9f923d1866c2e40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652943"
---
# <a name="processcomponents-action"></a>Acción ProcessComponents

La acción ProcessComponents registra y anula el registro de componentes, sus rutas de acceso clave y los clientes de componentes. La acción ProcessComponents consulta la columna de la ruta de la [tabla de componentes](component-table.md) para determinar keypaths. [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) usa este registro para devolver la ruta de acceso de un componente para un cliente del producto.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción ProcessComponents debe aparecer después de la acción [InstallInitialize](installinitialize-action.md) .

## <a name="actiondata-messages"></a>Mensajes ActionData

Para cada componente que se va a registrar.



| Campo | Descripción de los datos de acción      |
|-------|---------------------------------|
| \[1\] | ProductId                       |
| \[2\] | ComponentId                     |
| \[3\] | Ruta de acceso de la clave del componente. |



 

Para cada componente del que se va a anular el registro.



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | ProductId                  |
| \[2\] | ComponentId                |



 

 

 



