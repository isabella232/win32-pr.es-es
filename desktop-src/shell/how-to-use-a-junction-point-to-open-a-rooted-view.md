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
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a><span data-ttu-id="62283-103">Cómo abrir una vista con raíz de un punto de unión a través del registro</span><span class="sxs-lookup"><span data-stu-id="62283-103">How to Open a Rooted View of a Junction Point Through the Registry</span></span>

<span data-ttu-id="62283-104">Puede usar el registro para especificar que al examinar un punto de Unión se abra una vista con raíz en lugar de la vista predeterminada del contenido de la extensión asociada.</span><span class="sxs-lookup"><span data-stu-id="62283-104">You can use the registry to specify that browsing into a junction point will open a rooted view rather than the default view of the contents of the associated extension.</span></span>

## <a name="instructions"></a><span data-ttu-id="62283-105">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="62283-105">Instructions</span></span>


<span data-ttu-id="62283-106">Para especificar que el examen en un punto de Unión debe abrir una vista con raíz, agregue el \\ **comando** Open y **Explore** \\ las subclaves de **comando** a la subclave **CLSID** de la extensión, con sus valores predeterminados asignados a las líneas de comandos que se muestran aquí:</span><span class="sxs-lookup"><span data-stu-id="62283-106">To specify that browsing into a junction point should open a rooted view, add **Open**\\**Command** and **Explore**\\**Command** subkeys to your extension's **CLSID** subkey, with their default values assigned to the command lines shown here:</span></span>

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

<span data-ttu-id="62283-107">Una vez agregados esos valores, se inicia una instancia de Explorer.exe para mostrar el contenido de la extensión como una vista con raíz cuando el usuario selecciona el punto de Unión.</span><span class="sxs-lookup"><span data-stu-id="62283-107">Once you've added those values, an instance of Explorer.exe is launched to display the contents of the extension as a rooted view when the user selects the junction point.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62283-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62283-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62283-109">Especificar la ubicación de una extensión de espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="62283-109">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="62283-110">Cómo abrir una vista con raíz de un punto de unión a través de un archivo de acceso directo</span><span class="sxs-lookup"><span data-stu-id="62283-110">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



