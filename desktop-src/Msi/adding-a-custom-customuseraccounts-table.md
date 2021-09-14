---
description: Una especificación del ejemplo es que la información de la cuenta de usuario se lee de una tabla personalizada en la base de datos de instalación y no se codifica de forma automática en la acción personalizada.
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: Agregar una tabla CustomUserAccounts personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58366c725ecc135b9583c926a16383a5ad5a01
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159219"
---
# <a name="adding-a-custom-customuseraccounts-table"></a>Agregar una tabla CustomUserAccounts personalizada

Una especificación del ejemplo es que la información de la cuenta de usuario se lee de una tabla personalizada en la base de datos de instalación y no se codifica de forma automática en la acción personalizada.

Agregue una tabla personalizada a la base de datos de instalación de ejemplo denominada CustomUserAccounts para contener la información de la cuenta de usuario. Vea [Ejemplos de consultas de base](examples-of-database-queries-using-sql-and-script.md) de datos SQL y Script para obtener un ejemplo de cómo agregar una tabla personalizada. Use el esquema siguiente para la tabla CustomUserAccounts. Vea [Formato de definición de columna](column-definition-format.md) para obtener una explicación de los tipos de columna.



| Columna     | Tipo | Clave | Nullable | Descripción                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UserName   | s72  | Y   | N        | Nombre de la cuenta de usuario que se va a crear.                                                                                                                                                                                                                                                                        |
| Contraseña   | s72  |     | N        | Nombre de la propiedad que contiene la contraseña de la cuenta. Se trata de [una propiedad pública establecida](public-properties.md) en la línea de comandos o a través de un control de [edición](edit-control.md) en la interfaz de usuario. Este control de edición debe tener el [atributo de control de contraseña](password-control-attribute.md). |
| Atributos | i4   |     | Y        | Atributos de la cuenta. Se definen como valores **DWORD** para el miembro usri1 \_ flags de la estructura USER \_ INFO \_ 1.                                                                                                                                                                              |



 

Una vez agregada la tabla CustomUserAccounts a la base de datos, puede editar esta tabla mediante Orca, un editor de tablas proporcionado con el SDK del instalador de Windows u otro editor. Escriba el registro siguiente en la tabla CustomUserAccounts para crear una cuenta de usuario protegida con contraseña para un usuario llamado TestUser. Tenga en cuenta que 512 es el valor numérico de UF \_ NORMAL \_ ACCOUNT.

CustomUserAccounts (tabla)



| UserName | Contraseña         | Atributos |
|----------|------------------|------------|
| TestUser | TESTUSERPASSWORD | 512        |



 

Agregue los siguientes registros a la \_ tabla Validation de la tabla personalizada.

[\_Tabla de validación](-validation-table.md)



| Tabla              | Columna     | Nullable | MinValue | MaxValue   | KeyTable | KeyColumn | Category                     | Set | Descripción |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| CustomUserAccounts | UserName   | N        |          |            |          |           | [Texto](text.md)             |     |             |
| CustomUserAccounts | Contraseña   | N        |          |            |          |           | [Identificador](identifier.md) |     |             |
| CustomUserAccounts | Atributos | Y        | 0        | 2147483647 |          |           | null                         |     |             |



 

Continúe con [la creación de las tablas ActionText y Error](authoring-the-actiontext-and-error-tables.md).

 

 



