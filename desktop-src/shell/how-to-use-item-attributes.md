---
description: Los valores de marca SFGAO de los atributos de Shell para un elemento pueden probarse para determinar si el verbo debe estar habilitado o deshabilitado.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Cómo usar atributos de elemento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a438c81258677822ca9b940eb9f74366d6226ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909530"
---
# <a name="how-to-use-item-attributes"></a><span data-ttu-id="b8e5d-103">Cómo usar atributos de elemento</span><span class="sxs-lookup"><span data-stu-id="b8e5d-103">How to Use Item Attributes</span></span>

<span data-ttu-id="b8e5d-104">Los valores de marca [**SFGAO**](sfgao.md) de los atributos de Shell para un elemento pueden probarse para determinar si el verbo debe estar habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b8e5d-104">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="b8e5d-105">Para usar esta característica de atributo, agregue los siguientes valores de **reg \_ DWORD** en el verbo:</span><span class="sxs-lookup"><span data-stu-id="b8e5d-105">To use this attribute feature, add the following **REG\_DWORD** values under the verb:</span></span>

## <a name="instructions"></a><span data-ttu-id="b8e5d-106">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="b8e5d-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="b8e5d-107">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="b8e5d-107">Step 1:</span></span>

<span data-ttu-id="b8e5d-108">El valor AttributeMask especifica el valor de [**SFGAO**](sfgao.md) de los valores de bit de la máscara que se va a probar con.</span><span class="sxs-lookup"><span data-stu-id="b8e5d-108">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>

### <a name="step-2"></a><span data-ttu-id="b8e5d-109">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="b8e5d-109">Step 2:</span></span>

<span data-ttu-id="b8e5d-110">El valor AttributeValue especifica el valor de [**SFGAO**](sfgao.md) de los bits que se prueban.</span><span class="sxs-lookup"><span data-stu-id="b8e5d-110">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>

### <a name="step-3"></a><span data-ttu-id="b8e5d-111">Paso 3:</span><span class="sxs-lookup"><span data-stu-id="b8e5d-111">Step 3:</span></span>

<span data-ttu-id="b8e5d-112">ImpliedSelectionModel especifica cero para los verbos de elemento o un valor distinto de cero para los verbos en el menú contextual del fondo.</span><span class="sxs-lookup"><span data-stu-id="b8e5d-112">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8e5d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8e5d-113">Remarks</span></span>

<span data-ttu-id="b8e5d-114">En la siguiente entrada del registro de ejemplo, AttributeMask se establece en [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).</span><span class="sxs-lookup"><span data-stu-id="b8e5d-114">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

 

 



