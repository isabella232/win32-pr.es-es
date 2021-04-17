---
description: Las acciones personalizadas ProcessAccounts y UninstallAccounts generan las acciones personalizadas diferidas que crean, quitan o revierten las cuentas de usuario.
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: Crear la tabla InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa09895d5e5d2543b5594f4795734d26163a4f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667027"
---
# <a name="authoring-the-installexecutesequence-table"></a>Crear la tabla InstallExecuteSequence

Las acciones personalizadas ProcessAccounts y UninstallAccounts generan las acciones personalizadas diferidas que crean, quitan o revierten las cuentas de usuario. Las acciones personalizadas ProcessAccounts y UninstallAccounts deben especificarse en la [tabla InstallExecuteSequence](installexecutesequence-table.md) que se va a ejecutar. Agregue las siguientes entradas a la [tabla InstallExecuteSequence](installexecutesequence-table.md). Dado que estas acciones personalizadas deben formar parte de la generación del script, ambas acciones personalizadas se deben secuenciar después de la [acción InstallInitialize](installinitialize-action.md).

La condición de ProcessAccounts garantiza lo siguiente. Consulte [Sintaxis de la instrucción condicional](conditional-statement-syntax.md).

-   ProcessAccounts solo se ejecuta si el componente TestAccount se instala localmente en el equipo.
-   La cuenta de prueba de componentes no está instalada actualmente o está instalada para ejecutarse desde el origen.

La condición de UninstallAccount garantiza lo siguiente:

-   UninstallAccounts solo se ejecuta si el componente TestAccount está instalado localmente en el equipo.
-   La cuenta de prueba de componentes se está quitando o se está instalando para ejecutarse desde el origen.

[Tabla InstallExecuteSequence](installexecutesequence-table.md)



| Acción            | Condición                                                           | Secuencia |
|-------------------|---------------------------------------------------------------------|----------|
| ProcessAccounts   | VersionNT y (? TestAccount = 2 o? TestAccount = 4) y $TestAccount = 3 | 1550     |
| UninstallAccounts | VersionNT y? TestAccount = 3 y ($TestAccount = 4 o $TestAccount = 2) | 1560     |



 

Continúe con [la creación de la interfaz de usuario para la entrada de contraseña](authoring-the-user-interface-for-password-input.md).

 

 



