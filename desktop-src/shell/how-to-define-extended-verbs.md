---
description: Puede usar el Registro para definir uno o varios verbos extendidos. Los comandos asociados solo se mostrarán cuando el usuario haga clic con el botón derecho en un objeto mientras presiona la tecla MAYÚS.
ms.assetid: C6E51716-1D4F-454F-9AF4-8D0E486CB885
title: Definición de verbos extendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef73244a03101de02653625912701b81aa9e8e11d975f96dd417eaa137bfba07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859722"
---
# <a name="how-to-define-extended-verbs"></a>Definición de verbos extendidos

Puede usar el Registro para definir uno o varios verbos extendidos. Los comandos asociados solo se mostrarán cuando el usuario haga clic con el botón derecho en un objeto mientras presiona la tecla MAYÚS.

## <a name="instructions"></a>Instructions


Para definir un verbo como extendido, basta con agregar un valor **REG \_ SZ** "extendido" a la subclave del verbo. El valor no debe tener ningún dato asociado. La siguiente entrada del Registro de ejemplo muestra el ejemplo de la sección anterior, con "doit" definido como verbo extendido.

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

 

 



