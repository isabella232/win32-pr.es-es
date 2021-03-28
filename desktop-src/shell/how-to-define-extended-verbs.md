---
description: Puede utilizar el registro para definir uno o más verbos extendidos. Los comandos asociados solo se mostrarán cuando el usuario haga clic con el botón derecho en un objeto mientras presiona la tecla Mayús.
ms.assetid: C6E51716-1D4F-454F-9AF4-8D0E486CB885
title: Cómo definir verbos extendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4bd8cca04b40bb0b0b77bab5fd7546fd5bff45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985450"
---
# <a name="how-to-define-extended-verbs"></a><span data-ttu-id="f103f-104">Cómo definir verbos extendidos</span><span class="sxs-lookup"><span data-stu-id="f103f-104">How to Define Extended Verbs</span></span>

<span data-ttu-id="f103f-105">Puede utilizar el registro para definir uno o más verbos extendidos.</span><span class="sxs-lookup"><span data-stu-id="f103f-105">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="f103f-106">Los comandos asociados solo se mostrarán cuando el usuario haga clic con el botón derecho en un objeto mientras presiona la tecla Mayús.</span><span class="sxs-lookup"><span data-stu-id="f103f-106">The associated commands will be displayed only when the user right-clicks an object while pressing the SHIFT key.</span></span>

## <a name="instructions"></a><span data-ttu-id="f103f-107">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="f103f-107">Instructions</span></span>


<span data-ttu-id="f103f-108">Para definir un verbo como extendido, basta con agregar un valor de **reg \_ SZ** "extendido" a la subclave del verbo.</span><span class="sxs-lookup"><span data-stu-id="f103f-108">To define a verb as extended, simply add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="f103f-109">El valor no debe tener ningún dato asociado.</span><span class="sxs-lookup"><span data-stu-id="f103f-109">The value should not have any data associated with it.</span></span> <span data-ttu-id="f103f-110">En la siguiente entrada del registro de ejemplo se muestra el ejemplo de la sección anterior, con "doit" definido como verbo extendido.</span><span class="sxs-lookup"><span data-stu-id="f103f-110">The following sample registry entry shows the example from the previous section, with "doit" defined as an extended verb.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            extended
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

 

 



