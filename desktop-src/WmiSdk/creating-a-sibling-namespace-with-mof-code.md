---
description: Otra forma de crear un espacio de nombres es usar el código Managed Object Format (MOF) para crear un espacio de nombres relacionado. Un espacio de nombres relacionado es un espacio de nombres que no existe como elemento secundario del espacio de nombres actual.
ms.assetid: 1a3f8569-e725-4158-9a2b-b440b9247925
ms.tgt_platform: multiple
title: Crear un espacio de nombres relacionado con código MOF
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4fcbf6e16ad51ab9a0df63e3497735b07cd6afc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653009"
---
# <a name="creating-a-sibling-namespace-with-mof-code"></a><span data-ttu-id="e864b-104">Crear un espacio de nombres relacionado con código MOF</span><span class="sxs-lookup"><span data-stu-id="e864b-104">Creating a Sibling Namespace with MOF Code</span></span>

<span data-ttu-id="e864b-105">Otra forma de crear un espacio de nombres es usar el código Managed Object Format (MOF) para crear un espacio de nombres relacionado.</span><span class="sxs-lookup"><span data-stu-id="e864b-105">Another way of creating a namespace is to use Managed Object Format (MOF) code to create a sibling namespace.</span></span> <span data-ttu-id="e864b-106">Un espacio de nombres relacionado es un espacio de nombres que no existe como elemento secundario del espacio de nombres actual.</span><span class="sxs-lookup"><span data-stu-id="e864b-106">A sibling namespace is a namespace that does not exist as a child of the current namespace.</span></span>

<span data-ttu-id="e864b-107">En el procedimiento siguiente se describe cómo crear un espacio de nombres relacionado con código MOF.</span><span class="sxs-lookup"><span data-stu-id="e864b-107">The following procedure describes how to create a sibling namespace with MOF code.</span></span>

<span data-ttu-id="e864b-108">**Para crear un espacio de nombres relacionado con código MOF**</span><span class="sxs-lookup"><span data-stu-id="e864b-108">**To create a sibling namespace with MOF code**</span></span>

1.  <span data-ttu-id="e864b-109">Inserte el comando [**\# pragma namespace**](pragma-namespace.md) en el código MOF antes de la declaración de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="e864b-109">Insert the [**\#pragma namespace**](pragma-namespace.md) command into your MOF code prior to the namespace declaration.</span></span>

    <span data-ttu-id="e864b-110">El comando [**\# pragma namespace**](pragma-namespace.md) indica a WMI dónde debe crear las instancias que siguen a la Directiva.</span><span class="sxs-lookup"><span data-stu-id="e864b-110">The [**\#pragma namespace**](pragma-namespace.md) command instructs WMI where to create the instances following the directive.</span></span>

2.  <span data-ttu-id="e864b-111">Cree una instancia de la clase [**\_ \_ namespace**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="e864b-111">Create an instance of the [**\_\_Namespace**](--namespace.md) class.</span></span>
3.  <span data-ttu-id="e864b-112">Compile el código con la utilidad [MOFCOMP](mofcomp.md) o la interfaz [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="e864b-112">Compile your code with the [mofcomp](mofcomp.md) utility or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="e864b-113">Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="e864b-113">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="e864b-114">En el siguiente ejemplo de código MOF se describe cómo crear un espacio de nombres como un elemento relacionado con el espacio de nombres "root \\ CIMv2".</span><span class="sxs-lookup"><span data-stu-id="e864b-114">The following MOF code example describes how to create a namespace as a sibling to the "Root\\CIMv2" namespace.</span></span>

``` syntax
#pragma namespace("\\\\.\\Root")

instance of __Namespace 
{
    Name = "MyNamespace";
};
```

 

 



