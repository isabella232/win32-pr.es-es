---
description: Puede localizar propiedades estáticas mediante el uso de mapas de valores parciales.
ms.assetid: 67e91454-c065-4ab2-a373-245c9392c71c
ms.tgt_platform: multiple
title: Localizar propiedades estáticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecaba200b7880991d349c6e0c0196c88ffa54b11
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104362832"
---
# <a name="localizing-static-properties"></a><span data-ttu-id="3f134-103">Localizar propiedades estáticas</span><span class="sxs-lookup"><span data-stu-id="3f134-103">Localizing Static Properties</span></span>

<span data-ttu-id="3f134-104">Puede localizar propiedades estáticas mediante el uso de mapas de valores parciales.</span><span class="sxs-lookup"><span data-stu-id="3f134-104">You can localize static properties by using partial value maps.</span></span>

<span data-ttu-id="3f134-105">En el procedimiento siguiente se describe cómo se pueden localizar las propiedades estáticas mediante mapas de valores parciales con expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="3f134-105">The following procedure describes how static properties can be localized using partial value maps with regular expressions.</span></span>

<span data-ttu-id="3f134-106">**Para usar asignaciones de valores para localizar propiedades estáticas**</span><span class="sxs-lookup"><span data-stu-id="3f134-106">**To use value maps to localize static properties**</span></span>

1.  <span data-ttu-id="3f134-107">Cree un archivo MOF maestro (Mastervm. mof).</span><span class="sxs-lookup"><span data-stu-id="3f134-107">Create a master MOF file (Mastervm.mof).</span></span>

    <span data-ttu-id="3f134-108">El siguiente ejemplo de código se puede usar para crear un archivo MOF maestro (Mastervm. mof).</span><span class="sxs-lookup"><span data-stu-id="3f134-108">The following code example can be used to create a master MOF file (Mastervm.mof).</span></span>

    ```syntax
    [Locale(0x409)]
    class Group1
    {
        [key] string ID;
        [DisplayName("Numbers"),
            ValueMap{0,1,2,3}:amended,
            Values{"Zero", "One", "Two", "Three"}:amended]
        Uint32 Numbers;
    };
    ```

2.  <span data-ttu-id="3f134-109">Cree las versiones independientes del idioma y específicas del idioma del archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="3f134-109">Create the language-neutral and language-specific versions of the MOF file.</span></span>

    <span data-ttu-id="3f134-110">Escriba el siguiente comando en un símbolo del sistema para crear versiones independientes del idioma y del idioma del archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="3f134-110">Type the following command at a command prompt to create the language-neutral and language-specific versions of the MOF file.</span></span>

    ```syntax
    mofcomp -MOF:LnVm.mof -MFL:LsVm.mfl -Amendment:MS_409 MasterVm.mof
    ```

    <span data-ttu-id="3f134-111">El compilador MOF genera los archivos MOF específicos del idioma y del idioma independiente, LnVm. mof y LsVm. mfl.</span><span class="sxs-lookup"><span data-stu-id="3f134-111">The MOF compiler generates the language-specific and language-neutral MOF files, LnVm.mof and LsVm.mfl.</span></span> <span data-ttu-id="3f134-112">Los valores de Inglés de Estados Unidos de la propiedad [numbers](numbers.md) se colocan en el archivo. MFL para el espacio de nombres American English.</span><span class="sxs-lookup"><span data-stu-id="3f134-112">The American English values for the [Numbers](numbers.md) property is placed in the .mfl file for the American English namespace.</span></span>

    <span data-ttu-id="3f134-113">En el ejemplo de código siguiente se muestra el contenido del archivo LsVm. mfl.</span><span class="sxs-lookup"><span data-stu-id="3f134-113">The following code example shows the contents of the LsVm.mfl file.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_409";};
    #pragma namespace("\\\\.\\root\\default\\ms_409")

    [AMENDMENT, LOCALE(0x409)] 
    class Group1
    {
      [ValueMap{0, 1, 2, 3} : Amended,
          Values{"Zero", "One", "Two", "Three"} : Amended] 
      Uint32 Numbers;
    };
    ```

3.  <span data-ttu-id="3f134-114">Compile los dos archivos MOF y almacene la información de clase en el repositorio CIM.</span><span class="sxs-lookup"><span data-stu-id="3f134-114">Compile the two MOF files and store the class information in the CIM repository.</span></span>

    <span data-ttu-id="3f134-115">Escriba el siguiente comando en un símbolo del sistema para compilar los dos archivos MOF.</span><span class="sxs-lookup"><span data-stu-id="3f134-115">Type the following command at a command prompt to compile the two MOF files.</span></span>

    ```syntax
    Mofcomp LnVm.mof 
    Mofcomp LsVm.mfl
    ```

4.  <span data-ttu-id="3f134-116">Localizar el archivo MFL para otras configuraciones regionales.</span><span class="sxs-lookup"><span data-stu-id="3f134-116">Localize the MFL file for other locales.</span></span>

    <span data-ttu-id="3f134-117">En el ejemplo de código siguiente se muestra el contenido de un archivo MFL para el espacio de nombres francés.</span><span class="sxs-lookup"><span data-stu-id="3f134-117">The following code example shows the contents of an MFL file for the French namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_40C";};
    #pragma namespace("\\\\.\\root\\default\\ms_40C")

    [AMENDMENT, LOCALE(0x40C)] 
    class Group1
    {
        [key] string ID;
        [ValueMap{0, 1, 2, 3} : Amended,
            Values{"Zero", "Un", "Deux", "Trois"} : Amended]
        Uint32 Numbers;
    };
    ```

<span data-ttu-id="3f134-118">El resultado neto es que el nombre para mostrar y el valor de la propiedad [numbers](numbers.md) dependen de la configuración regional del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="3f134-118">The net result is that both the display name and the value of the [Numbers](numbers.md) property depend on the locale of the logged-on user.</span></span> <span data-ttu-id="3f134-119">Si el usuario especifica una configuración regional que no se ha proporcionado, los datos del calificador predeterminado proceden del espacio de nombres inglés (MS \_ 409).</span><span class="sxs-lookup"><span data-stu-id="3f134-119">If the user specifies a locale that has not been provided, the default qualifier data comes from the English (ms\_409) namespace.</span></span>

<span data-ttu-id="3f134-120">La implicación de este diseño es que cada valor de cadena se utiliza como identificador de búsqueda, que no se puede localizar.</span><span class="sxs-lookup"><span data-stu-id="3f134-120">The implication of this design is that each string value is used as a lookup identifier, which cannot be localized.</span></span> <span data-ttu-id="3f134-121">Al definir este esquema, debe asegurarse de que el valor que el proveedor coloca es independiente de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="3f134-121">When defining this scheme, you must ensure that the value the provider puts in is locale-independent.</span></span>

> [!Note]  
> <span data-ttu-id="3f134-122">WMI no proporciona actualmente compatibilidad en tiempo de ejecución para asignar valores a cadenas definidas por calificadores.</span><span class="sxs-lookup"><span data-stu-id="3f134-122">WMI does not currently provide run-time support for mapping values to strings defined by qualifiers.</span></span> <span data-ttu-id="3f134-123">La interpretación de la sintaxis sugerida es responsabilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f134-123">Interpretation of the suggested syntax is the application's responsibility.</span></span>

 

 

 



