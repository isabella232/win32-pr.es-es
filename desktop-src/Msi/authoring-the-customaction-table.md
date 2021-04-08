---
description: Escriba los registros de las cinco acciones personalizadas de ejemplo creadas en la sección anterior en la tabla CustomAction. Para obtener más información sobre cómo rellenar la tabla CustomAction para este tipo de acción personalizada, vea acción personalizada tipo 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Creación de la tabla CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fb7d8cf99a30200e6a5525e3516e2b888c1129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001723"
---
# <a name="authoring-the-customaction-table"></a>Creación de la tabla CustomAction

Escriba los registros de las cinco acciones personalizadas de ejemplo creadas en la sección anterior en la [tabla CustomAction](customaction-table.md). Para obtener más información sobre cómo rellenar la tabla CustomAction para este tipo de acción personalizada, vea [acción personalizada tipo 1](custom-action-type-1.md).

[Tabla CustomAction](customaction-table.md)



| Acción            | Tipo  | Source      | Destino                |
|-------------------|-------|-------------|-----------------------|
| ProcessAccounts   | 1     | Process.dll | ProcessUserAccounts   |
| UninstallAccounts | 1     | Process.dll | UninstallUserAccounts |
| CreateAccount     | 11265 | Create.dll  | CreateUserAccount     |
| RemoveAccount     | 11265 | Remove.dll  | RemoveUserAccount     |
| RollbackAccount   | 9473  | Remove.dll  | RemoveUserAccount     |



 

El código fuente de C++ de las bibliotecas de vínculos dinámicos se proporciona en el SDK de Windows Installer. Use Process. cpp para crear el archivo Process.dll. Utilice Create. cpp para crear el archivo Create.dll. Utilice Remove. cpp para crear Remove.dll. Agregue estos archivos de biblioteca de vínculos dinámicos a la tabla binaria.

[Tabla binaria](binary-table.md)



| Nombre        | Datos            |
|-------------|-----------------|
| Process.dll | {*datos binarios*} |
| Create.dll  | {*datos binarios*} |
| Remove.dll  | {*datos binarios*} |



 

Continúe [agregando una tabla CustomUserAccounts personalizada](adding-a-custom-customuseraccounts-table.md).

 

 



