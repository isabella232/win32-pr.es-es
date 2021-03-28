---
description: Puede usar el registro para especificar que al examinar un punto de Unión se abra una vista con raíz en lugar de la vista predeterminada del contenido de la extensión asociada.
title: Cómo abrir una vista con raíz de un punto de unión a través del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa51e87ccb541e995300cb010f82c79e33112e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276743"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a>Cómo abrir una vista con raíz de un punto de unión a través del registro

Puede usar el registro para especificar que al examinar un punto de Unión se abra una vista con raíz en lugar de la vista predeterminada del contenido de la extensión asociada.

## <a name="instructions"></a>Instrucciones


Para especificar que el examen en un punto de Unión debe abrir una vista con raíz, agregue el \\ **comando** Open y **Explore** \\ las subclaves de **comando** a la subclave **CLSID** de la extensión, con sus valores predeterminados asignados a las líneas de comandos que se muestran aquí:

```
HKEY_CLASSES_ROOT
   CLSID
      {Extension CLSID}
         Shell
            Open
               Command
                  (Default) = %SYSTEMROOT%\explorer.exe/e,/root,"%1"
            Explore
               Command
                  (Default) = %SYSTEMROOT%\explorer.exe/e,/root,"%1"
```

Una vez agregados esos valores, se inicia una instancia de Explorer.exe para mostrar el contenido de la extensión como una vista con raíz cuando el usuario selecciona el punto de Unión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificar la ubicación de una extensión de espacio de nombres](nse-junction.md)
</dt> <dt>

[Cómo abrir una vista con raíz de un punto de unión a través de un archivo de acceso directo](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



