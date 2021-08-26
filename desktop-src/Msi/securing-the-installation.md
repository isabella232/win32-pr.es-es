---
description: Agregue todas las propiedades Password de la tabla CustomUserAccounts a la propiedad MsiHiddenProperties de la tabla Property.
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: Protección de la instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642170cc2ac4e84bebe5235e84328abe5039ede1bdb8fc2760bbd249ff5268de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040735"
---
# <a name="securing-the-installation"></a>Protección de la instalación

Agregue todas las propiedades Password de la tabla CustomUserAccounts a [**la propiedad MsiHiddenProperties**](msihiddenproperties.md) de la [tabla Property](property-table.md). Agregue también los nombres de las acciones personalizadas diferidas a la propiedad **MsiHiddenProperties.** Esto impedirá que el instalador escriba los valores de propiedad confidencial (las contraseñas) en el registro y garantizará que estos valores no se registran cuando las acciones personalizadas diferidas usan los valores como la propiedad CustomActionData.

Para que la contraseña del usuario esté disponible en el servicio Windows Installer, la propiedad password debe agregarse a la [**propiedad SecureCustomProperties.**](securecustomproperties.md)

[Tabla de propiedades](property-table.md)



| Propiedad                                                 | Value                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**MsiHiddenProperties**](msihiddenproperties.md)       | TESTUSERPASSWORD; CreateAccount; RemoveAccount; RollbackAccount |
| [**SecureCustomProperties**](securecustomproperties.md) | TESTUSERPASSWORD                                             |



 

Esto concluye el ejemplo.

 

 



