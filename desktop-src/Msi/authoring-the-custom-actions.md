---
description: 'En la tabla siguiente se enumeran las cinco acciones personalizadas que se usan para cumplir las especificaciones de ejemplo: ProcessAccounts, UninstallAccounts, CreateAccounts, RemoveAccounts y RollbackAccounts.'
ms.assetid: 389ec652-243e-4392-aec9-3a7eb90e6c68
title: Crear las acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09525490304762b98635bcbbe6c238ce3fe413f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001724"
---
# <a name="authoring-the-custom-actions"></a>Crear las acciones personalizadas

En la tabla siguiente se enumeran las cinco acciones personalizadas que se usan para cumplir las especificaciones de ejemplo: ProcessAccounts, UninstallAccounts, CreateAccounts, RemoveAccounts y RollbackAccounts. Todas estas acciones personalizadas se encuentran en [bibliotecas de vínculos dinámicos](dynamic-link-libraries.md) almacenadas en la [tabla binaria](binary-table.md). El código fuente de C++ para las bibliotecas de vínculos dinámicos que contienen las acciones personalizadas de ejemplo se proporciona en el SDK de Windows Installer. ProcessAccounts y UninstallAccounts están en el archivo Process. cpp. CreateAccount se encuentra en el archivo Create. cpp. RemoveAccount y RollbackAccount se encuentran en el archivo Remove. cpp. Estos archivos de origen se pueden usar para crear los archivos Process.dll, Create.dll y Remove.dll.

Dado que la creación o eliminación de una cuenta de usuario requiere privilegios elevados, las [acciones personalizadas de ejecución diferida](deferred-execution-custom-actions.md) que se ejecutan en el contexto del sistema deben usarse para crear, quitar o revertir cuentas de usuario. Las acciones personalizadas de ejecución inmediata, ProcessAccounts y UninstallAccounts, generan las acciones personalizadas diferidas que crean, quitan o revierten las cuentas de usuario: CreateAccount, RemoveAccount y RollbackAccount.

Dado que las acciones personalizadas diferidas no pueden leer información en las tablas de base de datos, ProcessAccounts y UninstallUserAccouts deben establecer una propiedad CustomActionData para pasar la información de la tabla de conjunto de datos a las acciones personalizadas diferidas, tal y como se describe en [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md). Cuando el instalador ejecuta el script de ejecución, las acciones personalizadas diferidas administran las cuentas de usuario según la información de la propiedad CustomActionData.

Dado que todas las acciones personalizadas están en bibliotecas de vínculos dinámicos almacenadas en la tabla binaria, todas incluyen las constantes msidbCustomActionTypeDll y msidbCustomActionTypeBinaryData en su tipo numérico base. ProcessAccounts y UninstallAccounts son ejemplos de [acción personalizada pura tipo 1](custom-action-type-1.md). Para obtener información sobre otros tipos de acciones personalizadas, vea la [lista de Resumen de todos los tipos de acción personalizados](summary-list-of-all-custom-action-types.md).

CreateAccount y RemoveAccount son [acciones personalizadas de ejecución aplazada](deferred-execution-custom-actions.md) que no permiten que los servicios suplanten a usuarios concretos. Estas acciones personalizadas incluyen las constantes msidbCustomActionTypeInScript y msidbCustomActionTypeNoImpersonate para especificar estas [acciones personalizadas en las opciones de ejecución del script](custom-action-in-script-execution-options.md).

RollbackAccount es una [acción personalizada de reversión](rollback-custom-actions.md) que solo quita las cuentas de usuario durante una [instalación de reversión](rollback-installation.md). RollbackAccount incluye las constantes msidbCustomActionTypeInScript y msidbCustomActionTypeRollback para especificar estas [acciones personalizadas en las opciones de ejecución del script](custom-action-in-script-execution-options.md).

Estas acciones personalizadas pueden controlar datos confidenciales, como contraseñas de usuario, que no se deben escribir en el archivo de registro. Por lo tanto, las acciones personalizadas diferidas deben incluir msidbCustomActionTypeHideTarget en el tipo de acción personalizada. Los nombres de las acciones personalizadas diferidas también deben agregarse a la lista de propiedades [**MsiHiddenProperties**](msihiddenproperties.md) en la [tabla de propiedades](property-table.md) debido a la manera en que las acciones personalizadas inmediatas pasan datos a acciones personalizadas diferidas mediante la propiedad CustomActionData.



| Acción personalizada     | Punto de entrada de DLL                       | Tipo de acción personalizada                                                                                                                                                         |
|-------------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProcessAccounts   | ProcessUserAccounts en Process.dll.   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| UninstallAccounts | UninstallUserAccounts en Process.dll. | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| CreateAccount     | CreateUserAccount en Create.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265. |
| RemoveAccount     | RemoveUserAccount en Remove.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265. |
| RollbackAccount   | RemoveUserAccount en Remove.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeRollback + msidbCustomActionTypeHideTarget = 9473.       |



 

Continúe con [la creación de la tabla CustomAction](authoring-the-customaction-table.md).

 

 



