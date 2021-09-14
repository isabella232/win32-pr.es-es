---
description: 'En la tabla siguiente se enumeran las cinco acciones personalizadas que se usan para cumplir las especificaciones de ejemplo: ProcessAccounts, UninstallAccounts, CreateAccounts, RemoveAccounts y RollbackAccounts.'
ms.assetid: 389ec652-243e-4392-aec9-3a7eb90e6c68
title: Creación de acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09525490304762b98635bcbbe6c238ce3fe413f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159013"
---
# <a name="authoring-the-custom-actions"></a>Creación de acciones personalizadas

En la tabla siguiente se enumeran las cinco acciones personalizadas que se usan para cumplir las especificaciones de ejemplo: ProcessAccounts, UninstallAccounts, CreateAccounts, RemoveAccounts y RollbackAccounts. Todas estas acciones personalizadas están en [bibliotecas de vínculos dinámicos almacenadas](dynamic-link-libraries.md) en [la tabla binaria](binary-table.md). El código fuente de C++ para las bibliotecas de vínculos dinámicos que contienen las acciones personalizadas de ejemplo se proporcionan en el SDK Windows Installer. ProcessAccounts y UninstallAccounts se encuentran en el archivo Process.cpp. CreateAccount está en el archivo Create.cpp. RemoveAccount y RollbackAccount se encuentran en el archivo Remove.cpp. Estos archivos de origen se pueden usar para crear los archivos Process.dll, Create.dll y Remove.dll.

Dado que la creación o eliminación de [](deferred-execution-custom-actions.md) una cuenta de usuario requiere privilegios elevados, las acciones personalizadas de ejecución diferida que se ejecutan en el contexto del sistema deben usarse para crear, quitar o revertir cuentas de usuario. Las acciones personalizadas de ejecución inmediata, ProcessAccounts y UninstallAccounts, generan las acciones personalizadas diferidas que crean, quitan o revierte cuentas de usuario: CreateAccount, RemoveAccount y RollbackAccount.

Dado que las acciones personalizadas diferidas no pueden leer información en tablas de base de datos, ProcessAccounts y UninstallUserAccouts deben establecer una propiedad CustomActionData para pasar la información de la tabla UserAccounts a las acciones personalizadas diferidas como se describe en Obtención de información de contexto para acciones personalizadas de ejecución [aplazada.](obtaining-context-information-for-deferred-execution-custom-actions.md) Cuando el instalador ejecuta el script de ejecución, las acciones personalizadas diferidas controlan las cuentas de usuario según la información de la propiedad CustomActionData.

Dado que todas las acciones personalizadas están en bibliotecas de vínculos dinámicos almacenadas en la tabla Binary, todas incluyen las constantes msidbCustomActionTypeDll y msidbCustomActionTypeBinaryData en su tipo numérico base. ProcessAccounts y UninstallAccounts son ejemplos de acción [personalizada pura de tipo 1.](custom-action-type-1.md) Para obtener información sobre otros tipos de acciones personalizadas, vea [La lista de resumen de todos los tipos de acción personalizados](summary-list-of-all-custom-action-types.md).

CreateAccount y RemoveAccount son acciones personalizadas de ejecución [aplazada](deferred-execution-custom-actions.md) que no permiten a los servicios suplantar a usuarios concretos. Estas acciones personalizadas incluyen las constantes msidbCustomActionTypeInScript y msidbCustomActionTypeNoImpersonate para especificar estas opciones de ejecución de acciones personalizadas en [script.](custom-action-in-script-execution-options.md)

RollbackAccount es una [acción personalizada de reversión](rollback-custom-actions.md) que solo quita las cuentas de usuario durante una [instalación de reversión.](rollback-installation.md) RollbackAccount incluye las constantes msidbCustomActionTypeInScript y msidbCustomActionTypeRollback para especificar estas opciones de ejecución de acciones personalizadas en [script.](custom-action-in-script-execution-options.md)

Estas acciones personalizadas pueden controlar datos confidenciales, como contraseñas de usuario, que no deben escribirse en el archivo de registro. Por lo tanto, las acciones personalizadas diferidas deben incluir msidbCustomActionTypeHideTarget en el tipo de acción personalizada. Los nombres de las acciones personalizadas diferidas también deben agregarse a la lista de propiedades [**MsiHiddenProperties**](msihiddenproperties.md) de la tabla [Property](property-table.md) debido a la manera en que las acciones personalizadas inmediatas pasan datos a acciones personalizadas diferidas mediante la propiedad CustomActionData.



| Acción personalizada     | Punto de entrada de DLL                       | Tipo de acción personalizada                                                                                                                                                         |
|-------------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProcessAccounts   | ProcessUserAccounts en Process.dll.   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| UninstallAccounts | UninstallUserAccounts en Process.dll. | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| CreateAccount     | CreateUserAccount en Create.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265. |
| RemoveAccount     | RemoveUserAccount en Remove.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265. |
| RollbackAccount   | RemoveUserAccount en Remove.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeRollback + msidbCustomActionTypeHideTarget = 9473.       |



 

Continúe con [Creación de la tabla CustomAction](authoring-the-customaction-table.md).

 

 



