---
description: En Windows 7 y versiones posteriores, puede usar la subclave ExtendedSubCommandsKey para crear menús en cascada ampliados.
ms.assetid: 6E8B4FB7-D4DB-4DBC-AF6F-59D02CB6AB13
title: Crear menús en cascada con la entrada del registro ExtendedSubCommandsKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220a38825ae250a0d58d30bc7de93f290f819eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813710"
---
# <a name="how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="f8185-103">Cómo crear menús en cascada con la entrada del registro ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="f8185-103">How to Create Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="f8185-104">En Windows 7 y versiones posteriores, puede usar la subclave **ExtendedSubCommandsKey** para crear menús en cascada ampliados.</span><span class="sxs-lookup"><span data-stu-id="f8185-104">In Windows 7 and later, you can use the **ExtendedSubCommandsKey** subkey to create extended cascading menus.</span></span>

<span data-ttu-id="f8185-105">La siguiente captura de pantalla es un ejemplo de un menú en cascada extendido.</span><span class="sxs-lookup"><span data-stu-id="f8185-105">The following screen shot is an example of an extended cascading menu.</span></span>

![captura de pantalla que muestra el menú en cascada ampliado para dispositivos](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="f8185-107">Dado que la **\_ \_ raíz de las clases HKEY** es una combinación de **HKEY \_ Current \_ User** y **HKEY \_ local \_ Machine**, puede registrar los subverbos en la subclave de clases de software del **\_ \_ usuario actual HKEY** \\  \\  .</span><span class="sxs-lookup"><span data-stu-id="f8185-107">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register the subverbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="f8185-108">La ventaja de hacerlo es que el permiso elevado no es necesario.</span><span class="sxs-lookup"><span data-stu-id="f8185-108">The advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="f8185-109">Otras asociaciones de archivo pueden volver a usar todo el conjunto de verbos especificando la misma subclave **ExtendedSubCommandsKey** .</span><span class="sxs-lookup"><span data-stu-id="f8185-109">Other file associations can reuse this entire set of verbs by specifying the same **ExtendedSubCommandsKey** subkey.</span></span> <span data-ttu-id="f8185-110">Si no necesita volver a usar este conjunto de verbos, puede enumerar los verbos en el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="f8185-110">If you do not need to reuse this set of verbs, you can list the verbs under the parent.</span></span> <span data-ttu-id="f8185-111">En este caso, asegúrese de que el valor predeterminado del elemento primario está vacío, tal como se muestra en el ejemplo de entrada del registro de esta sección.</span><span class="sxs-lookup"><span data-stu-id="f8185-111">In this case, make sure the default value of the parent is empty, as illustrated in the registry entry example in this section.</span></span>

## <a name="instructions"></a><span data-ttu-id="f8185-112">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="f8185-112">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="f8185-113">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="f8185-113">Step 1:</span></span>

<span data-ttu-id="f8185-114">Cree una subclave en **HKEY \_ classes \_ root** \\ *ProgID* \\ **Shell** \\ *CascadeMenuKey* y asigne a CascadeMenuKey un nombre como *CascadeTest*, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f8185-114">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell**\\*CascadeMenuKey* and give the CascadeMenuKey a name such as *CascadeTest*, for example.</span></span> <span data-ttu-id="f8185-115">A continuación, agregue una entrada MUIVerb del tipo **reg \_ SZ** y asígnele un nombre como el menú de prueba en cascada 2, tal como se muestra en el siguiente ejemplo del registro.</span><span class="sxs-lookup"><span data-stu-id="f8185-115">Then add a MUIVerb entry of **REG\_SZ** type and give it a name such as Test Cascade Menu 2, as illustrated in the following registry example.</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      shell
         CascadeTest
            MUIVerb = Test Cascade Menu 2
```

### <a name="step-2"></a><span data-ttu-id="f8185-116">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="f8185-116">Step 2:</span></span>

<span data-ttu-id="f8185-117">En la subclave *CascadeTest* que creó, agregue una subclave **ExtendedSubCommandsKey** y, a continuación, agregue los subcomandos de documento (de tipo **reg \_ SZ**); por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f8185-117">Under the *CascadeTest* subkey that you created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of type **REG\_SZ**); for example:</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Layout
               Properties
               Select all
```

<span data-ttu-id="f8185-118">Asegúrese de que el valor predeterminado de la subclave *Test Cascade Menu 2* esté vacío y se muestre como **(valor no establecido)**.</span><span class="sxs-lookup"><span data-stu-id="f8185-118">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

### <a name="step-3"></a><span data-ttu-id="f8185-119">Paso 3:</span><span class="sxs-lookup"><span data-stu-id="f8185-119">Step 3:</span></span>

<span data-ttu-id="f8185-120">Rellene los subverbos utilizando cualquiera de las siguientes implementaciones de verbo estático.</span><span class="sxs-lookup"><span data-stu-id="f8185-120">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="f8185-121">Tenga en cuenta que la subclave CommandFlags representa los valores de EXPCMDFLAGS.</span><span class="sxs-lookup"><span data-stu-id="f8185-121">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="f8185-122">Si desea agregar un separador antes o después del elemento de menú en cascada, use ECF \_ SEPARATORBEFORE (0x20) o ECF \_ SEPARATORAFTER (0x40).</span><span class="sxs-lookup"><span data-stu-id="f8185-122">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="f8185-123">Para obtener una descripción de estas marcas de Windows 7 y versiones posteriores, vea [**IExplorerCommand:: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="f8185-123">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="f8185-124">ECF \_ SEPARATORBEFORE solo funciona para los elementos de menú de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="f8185-124">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="f8185-125">MUIVerb es de tipo **reg \_ SZ** y CommandFlags es de tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f8185-125">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Shell
                  cmd1
                     MUIVerb = Notepad
                     command
                        (Default) = %SystemRoot%\system32\notepad.exe %1
                  cmd2
                     MUIVerb = Wordpad
                     CommandFlags = 0x20
                     command
                        (Default) = C:\Program Files\Windows NT\Accessories\wordpad.exe %1
```

## <a name="remarks"></a><span data-ttu-id="f8185-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8185-126">Remarks</span></span>

<span data-ttu-id="f8185-127">La siguiente captura de pantalla es una ilustración de los ejemplos anteriores de entradas de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="f8185-127">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![captura de pantalla que muestra un ejemplo de un menú en cascada con opciones de Bloc de notas y WordPad](images/file-assoc/testcascademenu2.png)

 

 



