---
description: Indica al compilador MOF que separe un archivo MOF en versiones independientes del lenguaje y específicas del idioma.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: modificación de pragma
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1269ac1a96617b72852e687b2a38ce8d331ab3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811425"
---
# <a name="pragma-amendment"></a><span data-ttu-id="5cce4-103">modificación de pragma</span><span class="sxs-lookup"><span data-stu-id="5cce4-103">pragma amendment</span></span>

<span data-ttu-id="5cce4-104">El comando de preprocesador de **modificación de pragma** indica al compilador de MOF que separe un archivo MOF en versiones independientes del idioma y del idioma.</span><span class="sxs-lookup"><span data-stu-id="5cce4-104">The **pragma amendment** preprocessor command directs the MOF compiler to separate a MOF file into language-neutral and language-specific versions.</span></span> <span data-ttu-id="5cce4-105">El archivo MOF específico del idioma mueve los calificadores modificados a un espacio de nombres para una configuración regional específica.</span><span class="sxs-lookup"><span data-stu-id="5cce4-105">The language-specific MOF file moves amended qualifiers to a namespace for a specific locale.</span></span> <span data-ttu-id="5cce4-106">Después, debe compilar los archivos MOF específicos del idioma y del idioma independiente para almacenar la información de clase en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="5cce4-106">You then compile the language-specific and language-neutral MOF files to store class information in the WMI repository.</span></span>

## <a name="examples"></a><span data-ttu-id="5cce4-107">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5cce4-107">Examples</span></span>

<span data-ttu-id="5cce4-108">En el ejemplo siguiente se muestra cómo crear un archivo MOF que contenga calificadores modificados.</span><span class="sxs-lookup"><span data-stu-id="5cce4-108">The following example shows how to create a MOF file that contains amended qualifiers.</span></span> <span data-ttu-id="5cce4-109">Después, puede compilar el código MOF con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="5cce4-109">You can then compile the MOF code with the following command:</span></span>

<span data-ttu-id="5cce4-110">**MOFCOMP** **-MOF: Lnmof. mof** **-MFL: Lsmof. MFL** **Mastermof. mof**</span><span class="sxs-lookup"><span data-stu-id="5cce4-110">**mofcomp** **-MOF:Lnmof.mof** **-MFL:Lsmof.mfl** **Mastermof.mof**</span></span>

<span data-ttu-id="5cce4-111">El comando indica al compilador MOF que genere dos archivos MOF del archivo Mastermof. mof original.</span><span class="sxs-lookup"><span data-stu-id="5cce4-111">The command instructs the MOF compiler to produce two MOF files from the original Mastermof.mof file.</span></span> <span data-ttu-id="5cce4-112">El compilador MOF genera una versión independiente del lenguaje del archivo MOF, denominada Lnmof. mof, con todos los elementos específicos del idioma que se han quitado.</span><span class="sxs-lookup"><span data-stu-id="5cce4-112">The MOF compiler produces a language-neutral version of the MOF file, called Lnmof.mof, with all language-specific items removed.</span></span> <span data-ttu-id="5cce4-113">El compilador también crea un segundo archivo MOF específico del lenguaje denominado Lsmof. MFL que contiene solo los elementos que se deben localizar.</span><span class="sxs-lookup"><span data-stu-id="5cce4-113">The compiler also creates a second, language-specific MOF file called Lsmof.mfl that contains only items that you must localize.</span></span>

> [!Note]  
> <span data-ttu-id="5cce4-114">Cuando divida un archivo MOF con el calificador de **modificación** o el comando **pragma de modificación** , debe especificar las opciones **-MOF** y **-MFL** .</span><span class="sxs-lookup"><span data-stu-id="5cce4-114">When you are splitting a MOF file with the **amendment** qualifier or the **pragma amendment** command, you must specify the **-MOF** and **-MFL** options.</span></span> <span data-ttu-id="5cce4-115">De lo contrario, el compilador no genera ningún archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="5cce4-115">Otherwise, the compiler does not generate any output files.</span></span> <span data-ttu-id="5cce4-116">A continuación, debe compilar los dos archivos de salida para que la información de la clase esté disponible en WMI.</span><span class="sxs-lookup"><span data-stu-id="5cce4-116">You must then compile the two output files to make the class information available to WMI.</span></span>

 


```mof
#pragma amendment ("MS_409")

[Description("Localized version of MyClass" for American English") :
    Amended, LOCALE(0x409)] 

Class myclass
{
     [DisplayName("User Name") : Amended,
     Description("The Name property contains the name of the user") : 
     Amended, key]
    string Name;

    uint64 Value; // non-localized value field

     [DisplayName("Time Stamp") : Amended,
     Description("This property shows when the object was created") : 
     Amended] 
    uint64 Timestamp;
};
```



## <a name="requirements"></a><span data-ttu-id="5cce4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cce4-117">Requirements</span></span>



| <span data-ttu-id="5cce4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cce4-118">Requirement</span></span> | <span data-ttu-id="5cce4-119">Value</span><span class="sxs-lookup"><span data-stu-id="5cce4-119">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5cce4-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5cce4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5cce4-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5cce4-121">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5cce4-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5cce4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5cce4-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5cce4-123">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cce4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5cce4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cce4-125">Comandos de preprocesador</span><span class="sxs-lookup"><span data-stu-id="5cce4-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




