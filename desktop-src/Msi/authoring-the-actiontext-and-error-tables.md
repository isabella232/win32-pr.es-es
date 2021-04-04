---
description: Las especificaciones de ejemplo incluyen el envío de mensajes de ActionData cuando una acción personalizada crea o quita una cuenta de usuario y notifica un error si no se puede crear una cuenta.
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: Creación de las tablas de error y de ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20646a90ca76c159a88bdd8a6d026ff10845da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909070"
---
# <a name="authoring-the-actiontext-and-error-tables"></a>Creación de las tablas de error y de ActionText

Las especificaciones de ejemplo incluyen el envío de mensajes de ActionData cuando una acción personalizada crea o quita una cuenta de usuario y notifica un error si no se puede crear una cuenta.

Escriba las siguientes entradas en la tabla de ActionText para proporcionar información usada por los mensajes de ActionText.

[Tabla de ActionText](actiontext-table.md)



| Acción            | Descripción                                                       | Plantilla                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| ProcessAccounts   | Generar acciones para crear cuentas de usuario en el equipo local. | Cuenta: \[ 1 \] , atributos: \[ 2\] |
| CreateAccount     | Creando una cuenta de usuario en el equipo local.                      | Cuenta: \[ 1\]                    |
| RemoveAccount     | Quitando la cuenta de usuario del equipo local.                    | Cuenta: \[ 1\]                    |
| RollbackAccount   | Revertir la creación de cuentas de usuario en el equipo local. | Cuenta: \[ 1\]                    |
| UninstallAccounts | Generar acciones para quitar cuentas de usuario en el equipo local. | Cuenta: \[ 1\]                    |



 

Escriba las siguientes entradas en la tabla de errores para proporcionar la información que utiliza el informe de errores.

[Tabla de errores](error-table.md)



| Error | Message                                                                        |
|-------|--------------------------------------------------------------------------------|
| 25001 | No se puede crear la cuenta \[ de usuario ' 2 \] ' en el equipo local. Código de error: \[ 3 \] . |
| 25002 | La cuenta de usuario ' \[ 2 \] ' ya existe en el equipo local.                      |
| 25003 | No se puede quitar la cuenta \[ de usuario ' 2 \] ' en el equipo local. Código de error: \[ 3 \] . |
| 25004 | La cuenta de usuario ' \[ 2 \] ' no existe en el equipo local.                      |



 

Continúe con [la creación de la tabla InstallExecuteSequence](authoring-the-installexecutesequence-table.md).

 

 



