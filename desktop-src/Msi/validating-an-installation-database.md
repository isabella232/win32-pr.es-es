---
description: Los autores de paquetes de instalación siempre deben ejecutar la validación en sus paquetes antes de intentar instalar el paquete por primera vez y volver a ejecutar la validación cada vez que realicen cambios en el paquete.
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: Validar una base de datos de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28d4d1937b5946d6c1df85a4c6c21ec8113ef6463b5aaad0e181f4bdc711e70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995825"
---
# <a name="validating-an-installation-database"></a>Validar una base de datos de instalación

Los autores de paquetes de instalación siempre deben ejecutar la validación en sus paquetes antes de intentar instalar el paquete por primera vez y volver a ejecutar la validación cada vez que realicen cambios en el paquete. La validación examina la base de datos en busca de errores que pueden parecer válidos individualmente, pero que provocan un comportamiento incorrecto en el contexto de toda la base de datos. Si se intenta instalar un paquete que produce un error en la validación, se puede dañar el sistema del usuario. Consulte las secciones Validación de [paquetes](package-validation.md) y Evaluadores de coherencia [interna : ICEs](internal-consistency-evaluators-ices.md).

Puede validar el paquete de ejemplo mediante [Orca.exe](orca-exe.md) o [Msival2.exe](msival2-exe.md). Para ver la ayuda para cambiar Msival2.exe directorios y escriba en la línea de comandos.

Msival2 -?

El archivo .rev darice.rev contiene las acciones personalizadas de ICE que necesita Msival2.exe para realizar la validación. Para validar el MNP2000.msi entrar

msival2 MNP2000.msi Darice.rev

Para obtener una descripción de los mensajes de error y advertencia devueltos por la validación, vea la [referencia de ICE](ice-reference.md). Corrija todos los errores del paquete y vuelva a ejecutar la validación según sea necesario hasta que el paquete pase la validación sin errores.

Una vez que el paquete pasa la validación, puede instalar el paquete de ejemplo haciendo clic en el icono de MNP2000.msi o desde la línea de comandos mediante las opciones de [la línea de comandos](command-line-options.md).

Esto completa la instalación de ejemplo.

## <a name="next-example"></a>Ejemplo siguiente

[Ejemplo de actualización](an-upgrade-example.md)

 

 



