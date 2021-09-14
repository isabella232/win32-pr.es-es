---
description: Las especificaciones de ejemplo incluyen el envío de mensajes ActionData cuando una acción personalizada crea o quita una cuenta de usuario, y la notificación de un error si no se puede crear una cuenta.
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: Creación de las tablas ActionText y Error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20646a90ca76c159a88bdd8a6d026ff10845da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159014"
---
# <a name="authoring-the-actiontext-and-error-tables"></a>Creación de las tablas ActionText y Error

Las especificaciones de ejemplo incluyen el envío de mensajes ActionData cuando una acción personalizada crea o quita una cuenta de usuario, y la notificación de un error si no se puede crear una cuenta.

Escriba las siguientes entradas en la tabla ActionText para proporcionar la información utilizada por los mensajes ActionText.

[ActionText (tabla)](actiontext-table.md)



| Acción            | Descripción                                                       | Plantilla                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| ProcessAccounts   | Generación de acciones para crear cuentas de usuario en el equipo local. | Cuenta: \[ 1 \] , Atributos: \[ 2\] |
| CreateAccount     | Crear una cuenta de usuario en el equipo local.                      | Cuenta: \[ 1\]                    |
| RemoveAccount     | Quitar la cuenta de usuario del equipo local.                    | Cuenta: \[ 1\]                    |
| RollbackAccount   | Revertir la creación de cuentas de usuario en el equipo local. | Cuenta: \[ 1\]                    |
| UninstallAccounts | Generación de acciones para quitar cuentas de usuario en el equipo local. | Cuenta: \[ 1\]                    |



 

Escriba las siguientes entradas en la tabla Error para proporcionar la información utilizada por los informes de errores.

[Tabla de errores](error-table.md)



| Error | Message                                                                        |
|-------|--------------------------------------------------------------------------------|
| 25001 | No se puede crear la cuenta de usuario \[ "2" \] en el equipo local. Código de error: \[ 3 \] . |
| 25002 | La cuenta de usuario \[ "2" \] ya existe en la máquina local.                      |
| 25003 | No se puede quitar la cuenta de usuario \[ "2" \] en la máquina local. Código de error: \[ 3 \] . |
| 25004 | La cuenta de \[ usuario "2" \] no existe en la máquina local.                      |



 

Continúe con [Creación de la tabla InstallExecuteSequence](authoring-the-installexecutesequence-table.md).

 

 



