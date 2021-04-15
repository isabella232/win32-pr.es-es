---
description: En Windows 7 y versiones posteriores, puede usar la entrada subcomandos del registro para crear menús en cascada mediante el procedimiento que se indica en este tema.
title: Crear menús en cascada con la entrada del registro subcomandos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b1168daae5ea927f079c66eb436c099f8b3d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997713"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a>Cómo crear menús en cascada con la entrada del registro subcomandos

En Windows 7 y versiones posteriores, puede usar la entrada subcomandos del registro para crear menús en cascada mediante el procedimiento que se indica en este tema.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Cree una nueva subclave en **HKEY \_ classes \_ root** \\ *ProgID* \\ **Shell**, donde *ProgID* es el tipo de archivo para el que desea agregar un menú en cascada. Puede asignar a esta nueva subclave cualquier cosa que desee. En el resto de este tema, lo llamaremos *CascadeMenu*, tal y como se muestra en el ejemplo siguiente.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a>Paso 2:

Agregue una entrada denominada "MUIVerb", de tipo **reg \_ SZ** o **reg \_ Expand \_ SZ**, a la subclave *CascadeMenu* . Asigne esta entrada a un valor de cadena como "menú en cascada de prueba". Normalmente, esta cadena se proporciona como una referencia de recurso con el formato " @file , Resource". No se debe establecer el valor (predeterminado) de la subclave *CascadeMenu* .

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a>Paso 3:

Agregue una entrada denominada "subcommands", de tipo **reg \_ SZ** o **reg \_ Expand \_ SZ**, a la subclave *CascadeMenu* . Asigne esta entrada a una lista delimitada por signos de punto y coma de los verbos que deben aparecer en el menú, en el orden de aparición deseado.

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a>Paso 4:

Rellene la subclave **CommandStore** con implementaciones de verbo para cualquier método de implementación de verbo estático personalizado que haya usado en la entrada de subcomandos. por ejemplo:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  CommandStore
                     Shell
                        VerbName
                           command
                              (Default) = notepad.exe %1
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear menús en cascada estáticos](creating-static-cascading-menus.md)
</dt> </dl>

 

 



