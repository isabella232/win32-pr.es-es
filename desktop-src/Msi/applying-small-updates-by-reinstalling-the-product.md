---
description: Una actualización pequeña se puede aplicar a una aplicación mediante la reinstalación completa o parcial de la aplicación desde la línea de comandos o desde un programa.
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: Aplicar actualizaciones pequeñas reinstalando el producto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27b97ff0274baac5a4ec30df244394a609ed525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001746"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a>Aplicar actualizaciones pequeñas reinstalando el producto

Una actualización pequeña se puede aplicar a una aplicación mediante la reinstalación completa o parcial de la aplicación desde la línea de comandos o desde un programa.

**Para propagar la actualización pequeña a los usuarios actuales (se trata de una reinstalación completa) desde la línea de comandos**

1.  Desde la línea de comandos, use: **msiexec \[ /fvomus** _ruta de acceso para actualizar el archivo. msi_ *_\]_* o **msiexec/i \[** _path para actualizar el archivo. msi_ *_\] REINSTALL = ALL REINSTALLMODE = vomus_*.
2.  El archivo. msi actualizado se almacena en caché en el equipo del usuario. Tenga en cuenta que no es posible que el usuario vuelva a instalar el producto mediante agregar o quitar programas, ya que el archivo. msi actualizado aún no se encuentra en el equipo del usuario.

**Para propagar una pequeña actualización a los usuarios actuales (se trata de una reinstalación completa) de un programa**

1.  En un programa, llame a [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) y especifique el \_ método REINSTALLMODE, REINSTALLMODE \_ FILEOLDERVERSION, REINSTALLMODE \_ MACHINEDATA, REINSTALLMODE \_ USERDATA y REINSTALLMODE \_ .
2.  El archivo. msi actualizado se almacena en caché en el equipo del usuario.

El método siguiente inicia una reinstalación de solo las características o los componentes que se ven afectados por la actualización pequeña.

**Para propagar una pequeña actualización a los usuarios actuales (se trata de una reinstalación parcial)**

1.  Obtenga una lista de los nombres de las características y los componentes que se ven afectados por la actualización pequeña.
2.  En el símbolo del sistema, use **: \[ msiexec/i** _rutaDeAcceso para actualizar el archivo. msi_ *_\] REINSTALL = \[_* lista _\] de características_ **REINSTALLMODE = vomus**.
3.  El archivo. msi actualizado se almacena en caché en el equipo del usuario.

 

 



