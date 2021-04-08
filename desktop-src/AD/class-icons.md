---
title: Iconos de clase
description: El icono que se usa para representar un objeto de clase se puede especificar en el atributo iconPath del contenedor DisplaySpecifiers.
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- nombres para mostrar de clase AD, iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691d4ef22babeded12ec9b951f92247df99521b6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995102"
---
# <a name="class-icons"></a><span data-ttu-id="b9816-104">Iconos de clase</span><span class="sxs-lookup"><span data-stu-id="b9816-104">Class Icons</span></span>

<span data-ttu-id="b9816-105">El icono que se usa para representar un objeto de clase se puede especificar en el atributo **iconPath** del contenedor DisplaySpecifiers.</span><span class="sxs-lookup"><span data-stu-id="b9816-105">The icon used to represent a class object can be specified in the **iconPath** attribute in the DisplaySpecifiers container.</span></span> <span data-ttu-id="b9816-106">Además, cada clase puede almacenar varios Estados de icono.</span><span class="sxs-lookup"><span data-stu-id="b9816-106">Moreover, each class can store multiple icon states.</span></span> <span data-ttu-id="b9816-107">Por ejemplo, una clase de carpeta puede tener iconos para los Estados abierto, cerrado y deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b9816-107">For example, a folder class can have icons for the open, closed, and disabled states.</span></span> <span data-ttu-id="b9816-108">La implementación actual acepta un máximo de dieciséis Estados de icono diferentes por clase.</span><span class="sxs-lookup"><span data-stu-id="b9816-108">The current implementation accepts a maximum of sixteen different icon states per class.</span></span>

<span data-ttu-id="b9816-109">El atributo **iconPath** se puede especificar de una de estas dos maneras.</span><span class="sxs-lookup"><span data-stu-id="b9816-109">The **iconPath** attribute can be specified in one of two ways.</span></span>


```C++
<state>,<icon file name>
```



<span data-ttu-id="b9816-110">or</span><span class="sxs-lookup"><span data-stu-id="b9816-110">or</span></span>


```C++
<state>,<module file name>,<resource ID>
```



<span data-ttu-id="b9816-111">En estos ejemplos, el " &lt; estado &gt; " es un entero con un valor comprendido entre 0 y 15.</span><span class="sxs-lookup"><span data-stu-id="b9816-111">In these examples, the "&lt;state&gt;" is an integer with a value between 0 and 15.</span></span> <span data-ttu-id="b9816-112">El valor 0 se define como el estado predeterminado o cerrado del icono.</span><span class="sxs-lookup"><span data-stu-id="b9816-112">The value 0 is defined to be the default or closed state of the icon.</span></span> <span data-ttu-id="b9816-113">El valor 1 se define como el estado abierto del icono.</span><span class="sxs-lookup"><span data-stu-id="b9816-113">The value 1 is defined to be the open state of the icon.</span></span> <span data-ttu-id="b9816-114">El valor 2 es el Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b9816-114">The value 2 is the disabled state.</span></span> <span data-ttu-id="b9816-115">Todos los demás valores están definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b9816-115">All other values are application-defined.</span></span>

<span data-ttu-id="b9816-116">El " &lt; nombre de archivo &gt; de icono" es la ruta de acceso y el nombre de un archivo de icono que contiene la imagen del icono.</span><span class="sxs-lookup"><span data-stu-id="b9816-116">The "&lt;icon file name&gt;" is the path and file name of an icon file that contains the icon image.</span></span>

<span data-ttu-id="b9816-117">El " &lt; nombre de archivo &gt; de módulo" es la ruta de acceso y el nombre de un módulo, como un archivo exe o dll, que contiene la imagen de icono en un recurso.</span><span class="sxs-lookup"><span data-stu-id="b9816-117">The "&lt;module file name&gt;" is the path and file name of a module, such as an EXE or DLL, that contains the icon image in a resource.</span></span> <span data-ttu-id="b9816-118">El " &lt; identificador &gt; de recurso" es un entero que especifica el identificador de recurso del recurso de icono dentro del módulo.</span><span class="sxs-lookup"><span data-stu-id="b9816-118">The "&lt;resource ID&gt;" is an integer that specifies the resource identifier of the icon resource within the module.</span></span>

## <a name="adding-a-value-to-the-iconpath-attribute"></a><span data-ttu-id="b9816-119">Agregar un valor al atributo **iconPath**</span><span class="sxs-lookup"><span data-stu-id="b9816-119">Adding a Value to the **iconPath** Attribute</span></span>

<span data-ttu-id="b9816-120">Para agregar un valor al atributo **iconPath** , realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="b9816-120">To add a value to the **iconPath** attribute, perform the following steps.</span></span>

1.  <span data-ttu-id="b9816-121">Determine si el valor del atributo existe.</span><span class="sxs-lookup"><span data-stu-id="b9816-121">Determine if the value for the attribute exists.</span></span> <span data-ttu-id="b9816-122">Si un valor se va a reemplazar, elimine primero el valor existente mediante el método [**IADs::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) con el parámetro *LnControlCode* establecido en **ADS \_ Property \_ Delete** y el parámetro *vProp* establecido en el valor que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="b9816-122">If a value is to be replaced, first, delete the existing value using the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_DELETE** and the *vProp* parameter set to the value to be removed.</span></span> <span data-ttu-id="b9816-123">No use la **\_ propiedad ADS \_ Clear** o la actualización de la **\_ propiedad \_ ADS** para *lnControlCode*.</span><span class="sxs-lookup"><span data-stu-id="b9816-123">Do not use **ADS\_PROPERTY\_CLEAR** or **ADS\_PROPERTY\_UPDATE** for *lnControlCode*.</span></span>
2.  <span data-ttu-id="b9816-124">Cree la cadena que representa los datos del icono de atributo.</span><span class="sxs-lookup"><span data-stu-id="b9816-124">Create the string that represents the attribute icon data.</span></span> <span data-ttu-id="b9816-125">Para obtener un ejemplo, vea el formato anterior.</span><span class="sxs-lookup"><span data-stu-id="b9816-125">For an example, see the format above.</span></span>
3.  <span data-ttu-id="b9816-126">Para agregar el nuevo valor, use el método [**IADs::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) con el parámetro *lnControlCode* establecido en la **propiedad de ADS \_ \_ Append**.</span><span class="sxs-lookup"><span data-stu-id="b9816-126">To add the new value, use the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_APPEND**.</span></span>
4.  <span data-ttu-id="b9816-127">Para confirmar los cambios en el directorio, llame a [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="b9816-127">To commit changes to the directory, call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 