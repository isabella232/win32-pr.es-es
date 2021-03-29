---
description: Agregue todas las propiedades de contraseña de la tabla CustomUserAccounts a la propiedad MsiHiddenProperties de la tabla de propiedades.
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: Protección de la instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add5211327508dbbf6531c48c3d2ae40f095375d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003134"
---
# <a name="securing-the-installation"></a>Protección de la instalación

Agregue todas las propiedades de contraseña de la tabla CustomUserAccounts a la propiedad [**MsiHiddenProperties**](msihiddenproperties.md) de la [tabla de propiedades](property-table.md). Agregue también los nombres de las acciones personalizadas diferidas a la propiedad **MsiHiddenProperties** . Esto impedirá que el instalador escriba los valores de propiedad confidenciales (las contraseñas) en el registro y garantizará que estos valores no se registran cuando las acciones personalizadas diferidas usan los valores como la propiedad CustomActionData.

Para que la contraseña del usuario esté disponible en el servicio de Windows Installer, la propiedad password debe agregarse a la propiedad [**SecureCustomProperties**](securecustomproperties.md) .

[Tabla de propiedades](property-table.md)



| Propiedad                                                 | Value                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**MsiHiddenProperties**](msihiddenproperties.md)       | TESTUSERPASSWORD; CreateAccount; RemoveAccount RollbackAccount |
| [**SecureCustomProperties**](securecustomproperties.md) | TESTUSERPASSWORD                                             |



 

Esto concluye el ejemplo.

 

 



