---
description: 'Tiene dos opciones al compilar un archivo MOF: mediante la utilidad de línea de comandos o mediante una interfaz de programación.'
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Ejecución del compilador MOF en un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f62834944e995c3e7f3763c460d72f9f70aa66
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230242"
---
# <a name="running-the-mof-compiler-on-a-file"></a><span data-ttu-id="48fa1-103">Ejecución del compilador MOF en un archivo</span><span class="sxs-lookup"><span data-stu-id="48fa1-103">Running the MOF Compiler on a File</span></span>

<span data-ttu-id="48fa1-104">Tiene dos opciones al compilar un archivo MOF: mediante la utilidad de línea de comandos o mediante una interfaz de programación.</span><span class="sxs-lookup"><span data-stu-id="48fa1-104">You have two choices when compiling a MOF file: using the command-line utility or using a programmatic interface.</span></span>

<span data-ttu-id="48fa1-105">Hasta que ejecute el compilador MOF, [**Mofcomp.exe**](mofcomp.md), un proveedor no está registrado con WMI y las clases que creó en el archivo MOF no están disponibles en el [*repositorio WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="48fa1-105">Until you run the MOF compiler, [**Mofcomp.exe**](mofcomp.md), a provider is not registered with WMI and the classes it created in the MOF file are not available in the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="48fa1-106">En el procedimiento siguiente se describe cómo compilar un archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="48fa1-106">The following procedure describes how to compile a MOF file.</span></span>

<span data-ttu-id="48fa1-107">**Para ejecutar el compilador MOF en un archivo desde la línea de comandos**</span><span class="sxs-lookup"><span data-stu-id="48fa1-107">**To run the MOF compiler on a file from the command line**</span></span>

1.  <span data-ttu-id="48fa1-108">Llame al compilador MOF desde la línea de comandos con la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="48fa1-108">Call the MOF compiler from the command line, using the following syntax.</span></span>

    <span data-ttu-id="48fa1-109">**mofcomp** _MOFfile_**.mof**</span><span class="sxs-lookup"><span data-stu-id="48fa1-109">**mofcomp** _MOFfile_**.mof**</span></span>

    <span data-ttu-id="48fa1-110">El compilador de MOF admite una variedad de modificadores para controlar situaciones de procesamiento especiales.</span><span class="sxs-lookup"><span data-stu-id="48fa1-110">The MOF compiler supports a variety of switches to control special processing situations.</span></span> <span data-ttu-id="48fa1-111">Todos los modificadores son opcionales y se permite cualquier combinación de modificadores.</span><span class="sxs-lookup"><span data-stu-id="48fa1-111">All of the switches are optional, and any combination of switches is allowed.</span></span> <span data-ttu-id="48fa1-112">Sin embargo, no tiene sentido usar algunos de los modificadores en combinación con otros.</span><span class="sxs-lookup"><span data-stu-id="48fa1-112">However, it does not make sense to use some of the switches in combination with others.</span></span> <span data-ttu-id="48fa1-113">Por ejemplo, para combinar los modificadores **-class:updateonly** y **-class:createonly,** el compilador no realiza ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="48fa1-113">For example, to combine the **-class:updateonly** and **-class:createonly** switches results in the compiler not performing any action.</span></span>

    <span data-ttu-id="48fa1-114">De forma predeterminada, Mofcomp.exe las clases compiladas en el espacio de \\ nombres WMI predeterminado raíz.</span><span class="sxs-lookup"><span data-stu-id="48fa1-114">By default, Mofcomp.exe stores the compiled classes in the root\\default WMI namespace.</span></span> <span data-ttu-id="48fa1-115">Tenga en cuenta que el espacio de nombres predeterminado Mofcomp.exe no es el mismo que el espacio de nombres predeterminado para scripting.</span><span class="sxs-lookup"><span data-stu-id="48fa1-115">Note that the default namespace for Mofcomp.exe is not the same as the default namespace for scripting.</span></span> <span data-ttu-id="48fa1-116">El espacio de nombres predeterminado para scripting se especifica en el Control WMI de la pestaña Opciones avanzadas. Para obtener más información, vea [Establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="48fa1-116">The default namespace for scripting is specified in the WMI Control on the Advanced tab. For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

    <span data-ttu-id="48fa1-117">Puede cambiar el espacio de nombres que recibe las clases de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="48fa1-117">You can change the namespace that receives the classes in two ways.</span></span>

    1.  <span data-ttu-id="48fa1-118">Use el **modificador -N** para el **comando mofcomp.**</span><span class="sxs-lookup"><span data-stu-id="48fa1-118">Use the **-N** switch for the **mofcomp** command.</span></span>
    2.  <span data-ttu-id="48fa1-119">Inserte el espacio de nombres \# [**pragma del comando de preprocesador**](pragma-namespace.md) en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="48fa1-119">Insert the preprocessor command \#[**pragma namespace**](pragma-namespace.md) in the MOF file.</span></span>

2.  <span data-ttu-id="48fa1-120">Opcionalmente, puede compilar un archivo MOF mediante programación.</span><span class="sxs-lookup"><span data-stu-id="48fa1-120">Optionally, you can compile a MOF file programmatically.</span></span> <span data-ttu-id="48fa1-121">Para obtener más información, [**vea IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span><span class="sxs-lookup"><span data-stu-id="48fa1-121">For more information, see [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span></span>

## <a name="related-topics"></a><span data-ttu-id="48fa1-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="48fa1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48fa1-123">Compilación de archivos MOF</span><span class="sxs-lookup"><span data-stu-id="48fa1-123">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="48fa1-124">**mofcomp**</span><span class="sxs-lookup"><span data-stu-id="48fa1-124">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="48fa1-125">Comandos de preprocesador</span><span class="sxs-lookup"><span data-stu-id="48fa1-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



