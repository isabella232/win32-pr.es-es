---
description: Muestra cómo invocar un comando DDE mediante un verbo shell.
ms.assetid: 65DDD992-5E96-447E-9151-2CCA740822A1
title: Asociación de verbos con comandos DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7174a22c993d93c347c8a0368fa7d1798362070f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360374"
---
# <a name="how-to-associate-verbs-with-dde-commands"></a>Asociación de verbos con comandos DDE

Al invocar un verbo normalmente se inicia la aplicación especificada por la subclave command del verbo. Sin embargo, si la aplicación admite datos dinámicos Exchange (DDE), puede hacer que shell inicie una conversación de DDE.

Para especificar que la invocación de un verbo debe iniciar una conversación de DDE, siga estos pasos.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Paso 1:

Agregue una **subclave ddeexec** a la clave del verbo.

### <a name="step-2"></a>Paso 2:

Establezca el valor predeterminado de **ddeexec en** la cadena de comando DDE.

## <a name="remarks"></a>Observaciones

La **clave ddeexec** tiene tres subclaves opcionales que proporcionan cierto control sobre el proceso DDE:

-   **aplicación**. Establezca el valor predeterminado de esta subclave en el nombre de la aplicación que se usará para establecer la conversación de DDE. Si no hay ninguna **subclave** de aplicación, se usa el valor predeterminado de la **subclave** de comandos del verbo como nombre de la aplicación.
-   **tema**. Establezca el valor predeterminado de esta subclave en el nombre del tema de la conversación de DDE. Si no hay ninguna **subclave** de tema, system se usa como nombre del tema.
-   **ifexec**. Establezca el valor predeterminado de esta subclave en el comando DDE que se usará si no se puede iniciar la conversación de DDE. Cuando se produce un error de iniciación, se inicia la aplicación especificada por el valor predeterminado de la subclave **command** del verbo. Si existe **una clave ifexec,** su valor predeterminado se usará como comando DDE. Si no hay ninguna subclave **ifexec,** el valor predeterminado de la clave **ddeexec** se usará de nuevo como comando DDE.

En el ejemplo siguiente se especifica que al invocar el verbo abierto para MyProgram.1 se inicia una conversación de DDE con un comando DDE de Open("%1") y un nombre de aplicación de MyProgram.

```
HKEY_CLASSES_ROOT
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
            ddeexec
               (Default) = Open("%1")
               application
                  (Default) = MyProgram
```

 

 



