---
description: La acción ProcessComponents registra y anula el registro de los componentes, sus rutas de acceso de clave y los clientes de componentes.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: Acción ProcessComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aef1f71e9a50b714a12848fc9f923d1866c2e40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473945"
---
# <a name="processcomponents-action"></a>Acción ProcessComponents

La acción ProcessComponents registra y anula el registro de los componentes, sus rutas de acceso de clave y los clientes de componentes. La acción ProcessComponents consulta la columna KeyPath de la [tabla Component](component-table.md) para determinar las rutas de acceso de clave. [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) usa este registro para devolver la ruta de acceso de un componente para un cliente de producto.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción ProcessComponents debe ir después [de la acción InstallInitialize.](installinitialize-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData

Para cada componente que se va a registrar.



| Campo | Descripción de los datos de acción      |
|-------|---------------------------------|
| \[1\] | ProductId                       |
| \[2\] | Componentid                     |
| \[3\] | Ruta de acceso de clave para el componente. |



 

Para cada componente que se anula el registro.



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | ProductId                  |
| \[2\] | Componentid                |



 

 

 



