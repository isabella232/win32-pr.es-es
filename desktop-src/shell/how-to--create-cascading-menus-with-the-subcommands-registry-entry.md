---
description: En Windows 7 y versiones posteriores, puede usar la entrada SubCommands del Registro para crear menús en cascada mediante el procedimiento indicado en este tema.
title: Crear menús en cascada con la entrada del Registro SubCommands
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b1168daae5ea927f079c66eb436c099f8b3d96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572524"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a>Cómo crear menús en cascada con la entrada del Registro SubCommands

En Windows 7 y versiones posteriores, puede usar la entrada SubCommands del Registro para crear menús en cascada mediante el procedimiento indicado en este tema.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Paso 1:

Cree una nueva subclave en el shell de ProgID raíz **HKEY \_ CLASSES \_**, donde ProgID es el tipo de archivo para el que desea agregar \\  \\ un menú en cascada.  Puede nombrar esta nueva subclave como quiera. En el resto de este tema, lo llamaremos *CascadeMenu*, como se muestra en el ejemplo siguiente.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a>Paso 2:

Agregue una entrada denominada "SZVerb", de tipo **REG \_ SZ** o **REG EXPAND \_ \_ SZ,** a la subclave *CascadeMenu.* Asigne a esta entrada un valor de cadena como "Test Cascade Menu". Normalmente, esta cadena se proporciona como una referencia de recurso con el formato @file ", resource". No se debe establecer el valor (predeterminado) de la subclave *CascadeMenu.*

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a>Paso 3:

Agregue una entrada denominada "SubCommands", de tipo **REG \_ SZ** o **REG EXPAND \_ \_ SZ,** a la subclave *CascadeMenu.* Asigne a esta entrada una lista delimitada por punto y coma de los verbos que deben aparecer en el menú, en el orden de apariencia deseado.

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a>Paso 4:

Rellene la **subclave CommandStore** con implementaciones de verbo para cualquier método de implementación de verbo estático personalizado que haya usado en la entrada SubCommands; por ejemplo:

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

[Crear menús estáticos en cascada](creating-static-cascading-menus.md)
</dt> </dl>

 

 



