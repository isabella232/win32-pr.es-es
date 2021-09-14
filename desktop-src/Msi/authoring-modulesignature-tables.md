---
description: La tabla ModuleSignature contiene toda la información necesaria para identificar el módulo de combinación.
ms.assetid: 5f0b4590-dac3-4528-b714-ff760ae8d123
title: Creación de tablas ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796775b0237c17db4fa21075a792c372bed3e97b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159027"
---
# <a name="authoring-modulesignature-tables"></a>Creación de tablas ModuleSignature

La [tabla ModuleSignature](modulesignature-table.md) contiene toda la información necesaria para identificar el módulo de combinación.

El campo ModuleID es la clave principal de esta tabla y debe seguir la convención descrita en Nomenclatura de claves principales en bases de datos [de módulos de mezcla](naming-primary-keys-in-merge-module-databases.md). Por ejemplo, si el nombre legible del módulo de mezcla es MyLibrary y el GUID del módulo de mezcla es {880DE2F0-CDD8-11D1-A849-006097ABDE17}, La entrada de la columna ModuleID de la tabla ModuleSignature se convierte en MyLibrary.880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.

Escriba el identificador decimal del idioma predeterminado del módulo merge en el campo Idioma de la tabla ModuleSignature.

Escriba la versión del módulo merge en el campo Versión.

 

 



