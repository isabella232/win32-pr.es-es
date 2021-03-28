---
description: Además del registro de modelo de objetos componentes (COM) normal, se deben completar los pasos siguientes para poder registrar controladores de superposición de iconos.
ms.assetid: 73EE5E69-969B-409E-9E8F-5837720EA0B3
title: Cómo registrar controladores de superposición de iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb58747adc9b754481f43fec825a4588e1606ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997696"
---
# <a name="how-to-register-icon-overlay-handlers"></a><span data-ttu-id="f157a-103">Cómo registrar controladores de superposición de iconos</span><span class="sxs-lookup"><span data-stu-id="f157a-103">How to Register Icon Overlay Handlers</span></span>

<span data-ttu-id="f157a-104">Además del registro de modelo de objetos componentes (COM) normal, se deben completar los pasos siguientes para poder registrar controladores de superposición de iconos.</span><span class="sxs-lookup"><span data-stu-id="f157a-104">In addition to normal Component Object Model (COM) registration, the following steps must be completed in order to register icon overlay handlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="f157a-105">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="f157a-105">Instructions</span></span>

### <a name="step-1-create-a-subkey-named-for-the-handler-under-this-key"></a><span data-ttu-id="f157a-106">Paso 1: crear una subclave denominada para el controlador en esta clave</span><span class="sxs-lookup"><span data-stu-id="f157a-106">Step 1: Create a subkey named for the handler under this key</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
```

### <a name="step-2-set-the-default-value-of-the-subkey-to-the-string-form-of-the-objects-class-identifier-clsidguid"></a><span data-ttu-id="f157a-107">Paso 2: establecer el valor predeterminado de la subclave en la forma de cadena del GUID del identificador de clase (CLSID) del objeto</span><span class="sxs-lookup"><span data-stu-id="f157a-107">Step 2: Set the default value of the subkey to the string form of the object's class identifier (CLSID)GUID</span></span>

<span data-ttu-id="f157a-108">En el ejemplo siguiente se muestra cómo registrar un controlador de superposición de iconos denominado superoverlay.</span><span class="sxs-lookup"><span data-stu-id="f157a-108">The following example illustrates how to register an icon overlay handler named MyOverlay.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
                     MyOverlay
                        (Default) = {MyOverlay CLSID GUID}
```

 

 



