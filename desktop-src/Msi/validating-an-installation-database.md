---
description: Los autores de los paquetes de instalación siempre deben ejecutar la validación en sus paquetes antes de intentar instalar el paquete por primera vez y volver a ejecutar la validación cada vez que realice cambios en el paquete.
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: Validar una base de datos de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6db262a280afa1d9222696d40a6f5949d69ece0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907612"
---
# <a name="validating-an-installation-database"></a>Validar una base de datos de instalación

Los autores de los paquetes de instalación siempre deben ejecutar la validación en sus paquetes antes de intentar instalar el paquete por primera vez y volver a ejecutar la validación cada vez que realice cambios en el paquete. La validación examina la base de datos en busca de errores que pueden parecer válidos de forma individual, pero que causan un comportamiento incorrecto en el contexto de toda la base de datos. Si intenta instalar un paquete que no supera la validación, puede dañar el sistema del usuario. Vea las secciones [validación de paquetes](package-validation.md) y [evaluadores de coherencia interna-CIEM](internal-consistency-evaluators-ices.md).

Puede validar el paquete de ejemplo mediante [Orca.exe](orca-exe.md) o [Msival2.exe](msival2-exe.md). Para ver la ayuda de Msival2.exe cambie los directorios y escriba en la línea de comandos.

Msival2 -?

El archivo. Cub Darice. Cub contiene las acciones personalizadas de ICE que necesita Msival2.exe para realizar la validación. Para validar el MNP2000.msi escriba

msival2 MNP2000.msi Darice. Cub

Para obtener una descripción de los mensajes de error y de advertencia devueltos por la validación, consulte la [referencia de ICE](ice-reference.md). Corrija todos los errores del paquete y vuelva a ejecutar la validación según sea necesario hasta que el paquete pase la validación sin errores.

Una vez que el paquete pasa la validación, puede instalar el paquete de ejemplo haciendo clic en el icono de MNP2000.msi o desde la línea de comandos con las opciones de la [línea de comandos](command-line-options.md).

Esto completa la instalación de ejemplo.

## <a name="next-example"></a>Ejemplo siguiente

[Un ejemplo de actualización](an-upgrade-example.md)

 

 



