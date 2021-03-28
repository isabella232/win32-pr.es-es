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
# <a name="how-to-define-extended-verbs"></a>Cómo definir verbos extendidos

Puede utilizar el registro para definir uno o más verbos extendidos. Los comandos asociados solo se mostrarán cuando el usuario haga clic con el botón derecho en un objeto mientras presiona la tecla Mayús.

## <a name="instructions"></a>Instrucciones


Para definir un verbo como extendido, basta con agregar un valor de **reg \_ SZ** "extendido" a la subclave del verbo. El valor no debe tener ningún dato asociado. En la siguiente entrada del registro de ejemplo se muestra el ejemplo de la sección anterior, con "doit" definido como verbo extendido.

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

 

 



