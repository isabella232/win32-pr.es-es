---
description: Definir atributos de tipo de archivo en el registro.
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: Cómo definir atributos de tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7844c65191d6513a06625a28c47accd3df5cc82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909549"
---
# <a name="how-to-define-file-type-attributes"></a><span data-ttu-id="8e907-103">Cómo definir atributos de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="8e907-103">How to Define File Type Attributes</span></span>

<span data-ttu-id="8e907-104">La asignación de atributos de tipo de archivo a un ProgID asociado permite controlar algunos aspectos del comportamiento del tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="8e907-104">Assigning file type attributes to an associated ProgID enables you to control some aspects of the file type's behavior.</span></span> <span data-ttu-id="8e907-105">Antes de Windows Vista, estos atributos podían permitirle limitar el grado en el que el usuario podía usar la pestaña de propiedades de **Opciones de carpeta** para modificar diversos aspectos del tipo de archivo, como su icono o verbos.</span><span class="sxs-lookup"><span data-stu-id="8e907-105">Prior to Windows Vista, these attributes could enable you to limit the extent to which the user could use the **Folder Options** property tab to modify various aspects of the file type, such as its icon or verbs.</span></span>

<span data-ttu-id="8e907-106">Los atributos de tipo de archivo son marcas binarias especificadas como valores **reg \_ DWORD** o **reg \_ Binary** en la subclave ProgID asociada del tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="8e907-106">File type attributes are binary flags specified as **REG\_DWORD** or **REG\_BINARY** values in the file type's associated ProgID subkey.</span></span>

<span data-ttu-id="8e907-107">Para asignar atributos para un tipo de archivo, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="8e907-107">To assign attributes for a file type, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="8e907-108">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="8e907-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="8e907-109">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="8e907-109">Step 1:</span></span>

<span data-ttu-id="8e907-110">Agregue una entrada marcas a la subclave ProgID asociada del tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="8e907-110">Add an EditFlags entry to the file type's associated ProgID subkey.</span></span>

### <a name="step-2"></a><span data-ttu-id="8e907-111">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="8e907-111">Step 2:</span></span>

<span data-ttu-id="8e907-112">Establezca la entrada en el valor de atributo adecuado.</span><span class="sxs-lookup"><span data-stu-id="8e907-112">Set the entry to the appropriate attribute value.</span></span>

<span data-ttu-id="8e907-113">En el ejemplo siguiente se muestran los \_ atributos FTA noremove (0x00000010) y FTA \_ NoNewVerb (0x00000020) establecidos para el tipo de archivo. MYP.</span><span class="sxs-lookup"><span data-stu-id="8e907-113">The following example shows the FTA\_NoRemove (0x00000010) and FTA\_NoNewVerb (0x00000020) attributes set for the .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
      EditFlags = 0x00000030
```

## <a name="remarks"></a><span data-ttu-id="8e907-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e907-114">Remarks</span></span>

<span data-ttu-id="8e907-115">Las marcas se pueden combinar con un operador lógico OR para formar el valor de atributo único.</span><span class="sxs-lookup"><span data-stu-id="8e907-115">The flags can be combined with a logical OR to form the single attribute value.</span></span>

<span data-ttu-id="8e907-116">Para obtener una lista de los posibles atributos de tipo de archivo y sus valores hexadecimales, y más detalles sobre cómo recuperar y establecer estos valores mediante programación, vea [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).</span><span class="sxs-lookup"><span data-stu-id="8e907-116">For a list of possible file type attributes and their hexadecimal values, and more details on programmatically retrieving and setting these values, see [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).</span></span>

 

 



