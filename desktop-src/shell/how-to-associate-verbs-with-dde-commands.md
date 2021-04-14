---
description: Muestra cómo invocar un comando DDE mediante un verbo de Shell.
ms.assetid: 65DDD992-5E96-447E-9151-2CCA740822A1
title: Cómo asociar verbos con comandos DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7174a22c993d93c347c8a0368fa7d1798362070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985463"
---
# <a name="how-to-associate-verbs-with-dde-commands"></a>Cómo asociar verbos con comandos DDE

Al invocar un verbo, normalmente se inicia la aplicación especificada por la subclave del comando del verbo. Sin embargo, si la aplicación admite Intercambio dinámico de datos (DDE), puede iniciar una conversación DDE en su lugar.

Para especificar que la invocación de un verbo debe iniciar una conversación DDE, siga estos pasos.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Agregue una subclave **ddeexec** a la clave del verbo.

### <a name="step-2"></a>Paso 2:

Establezca el valor predeterminado de **ddeexec** en la cadena de comandos DDE.

## <a name="remarks"></a>Observaciones

La clave **ddeexec** tiene tres subclaves opcionales que proporcionan cierto control sobre el proceso DDE:

-   **aplicación**. Establezca el valor predeterminado de esta subclave en el nombre de la aplicación que se utilizará para establecer la conversación DDE. Si no hay ninguna subclave de la **aplicación** , se usa el valor predeterminado de la subclave del **comando** del verbo como el nombre de la aplicación.
-   **tema**. Establezca el valor predeterminado de esta subclave en el nombre de tema de la conversación DDE. Si no hay subclave de **tema** , el sistema se usa como nombre del tema.
-   **ifexec**. Establezca el valor predeterminado de esta subclave en el comando DDE que se utilizará si no se puede iniciar la conversación DDE. Cuando se produce un error en la inicialización, se inicia la aplicación especificada por el valor predeterminado de la subclave del **comando** del verbo. Si existe una clave **ifexec** , su valor predeterminado se usará como el comando DDE. Si no hay ninguna subclave **ifexec** , el valor predeterminado de la clave **ddeexec** se utilizará de nuevo como el comando DDE.

En el ejemplo siguiente se especifica que al invocar el verbo Open para el programa. 1 se inicia una conversación DDE con un comando DDE de Open ("%1") y un nombre de aplicación de mi programa.

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

 

 



