---
description: Una especificación del ejemplo es que la información de la cuenta de usuario se lee de una tabla personalizada en la base de datos de instalación y no se codifica de forma rígida en la acción personalizada.
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: Agregar una tabla CustomUserAccounts personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58366c725ecc135b9583c926a16383a5ad5a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652629"
---
# <a name="adding-a-custom-customuseraccounts-table"></a>Agregar una tabla CustomUserAccounts personalizada

Una especificación del ejemplo es que la información de la cuenta de usuario se lee de una tabla personalizada en la base de datos de instalación y no se codifica de forma rígida en la acción personalizada.

Agregue una tabla personalizada a la base de datos de instalación de ejemplo denominada CustomUserAccounts para almacenar la información de la cuenta de usuario. Vea [ejemplos de consultas de base de datos mediante SQL y script](examples-of-database-queries-using-sql-and-script.md) para obtener un ejemplo de cómo agregar una tabla personalizada. Use el siguiente esquema para la tabla CustomUserAccounts. Vea [formato de definición de columna](column-definition-format.md) para obtener una explicación de los tipos de columna.



| Columna     | Tipo | Clave | Nullable | Descripción                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UserName   | S72  | Y   | N        | Nombre de la cuenta de usuario que se va a crear.                                                                                                                                                                                                                                                                        |
| Contraseña   | S72  |     | N        | Nombre de la propiedad que contiene la contraseña de la cuenta. Se trata de una [propiedad pública](public-properties.md) establecida en la línea de comandos o a través de un [control de edición](edit-control.md) en la interfaz de usuario. Este control de edición debe tener el [atributo de control de contraseña](password-control-attribute.md). |
| Atributos | i4   |     | Y        | Atributos de la cuenta. Se definen como valores **DWORD** para el \_ miembro usri1 flags de la estructura de \_ información de usuario \_ 1.                                                                                                                                                                              |



 

Una vez agregada la tabla CustomUserAccounts a la base de datos, puede editar esta tabla mediante orca, un editor de tablas proporcionado con el SDK de Windows Installer u otro editor. Escriba el Registro siguiente en la tabla CustomUserAccounts para crear una cuenta de usuario protegida con contraseña para un usuario llamado TestUser. Tenga en cuenta que 512 es el valor numérico de la cuenta de fi \_ normal \_ .

Tabla CustomUserAccounts



| UserName | Contraseña         | Atributos |
|----------|------------------|------------|
| TestUser | TESTUSERPASSWORD | 512        |



 

Agregue los siguientes registros a la \_ tabla de validación para la tabla personalizada.

[\_Tabla de validación](-validation-table.md)



| Tabla              | Columna     | Nullable | MinValue | MaxValue   | KeyTable | KeyColumn | Category                     | Set | Descripción |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| CustomUserAccounts | UserName   | N        |          |            |          |           | [Texto](text.md)             |     |             |
| CustomUserAccounts | Contraseña   | N        |          |            |          |           | [Identificador](identifier.md) |     |             |
| CustomUserAccounts | Atributos | Y        | 0        | 2147483647 |          |           | null                         |     |             |



 

Continúe con [la creación de las tablas de error y de ActionText](authoring-the-actiontext-and-error-tables.md).

 

 



