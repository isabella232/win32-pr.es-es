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
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="74f5a-103">Cómo crear menús en cascada con la entrada del registro subcomandos</span><span class="sxs-lookup"><span data-stu-id="74f5a-103">How to Create Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="74f5a-104">En Windows 7 y versiones posteriores, puede usar la entrada subcomandos del registro para crear menús en cascada mediante el procedimiento que se indica en este tema.</span><span class="sxs-lookup"><span data-stu-id="74f5a-104">In Windows 7 and later, you can use the SubCommands entry in the registry to create cascading menus by using the procedure given in this topic.</span></span>

## <a name="instructions"></a><span data-ttu-id="74f5a-105">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="74f5a-105">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="74f5a-106">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="74f5a-106">Step 1:</span></span>

<span data-ttu-id="74f5a-107">Cree una nueva subclave en **HKEY \_ classes \_ root** \\ *ProgID* \\ **Shell**, donde *ProgID* es el tipo de archivo para el que desea agregar un menú en cascada.</span><span class="sxs-lookup"><span data-stu-id="74f5a-107">Create a new subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell**, where *ProgID* is the file type for which you want to add a cascading menu.</span></span> <span data-ttu-id="74f5a-108">Puede asignar a esta nueva subclave cualquier cosa que desee.</span><span class="sxs-lookup"><span data-stu-id="74f5a-108">You can name this new subkey anything you'd like.</span></span> <span data-ttu-id="74f5a-109">En el resto de este tema, lo llamaremos *CascadeMenu*, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="74f5a-109">For the remainder of this topic, we'll call it *CascadeMenu*, as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a><span data-ttu-id="74f5a-110">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="74f5a-110">Step 2:</span></span>

<span data-ttu-id="74f5a-111">Agregue una entrada denominada "MUIVerb", de tipo **reg \_ SZ** o **reg \_ Expand \_ SZ**, a la subclave *CascadeMenu* .</span><span class="sxs-lookup"><span data-stu-id="74f5a-111">Add an entry named "MUIVerb", of type **REG\_SZ** or **REG\_EXPAND\_SZ**, to the *CascadeMenu* subkey.</span></span> <span data-ttu-id="74f5a-112">Asigne esta entrada a un valor de cadena como "menú en cascada de prueba".</span><span class="sxs-lookup"><span data-stu-id="74f5a-112">Assign this entry a string value such as "Test Cascade Menu".</span></span> <span data-ttu-id="74f5a-113">Normalmente, esta cadena se proporciona como una referencia de recurso con el formato " @file , Resource".</span><span class="sxs-lookup"><span data-stu-id="74f5a-113">Normally, this string is provided as a resource reference in the form "@file, resource".</span></span> <span data-ttu-id="74f5a-114">No se debe establecer el valor (predeterminado) de la subclave *CascadeMenu* .</span><span class="sxs-lookup"><span data-stu-id="74f5a-114">The (Default) value for the *CascadeMenu* subkey should not be set.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a><span data-ttu-id="74f5a-115">Paso 3:</span><span class="sxs-lookup"><span data-stu-id="74f5a-115">Step 3:</span></span>

<span data-ttu-id="74f5a-116">Agregue una entrada denominada "subcommands", de tipo **reg \_ SZ** o **reg \_ Expand \_ SZ**, a la subclave *CascadeMenu* .</span><span class="sxs-lookup"><span data-stu-id="74f5a-116">Add an entry named "SubCommands", of type **REG\_SZ** or **REG\_EXPAND\_SZ**, to the *CascadeMenu* subkey.</span></span> <span data-ttu-id="74f5a-117">Asigne esta entrada a una lista delimitada por signos de punto y coma de los verbos que deben aparecer en el menú, en el orden de aparición deseado.</span><span class="sxs-lookup"><span data-stu-id="74f5a-117">Assign this entry a semicolon-delimited list of the verbs that should appear on the menu, in their desired order of appearance.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a><span data-ttu-id="74f5a-118">Paso 4:</span><span class="sxs-lookup"><span data-stu-id="74f5a-118">Step 4:</span></span>

<span data-ttu-id="74f5a-119">Rellene la subclave **CommandStore** con implementaciones de verbo para cualquier método de implementación de verbo estático personalizado que haya usado en la entrada de subcomandos. por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="74f5a-119">Populate the **CommandStore** subkey with verb implementations for any custom static verb implementation methods that you've used in your SubCommands entry; for example:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="74f5a-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74f5a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74f5a-121">Crear menús en cascada estáticos</span><span class="sxs-lookup"><span data-stu-id="74f5a-121">Creating Static Cascading Menus</span></span>](creating-static-cascading-menus.md)
</dt> </dl>

 

 



