---
description: Las acciones personalizadas ProcessAccounts y UninstallAccounts generan las acciones personalizadas diferidas que crean, quitan o revierte cuentas de usuario.
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: Creación de la tabla InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa09895d5e5d2543b5594f4795734d26163a4f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159011"
---
# <a name="authoring-the-installexecutesequence-table"></a>Creación de la tabla InstallExecuteSequence

Las acciones personalizadas ProcessAccounts y UninstallAccounts generan las acciones personalizadas diferidas que crean, quitan o revierte cuentas de usuario. Las acciones personalizadas ProcessAccounts y UninstallAccounts deben especificarse en la [tabla InstallExecuteSequence](installexecutesequence-table.md) que se va a ejecutar. Agregue las siguientes entradas a la [tabla InstallExecuteSequence](installexecutesequence-table.md). Dado que estas acciones personalizadas deben formar parte de la generación de scripts, ambas acciones personalizadas deben secuenciarse después de [la acción InstallInitialize](installinitialize-action.md).

La condición en ProcessAccounts garantiza lo siguiente. Vea [Sintaxis de instrucciones condicionales.](conditional-statement-syntax.md)

-   ProcessAccounts solo se ejecuta si el componente TestAccount se instala localmente en el equipo.
-   La cuenta de prueba del componente no está instalada actualmente o está instalada para ejecutarse desde el origen.

La condición en UninstallAccount garantiza lo siguiente:

-   UninstallAccounts solo se ejecuta si el componente TestAccount está instalado localmente en el equipo.
-   El componente Cuenta de prueba se está quitando o se está instalando para ejecutarse desde el origen.

[Tabla InstallExecuteSequence](installexecutesequence-table.md)



| Acción            | Condición                                                           | Secuencia |
|-------------------|---------------------------------------------------------------------|----------|
| ProcessAccounts   | VersionNT AND (? TestAccount=2 OR ? TestAccount=4) AND $TestAccount=3 | 1550     |
| UninstallAccounts | VersionNT AND ? TestAccount=3 AND ($TestAccount=4 OR $TestAccount=2) | 1560     |



 

Continúe con [Creación de la interfaz de usuario para la entrada de contraseña.](authoring-the-user-interface-for-password-input.md)

 

 



