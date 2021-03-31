---
description: La forma más sencilla de crear un espacio de nombres es usar el código Managed Object Format (MOF) para crear el espacio de nombres dentro del directorio actual. El directorio actual se define al iniciar sesión.
ms.assetid: 2b83cd96-079f-4178-9e5a-68ede3a92066
ms.tgt_platform: multiple
title: Crear un espacio de nombres secundario con código MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f80aa04e2ef4f5c7bbfc43d9020727b3b2a6e0d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104083594"
---
# <a name="creating-a-child-namespace-with-mof-code"></a><span data-ttu-id="2a790-104">Crear un espacio de nombres secundario con código MOF</span><span class="sxs-lookup"><span data-stu-id="2a790-104">Creating a Child Namespace with MOF Code</span></span>

<span data-ttu-id="2a790-105">La forma más sencilla de crear un espacio de nombres es usar el código Managed Object Format (MOF) para crear el espacio de nombres dentro del directorio actual.</span><span class="sxs-lookup"><span data-stu-id="2a790-105">The simplest way of creating a namespace is to use Managed Object Format (MOF) code to create the namespace inside the current directory.</span></span> <span data-ttu-id="2a790-106">El directorio actual se define al iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="2a790-106">The current directory is defined when you log on.</span></span>

<span data-ttu-id="2a790-107">En el procedimiento siguiente se describe cómo crear un espacio de nombres secundario mediante código MOF.</span><span class="sxs-lookup"><span data-stu-id="2a790-107">The following procedure describes how to create a child namespace using MOF code.</span></span>

<span data-ttu-id="2a790-108">**Para crear un espacio de nombres secundario mediante código MOF**</span><span class="sxs-lookup"><span data-stu-id="2a790-108">**To create a child namespace using MOF code**</span></span>

1.  <span data-ttu-id="2a790-109">Cree una instancia de la clase [**\_ \_ namespace**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="2a790-109">Create an instance of the [**\_\_Namespace**](--namespace.md) class.</span></span>

    <span data-ttu-id="2a790-110">En el ejemplo de código siguiente se muestra cómo crear un espacio de nombres secundario.</span><span class="sxs-lookup"><span data-stu-id="2a790-110">The following code example shows how to create a child namespace.</span></span>

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
    };
    ```

2.  <span data-ttu-id="2a790-111">Si desea solicitar al usuario que realice una conexión cifrada al espacio de nombres, use el calificador **RequiresEncryption** .</span><span class="sxs-lookup"><span data-stu-id="2a790-111">If you want to require the user to make an encrypted connection to the namespace, use the **RequiresEncryption** qualifier.</span></span> <span data-ttu-id="2a790-112">Para obtener más información, vea [requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="2a790-112">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

    <span data-ttu-id="2a790-113">En el ejemplo de código siguiente se muestra cómo requerir una conexión cifrada.</span><span class="sxs-lookup"><span data-stu-id="2a790-113">The following code example shows how to require an encrypted connection.</span></span>

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
        [RequiresEncryption(TRUE)] 
        instance of __MyNamespace { };
    };
    ```

3.  <span data-ttu-id="2a790-114">Si desea establecer un descriptor de seguridad en el espacio de nombres en lugar de usar la seguridad de espacio de nombres predeterminada, use el calificador **NamespaceSecuritySDDL** .</span><span class="sxs-lookup"><span data-stu-id="2a790-114">If you want to set a security descriptor on the namespace rather than using the default namespace security, use the **NamespaceSecuritySDDL** qualifier.</span></span> <span data-ttu-id="2a790-115">Para obtener más información, vea [establecer la seguridad del espacio de nombres cuando se crea el espacio de nombres](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="2a790-115">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>

    <span data-ttu-id="2a790-116">En el ejemplo de código siguiente se muestra cómo establecer un descriptor de seguridad en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="2a790-116">The following code example shows how to set a security descriptor on the namespace.</span></span>

    ``` syntax
    #pragma namespace("\\\\.\\root\\MyNamespace")

    [NamespaceSecuritySDDL ("O:AUG:AUD:(A;CI;0x00060033;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

4.  <span data-ttu-id="2a790-117">Compile y cargue la instancia de [**\_ \_ espacio de nombres**](--namespace.md) mediante la utilidad [MOFCOMP](mofcomp.md) o la interfaz [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="2a790-117">Compile and load the [**\_\_Namespace**](--namespace.md) instance using the [mofcomp](mofcomp.md) utility or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span> <span data-ttu-id="2a790-118">Tanto MOFCOMP como la interfaz **IMofCompiler** cargan automáticamente el espacio de nombres en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="2a790-118">Both mofcomp and the **IMofCompiler** interface automatically load the namespace into the current directory.</span></span> <span data-ttu-id="2a790-119">Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="2a790-119">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a790-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a790-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a790-121">**Calificadores WMI estándar**</span><span class="sxs-lookup"><span data-stu-id="2a790-121">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> </dl>

 

 



