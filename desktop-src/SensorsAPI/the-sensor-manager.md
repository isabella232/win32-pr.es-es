---
description: El objeto de administrador de sensor proporciona acceso a los sensores que están disponibles para su uso.
ms.assetid: dd39d533-9983-41b4-a9a3-d94dcadebaac
title: El objeto de administrador de sensores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715448a62c058c5e6825368003939e5ae2066847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154057"
---
# <a name="the-sensor-manager-object"></a>El objeto de administrador de sensores

El objeto de administrador de sensor proporciona acceso a los sensores que están disponibles para su uso.

Para usar la API de sensor, primero debe llamar al método **CoCreateInstance** de com para crear una instancia del objeto de administrador de sensor y recuperar un puntero a su interfaz, denominada [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager). El administrador del sensor mantiene la lista de sensores disponibles. Puede usar **ISensorManager** para llamar a métodos que recuperen grupos de sensores por categoría o por tipo, o puede llamar a un método para recuperar un sensor determinado mediante su identificador único. El administrador del sensor también le permite registrarse para recibir un evento que le informa cuando se ha conectado un nuevo sensor a la plataforma.

A veces, el administrador del sensor proporciona un puntero a un sensor, pero el usuario no ha habilitado el sensor. Por ejemplo, a menudo puede recuperar los valores de las propiedades del sensor no privado, como el fabricante o el modelo del sensor, antes de que el usuario habilite el sensor. Esta información puede ayudarle a decidir si desea solicitar al usuario permiso para usar el sensor. Puede llamar a [**ISensorManager:: RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) para solicitar al usuario que habilite un sensor determinado o una colección de sensores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrar permisos de usuario](managing-user-permissions.md)
</dt> <dt>

[Solicitar permisos de usuario](requesting-user-permissions.md)
</dt> </dl>

 

 
