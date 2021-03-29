---
title: Enumerar objetos
description: Para ver el objeto secundario de un contenedor, como una unidad organizativa (OU), enumere el objeto contenedor.
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- Enumerar objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26b78f084f95ac59c909b326be10d42c4a6696a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903062"
---
# <a name="enumerating-objects"></a><span data-ttu-id="d944d-104">Enumerar objetos</span><span class="sxs-lookup"><span data-stu-id="d944d-104">Enumerating Objects</span></span>

<span data-ttu-id="d944d-105">Para ver el objeto secundario de un contenedor, como una unidad organizativa (OU), enumere el objeto contenedor.</span><span class="sxs-lookup"><span data-stu-id="d944d-105">To view the child object of a container, such as an organizational unit (OU), enumerate the container object.</span></span> <span data-ttu-id="d944d-106">Para crear una analogía con un sistema de archivos, el objeto secundario se corresponderá con los archivos del directorio, mientras que el contenedor, que es el objeto primario, se corresponderá con el propio directorio.</span><span class="sxs-lookup"><span data-stu-id="d944d-106">To make an analogy to a file system, the child object would correspond to files in the directory, while the container, which is the parent object, would correspond to the directory itself.</span></span> <span data-ttu-id="d944d-107">También puede usar la operación enumerar cuando desee obtener el objeto primario de un objeto.</span><span class="sxs-lookup"><span data-stu-id="d944d-107">You may also use the enumerate operation when you want to get the parent object of an object.</span></span>

<span data-ttu-id="d944d-108">Al enumerar un objeto, realmente se enlaza a un objeto en el directorio y se devuelve una interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) en cada objeto.</span><span class="sxs-lookup"><span data-stu-id="d944d-108">When you enumerate an object, you actually bind to an object in the directory, and an [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface is returned on each object.</span></span>

<span data-ttu-id="d944d-109">En el ejemplo de código siguiente se muestra cómo enumerar los elementos secundarios de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="d944d-109">The following code example shows how to enumerate the children of a container.</span></span>


```VB
Dim ou As IADs
' Bind to an object using its DN.
On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")

For each child in ou
    Debug.Print child.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
```



<span data-ttu-id="d944d-110">Puede filtrar los tipos de objetos devueltos por la enumeración.</span><span class="sxs-lookup"><span data-stu-id="d944d-110">You can filter the types of objects returned from the enumeration.</span></span> <span data-ttu-id="d944d-111">Por ejemplo, para mostrar solo usuarios y grupos, use el siguiente ejemplo de código antes de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="d944d-111">For example, to display only users and groups, use the following code example before the enumeration.</span></span>


```VB
Ou.Filter = Array("user", "group")
```



<span data-ttu-id="d944d-112">Si tiene una referencia de objeto, puede obtener el elemento primario del objeto mediante la propiedad [**primaria**](iads-property-methods.md) [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="d944d-112">If you have an object reference, you can get the object's parent using the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) [**Parent**](iads-property-methods.md) property.</span></span> <span data-ttu-id="d944d-113">En el ejemplo de código siguiente se muestra cómo enlazar al objeto primario.</span><span class="sxs-lookup"><span data-stu-id="d944d-113">The following code example shows how to bind to the parent object.</span></span>


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



<span data-ttu-id="d944d-114">Para obtener más información, consulte [enumeración de objetos ADSI](enumerating-adsi-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d944d-114">For more information, see [Enumerating ADSI Objects](enumerating-adsi-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d944d-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d944d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d944d-116">Buscar objetos</span><span class="sxs-lookup"><span data-stu-id="d944d-116">Searching for Objects</span></span>](searching-for-objects.md)
</dt> </dl>

 

 




