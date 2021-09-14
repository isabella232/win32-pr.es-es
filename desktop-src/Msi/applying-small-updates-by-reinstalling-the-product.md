---
description: Una pequeña actualización se puede aplicar a una aplicación reinstalando total o parcialmente la aplicación desde la línea de comandos o desde un programa.
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: Aplicación de actualizaciones pequeñas mediante la reinstalación del producto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27b97ff0274baac5a4ec30df244394a609ed525
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159111"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a>Aplicación de actualizaciones pequeñas mediante la reinstalación del producto

Una pequeña actualización se puede aplicar a una aplicación reinstalando total o parcialmente la aplicación desde la línea de comandos o desde un programa.

**Para propagar la pequeña actualización a los usuarios actuales (se trata de una reinstalación completa) desde la línea de comandos**

1.  Desde la línea de comandos, use: **msiexec \[ /fvomus** path to _updated .msi file_ o *_\]_* **msiexec /I \[** path to updated .msi _file_ *_\] REINSTALL=ALL REINSTALLMODE=vomus_*.
2.  El archivo .msi se almacena en caché en el equipo del usuario. Tenga en cuenta que no es posible que el usuario vuelva a instalar el producto mediante Agregar o quitar programas porque el archivo .msi actualizado aún no está en el equipo del usuario.

**Para propagar una pequeña actualización a los usuarios actuales (esto es una reinstalación completa) desde un programa**

1.  Desde un programa, llame a [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) y especifique REINSTALLMODE \_ PACKAGE, REINSTALLMODE \_ FILEOLDERVERSION, REINSTALLMODE \_ MACHINEDATA, REINSTALLMODE USERDATA y \_ REINSTALLMODE \_ SHORTCUT
2.  El archivo .msi se almacena en caché en el equipo del usuario.

El método siguiente inicia una reinstalación de solo las características o componentes que se ven afectados por la pequeña actualización.

**Para propagar una pequeña actualización a los usuarios actuales (se trata de una reinstalación parcial)**

1.  Obtenga una lista de los nombres de características y componentes que se ven afectados por la pequeña actualización.
2.  En el símbolo del sistema, use: **msiexec /I \[** _path to updated .msi file_ *_\] REINSTALL= \[_* Feature _list \]_ **REINSTALLMODE=vomus**.
3.  El archivo .msi se almacena en caché en el equipo del usuario.

 

 



