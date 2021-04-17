---
description: Uno de los principales propósitos de obtener acceso a una colección es quitar un elemento de la colección. Puede quitar un elemento de una colección mediante una llamada al método SWbemPropertySet. Remove. Este método no está disponible para SWbemObjectSet o SWbemMethodSet.
ms.assetid: 4a71029c-9fe1-4348-9f78-daa345728e8d
ms.tgt_platform: multiple
title: Quitar un solo elemento de una colección WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dabeb3ff2e7e70cf6fe25f1ddfb0b14032119d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687240"
---
# <a name="removing-a-single-item-from-a-wmi-collection"></a><span data-ttu-id="41d95-105">Quitar un solo elemento de una colección WMI</span><span class="sxs-lookup"><span data-stu-id="41d95-105">Removing a Single Item from a WMI Collection</span></span>

<span data-ttu-id="41d95-106">Uno de los principales propósitos de obtener acceso a una colección es quitar un elemento de la colección.</span><span class="sxs-lookup"><span data-stu-id="41d95-106">One of the main purposes of accessing a collection is to remove an item from the collection.</span></span> <span data-ttu-id="41d95-107">Puede quitar un elemento de una colección mediante una llamada al método [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="41d95-107">You can remove an item from a collection with a call to the [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) method.</span></span> <span data-ttu-id="41d95-108">Este método no está disponible para [**SWbemObjectSet**](swbemobjectset.md) o [**SWbemMethodSet**](swbemmethodset.md).</span><span class="sxs-lookup"><span data-stu-id="41d95-108">This method is not available for [**SWbemObjectSet**](swbemobjectset.md) or [**SWbemMethodSet**](swbemmethodset.md).</span></span>

<span data-ttu-id="41d95-109">Los elementos se quitan por nombre en [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md)y [**SWbemNamedValueSet**](swbemnamedvalueset.md).</span><span class="sxs-lookup"><span data-stu-id="41d95-109">Items are removed by name from [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md), and [**SWbemNamedValueSet**](swbemnamedvalueset.md).</span></span> <span data-ttu-id="41d95-110">Sin embargo, los elementos de [**SWbemRefresher**](swbemrefresher.md) se quitan por índice y desde [**SWbemPrivilegeSet**](swbemprivilegeset.md) por la constante que representa el nombre del privilegio.</span><span class="sxs-lookup"><span data-stu-id="41d95-110">However, items in [**SWbemRefresher**](swbemrefresher.md) are removed by index and from [**SWbemPrivilegeSet**](swbemprivilegeset.md) by the constant that represents the privilege name.</span></span>

<span data-ttu-id="41d95-111">**Para quitar un elemento de una colección**</span><span class="sxs-lookup"><span data-stu-id="41d95-111">**To remove an item from a collection**</span></span>

-   <span data-ttu-id="41d95-112">En el ejemplo de código siguiente se muestra cómo quitar el elemento con una llamada al método [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="41d95-112">The following code example shows how to remove the item with a call to the [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) method.</span></span>

    ```VB
    oclass.Properties_.Remove "Prop2"
    ```

    

    <span data-ttu-id="41d95-113">En el ejemplo siguiente se crea una nueva clase denominada "NewClass" en el \\ espacio de nombres predeterminado raíz y se le agregan tres propiedades.</span><span class="sxs-lookup"><span data-stu-id="41d95-113">The following example creates a new class named "NewClass" in the root\\default namespace and adds three properties to it.</span></span> <span data-ttu-id="41d95-114">Después, el script utiliza el código del ejemplo anterior para eliminar la segunda propiedad.</span><span class="sxs-lookup"><span data-stu-id="41d95-114">The script then uses the code from the previous example to delete the second property.</span></span>

    ```VB
    ' Obtain an empty class and name it
    Const WBEM_CIMTYPE_STRING = 8
    Set objSWbemService = GetObject("winmgmts:root\default")
    Set objClass = objSWbemService.get()
    Wscript.Echo "Creating class NewClass"
    objClass.Path_.Class = "NewClass"

    ' Add three properties 
    For i = 1 to 3
        objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
    Next
    Getprops()

    ' Remove the Prop2 property
    objClass.Properties_.Remove "Prop2"
    Wscript.Echo "Second property removed "
    Getprops()

    ' Write the changes to the class back
    objClass.Put_

    Sub Getprops()
        Wscript.Echo "Number of Properties = " _
            & objClass.Properties_.Count
        For Each prop in objClass.Properties_
            Wscript.Echo prop.name
        Next
    End Sub
    ```

    

<span data-ttu-id="41d95-115">Para obtener más información, vea [manipular información de clase e instancia](manipulating-class-and-instance-information.md), [obtener acceso a una colección](accessing-a-collection.md)y [quitar varios elementos de una colección](removing-multiple-items-from-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="41d95-115">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Accessing a Collection](accessing-a-collection.md), and [Removing Multiple Items from a Collection](removing-multiple-items-from-a-collection.md).</span></span>

 

 



