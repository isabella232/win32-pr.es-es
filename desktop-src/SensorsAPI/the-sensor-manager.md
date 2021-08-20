---
description: El objeto del administrador de sensores proporciona acceso a los sensores que están disponibles para su uso.
ms.assetid: dd39d533-9983-41b4-a9a3-d94dcadebaac
title: El objeto Sensor Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9ce54dd72b642e599d8b7b26b8c94d1531767ec31b5ccd81a47b88746853a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117968418"
---
# <a name="the-sensor-manager-object"></a>El objeto Sensor Manager

El objeto del administrador de sensores proporciona acceso a los sensores que están disponibles para su uso.

Para usar sensor API, primero debe llamar al método COM **CoCreateInstance** para crear una instancia del objeto del administrador de sensores y recuperar un puntero a su interfaz, denominada [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager). El administrador de sensores mantiene la lista de sensores disponibles. Puede usar **ISensorManager** para llamar a métodos que recuperan grupos de sensores por categoría o tipo, o puede llamar a un método para recuperar un sensor determinado mediante su identificador único. El administrador de sensores también le permite registrarse para recibir un evento que le notifica cuándo se ha conectado un nuevo sensor a la plataforma.

A veces, el administrador de sensores proporciona un puntero a un sensor, pero el usuario no lo ha habilitado. Por ejemplo, a menudo puede recuperar valores para propiedades de sensor no privadas, como el fabricante o el modelo del sensor, antes de que el usuario lo permita. Esta información puede ayudarle a decidir si desea pedir permiso al usuario para usar el sensor. Puede llamar a [**ISensorManager::RequestPermissions para**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) pedir al usuario que habilite un sensor o una colección determinados de sensores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de permisos de usuario](managing-user-permissions.md)
</dt> <dt>

[Solicitud de permisos de usuario](requesting-user-permissions.md)
</dt> </dl>

 

 
