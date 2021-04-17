---
description: Obtener acceso a un valor del registro sin nombre
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: Obtener acceso a un valor del registro sin nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92860d240598f0353d1f4c9f41a77306942d272b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707101"
---
# <a name="accessing-an-unnamed-registry-value"></a><span data-ttu-id="6b805-103">Obtener acceso a un valor del registro sin nombre</span><span class="sxs-lookup"><span data-stu-id="6b805-103">Accessing an Unnamed Registry Value</span></span>

<span data-ttu-id="6b805-104">El valor predeterminado o sin nombre de una clave del registro se muestra como (valor predeterminado) o <No Name> en el editor del registro de regedit.</span><span class="sxs-lookup"><span data-stu-id="6b805-104">The default, or unnamed value of a registry key is shown as (Default) or <No Name> in the Regedit registry editor.</span></span> <span data-ttu-id="6b805-105">Puede utilizar el proveedor del registro del sistema para tener acceso a una clave del registro sin nombre.</span><span class="sxs-lookup"><span data-stu-id="6b805-105">You can use the System Registry provider to access an unnamed registry key.</span></span> <span data-ttu-id="6b805-106">Del mismo modo, también puede utilizar el proveedor del registro del sistema para obtener acceso a las descripciones de mapas de bits, que se definen como valores sin nombre.</span><span class="sxs-lookup"><span data-stu-id="6b805-106">Similarly, you can also use the System Registry provider to access bitmap descriptions, which are defined as unnamed values.</span></span>

<span data-ttu-id="6b805-107">En el procedimiento siguiente se describe cómo recuperar un valor del registro sin nombre.</span><span class="sxs-lookup"><span data-stu-id="6b805-107">The following procedure describes how to retrieve an unnamed registry value.</span></span>

<span data-ttu-id="6b805-108">**Para recuperar un valor del registro sin nombre**</span><span class="sxs-lookup"><span data-stu-id="6b805-108">**To retrieve an unnamed registry value**</span></span>

1.  <span data-ttu-id="6b805-109">Defina una propiedad y establezca el calificador **PropertyContext** de esa propiedad en una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="6b805-109">Define a property and set the **PropertyContext** qualifier of that property to an empty string.</span></span>

    <span data-ttu-id="6b805-110">En el ejemplo de código siguiente se muestra cómo la clase define las propiedades para contener los valores de la clave especificada por el calificador **ClassContext** .</span><span class="sxs-lookup"><span data-stu-id="6b805-110">The following code example shows how the class defines properties to hold values for the key specified by the **ClassContext** qualifier.</span></span> <span data-ttu-id="6b805-111">El valor predeterminado se almacena en la propiedad **predeterminada** .</span><span class="sxs-lookup"><span data-stu-id="6b805-111">The default value is stored in the **Default** property.</span></span>

    ``` syntax
    [dynamic, 
     provider("RegProv"), 
     ClassContext("local|hkey_local_machine\\software\\"
     "microsoft\\Active Setup\\Installed Components")]

    class RegTrans{
      [key] String Transports="";
      [PropertyContext("")] String Default;
      [PropertyContext("ComponentId")] String ComponentID;
      [PropertyContext("Locale")] String Locale;
    };
    ```

    <span data-ttu-id="6b805-112">La clave de transportes no utiliza el valor sin nombre, por lo que la compilación de este archivo MOF no genera ningún valor para la propiedad **predeterminada** a menos que se use una herramienta de edición del registro para cambiar el valor sin nombre.</span><span class="sxs-lookup"><span data-stu-id="6b805-112">The Transports key does not use the unnamed value, so compilation of this MOF file does not produce any value for the **Default** property unless a registry editing tool is used to change the unnamed value.</span></span>

2.  <span data-ttu-id="6b805-113">Para un archivo de mapa de bits, defina una propiedad y establezca el valor de **PropertyContext** de esa propiedad.</span><span class="sxs-lookup"><span data-stu-id="6b805-113">For a bitmap file, define a property and set the **PropertyContext** of that property.</span></span>

    <span data-ttu-id="6b805-114">En el ejemplo de código siguiente se muestra cómo definir una propiedad.</span><span class="sxs-lookup"><span data-stu-id="6b805-114">The following code example shows how to define a property.</span></span>

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 



