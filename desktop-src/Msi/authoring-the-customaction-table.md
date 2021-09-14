---
description: Escriba los registros de las cinco acciones personalizadas de ejemplo creadas en la sección anterior en la tabla CustomAction. Para obtener más información sobre cómo rellenar la tabla CustomAction para este tipo de acción personalizada, vea Tipo de acción personalizada 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Creación de la tabla CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fb7d8cf99a30200e6a5525e3516e2b888c1129
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159012"
---
# <a name="authoring-the-customaction-table"></a>Creación de la tabla CustomAction

Escriba los registros de las cinco acciones personalizadas de ejemplo creadas en la sección anterior en [la tabla CustomAction](customaction-table.md). Para obtener más información sobre cómo rellenar la tabla CustomAction para este tipo de acción personalizada, vea [Custom Action Type 1](custom-action-type-1.md).

[CustomAction (tabla)](customaction-table.md)



| Acción            | Tipo  | Source      | Destino                |
|-------------------|-------|-------------|-----------------------|
| ProcessAccounts   | 1     | Process.dll | ProcessUserAccounts   |
| UninstallAccounts | 1     | Process.dll | UninstallUserAccounts |
| CreateAccount     | 11265 | Create.dll  | CreateUserAccount     |
| RemoveAccount     | 11265 | Remove.dll  | RemoveUserAccount     |
| RollbackAccount   | 9473  | Remove.dll  | RemoveUserAccount     |



 

El código fuente de C++ para las bibliotecas de vínculos dinámicos se proporciona en el SDK Windows Installer. Use Process.cpp para crear el archivo Process.dll. Use Create.cpp para crear el archivo Create.dll. Use Remove.cpp para crear Remove.dll. Agregue estos archivos de biblioteca de vínculos dinámicos a la tabla Binary.

[Tabla binaria](binary-table.md)



| Nombre        | Datos            |
|-------------|-----------------|
| Process.dll | {*datos binarios*} |
| Create.dll  | {*datos binarios*} |
| Remove.dll  | {*datos binarios*} |



 

Continúe con [Agregar una tabla CustomUserAccounts personalizada.](adding-a-custom-customuseraccounts-table.md)

 

 



