---
description: Puede usar el Registro para especificar que al ir a un punto de unión se abrirá una vista raíz en lugar de la vista predeterminada del contenido de la extensión asociada.
title: Cómo abrir una vista con raíz de un punto de unión a través del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa51e87ccb541e995300cb010f82c79e33112e16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468188"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a>Cómo abrir una vista con raíz de un punto de unión a través del Registro

Puede usar el Registro para especificar que al ir a un punto de unión se abrirá una vista raíz en lugar de la vista predeterminada del contenido de la extensión asociada.

## <a name="instructions"></a>Instructions


Para especificar que la exploración en un punto de unión debe abrir una vista con raíz, agregue subclaves Abrir comando y Explorar comando a la \\  subclave  \\  **CLSID** de la extensión, con sus valores predeterminados asignados a las líneas de comandos que se muestran aquí:

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

Una vez que haya agregado esos valores, se inicia una instancia de Explorer.exe para mostrar el contenido de la extensión como una vista con raíz cuando el usuario selecciona el punto de unión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificar la ubicación de una extensión de espacio de nombres](nse-junction.md)
</dt> <dt>

[Cómo abrir una vista raíz de un punto de unión a través de un archivo de acceso directo](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



