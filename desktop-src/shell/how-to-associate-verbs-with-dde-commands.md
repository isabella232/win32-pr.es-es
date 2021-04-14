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
# <a name="how-to-associate-verbs-with-dde-commands"></a><span data-ttu-id="7868e-103">Cómo asociar verbos con comandos DDE</span><span class="sxs-lookup"><span data-stu-id="7868e-103">How to Associate Verbs with DDE Commands</span></span>

<span data-ttu-id="7868e-104">Al invocar un verbo, normalmente se inicia la aplicación especificada por la subclave del comando del verbo.</span><span class="sxs-lookup"><span data-stu-id="7868e-104">Invoking a verb ordinarily launches the application that is specified by the verb's command subkey.</span></span> <span data-ttu-id="7868e-105">Sin embargo, si la aplicación admite Intercambio dinámico de datos (DDE), puede iniciar una conversación DDE en su lugar.</span><span class="sxs-lookup"><span data-stu-id="7868e-105">However, if your application supports Dynamic Data Exchange (DDE), you can instead have the Shell initiate a DDE conversation.</span></span>

<span data-ttu-id="7868e-106">Para especificar que la invocación de un verbo debe iniciar una conversación DDE, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="7868e-106">To specify that invoking a verb should initiate a DDE conversation, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="7868e-107">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="7868e-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="7868e-108">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="7868e-108">Step 1:</span></span>

<span data-ttu-id="7868e-109">Agregue una subclave **ddeexec** a la clave del verbo.</span><span class="sxs-lookup"><span data-stu-id="7868e-109">Add a **ddeexec** subkey to the verb's key.</span></span>

### <a name="step-2"></a><span data-ttu-id="7868e-110">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="7868e-110">Step 2:</span></span>

<span data-ttu-id="7868e-111">Establezca el valor predeterminado de **ddeexec** en la cadena de comandos DDE.</span><span class="sxs-lookup"><span data-stu-id="7868e-111">Set the default value of **ddeexec** to the DDE command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="7868e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7868e-112">Remarks</span></span>

<span data-ttu-id="7868e-113">La clave **ddeexec** tiene tres subclaves opcionales que proporcionan cierto control sobre el proceso DDE:</span><span class="sxs-lookup"><span data-stu-id="7868e-113">The **ddeexec** key has three optional subkeys that provide some control over the DDE process:</span></span>

-   <span data-ttu-id="7868e-114">**aplicación**.</span><span class="sxs-lookup"><span data-stu-id="7868e-114">**application**.</span></span> <span data-ttu-id="7868e-115">Establezca el valor predeterminado de esta subclave en el nombre de la aplicación que se utilizará para establecer la conversación DDE.</span><span class="sxs-lookup"><span data-stu-id="7868e-115">Set the default value of this subkey to the application name to be used to establish the DDE conversation.</span></span> <span data-ttu-id="7868e-116">Si no hay ninguna subclave de la **aplicación** , se usa el valor predeterminado de la subclave del **comando** del verbo como el nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7868e-116">If there is no **application** subkey, the default value of the verb's **command** subkey is used as the application name.</span></span>
-   <span data-ttu-id="7868e-117">**tema**.</span><span class="sxs-lookup"><span data-stu-id="7868e-117">**topic**.</span></span> <span data-ttu-id="7868e-118">Establezca el valor predeterminado de esta subclave en el nombre de tema de la conversación DDE.</span><span class="sxs-lookup"><span data-stu-id="7868e-118">Set the default value of this subkey to the topic name of the DDE conversation.</span></span> <span data-ttu-id="7868e-119">Si no hay subclave de **tema** , el sistema se usa como nombre del tema.</span><span class="sxs-lookup"><span data-stu-id="7868e-119">If there is no **topic** subkey, System is used as the topic name.</span></span>
-   <span data-ttu-id="7868e-120">**ifexec**.</span><span class="sxs-lookup"><span data-stu-id="7868e-120">**ifexec**.</span></span> <span data-ttu-id="7868e-121">Establezca el valor predeterminado de esta subclave en el comando DDE que se utilizará si no se puede iniciar la conversación DDE.</span><span class="sxs-lookup"><span data-stu-id="7868e-121">Set the default value of this subkey to the DDE command to be used if DDE conversation cannot be initiated.</span></span> <span data-ttu-id="7868e-122">Cuando se produce un error en la inicialización, se inicia la aplicación especificada por el valor predeterminado de la subclave del **comando** del verbo.</span><span class="sxs-lookup"><span data-stu-id="7868e-122">When initiation fails, the application that is specified by the default value of the verb's **command** subkey is launched.</span></span> <span data-ttu-id="7868e-123">Si existe una clave **ifexec** , su valor predeterminado se usará como el comando DDE.</span><span class="sxs-lookup"><span data-stu-id="7868e-123">If an **ifexec** key exists, its default value will then be used as the DDE command.</span></span> <span data-ttu-id="7868e-124">Si no hay ninguna subclave **ifexec** , el valor predeterminado de la clave **ddeexec** se utilizará de nuevo como el comando DDE.</span><span class="sxs-lookup"><span data-stu-id="7868e-124">If there is no **ifexec** subkey, the default value of the **ddeexec** key will be used again as the DDE command.</span></span>

<span data-ttu-id="7868e-125">En el ejemplo siguiente se especifica que al invocar el verbo Open para el programa. 1 se inicia una conversación DDE con un comando DDE de Open ("%1") y un nombre de aplicación de mi programa.</span><span class="sxs-lookup"><span data-stu-id="7868e-125">The following example specifies that invoking the open verb for MyProgram.1 initiates a DDE conversation with a DDE command of Open("%1") and an application name of MyProgram.</span></span>

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

 

 



