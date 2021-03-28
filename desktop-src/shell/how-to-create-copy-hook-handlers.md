---
description: Usar las extensiones de Shell para implementar un controlador de enlace de copia.
ms.assetid: 05808281-84fb-402d-9fa1-3a747b29d030
title: Cómo crear controladores de enlace de copia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1468839eacc10272f8f97a120b98ada6d580bacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276751"
---
# <a name="how-to-create-copy-hook-handlers"></a><span data-ttu-id="6ebf9-103">Cómo crear controladores de enlace de copia</span><span class="sxs-lookup"><span data-stu-id="6ebf9-103">How to Create Copy Hook Handlers</span></span>

<span data-ttu-id="6ebf9-104">Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se explican en [crear controladores de extensión de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="6ebf9-104">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="6ebf9-105">Este documento se centra en los aspectos de la implementación que son específicos de los controladores de enlace de copia.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-105">This document focuses on those aspects of implementation that are specific to copy hook handlers.</span></span>

-   [<span data-ttu-id="6ebf9-106">Implementar controladores de enlace de copia</span><span class="sxs-lookup"><span data-stu-id="6ebf9-106">Implementing Copy Hook Handlers</span></span>](#step-1-implementing-copy-hook-handlers)
-   [<span data-ttu-id="6ebf9-107">Registrando controladores de enlace de copia</span><span class="sxs-lookup"><span data-stu-id="6ebf9-107">Registering Copy Hook Handlers</span></span>](#step-2-registering-copy-hook-handlers)
-   [<span data-ttu-id="6ebf9-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ebf9-108">Related topics</span></span>](#related-topics)

## <a name="instructions"></a><span data-ttu-id="6ebf9-109">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="6ebf9-109">Instructions</span></span>

### <a name="step-1-implementing-copy-hook-handlers"></a><span data-ttu-id="6ebf9-110">Paso 1: implementación de controladores de enlace de copia</span><span class="sxs-lookup"><span data-stu-id="6ebf9-110">Step 1: Implementing Copy Hook Handlers</span></span>

<span data-ttu-id="6ebf9-111">Al igual que todos los controladores de extensión de Shell, los controladores de enlace de copia son objetos de modelo de objetos componentes (COM) en proceso implementados como archivos dll.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-111">Like all Shell extension handlers, copy hook handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="6ebf9-112">Exportan una interfaz además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6ebf9-112">They export one interface in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)).</span></span> <span data-ttu-id="6ebf9-113">El shell inicializa el controlador directamente, por lo que no hay necesidad de una interfaz de inicialización como [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).</span><span class="sxs-lookup"><span data-stu-id="6ebf9-113">The Shell initializes the handler directly, so there is no need for an initialization interface such as [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).</span></span>

<span data-ttu-id="6ebf9-114">La interfaz [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) tiene un único método, [**ICopyHook:: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6ebf9-114">The [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) interface has a single method, [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)).</span></span> <span data-ttu-id="6ebf9-115">Cuando se va a migrar una carpeta, el shell llama a este método.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-115">When a folder is about to be moved, the Shell calls this method.</span></span> <span data-ttu-id="6ebf9-116">Pasa una gran variedad de información, entre las que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="6ebf9-116">It passes in a variety of information, including:</span></span>

-   <span data-ttu-id="6ebf9-117">Nombre de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-117">The folder's name.</span></span>
-   <span data-ttu-id="6ebf9-118">El destino de la carpeta o el nuevo nombre.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-118">The folder's destination or new name.</span></span>
-   <span data-ttu-id="6ebf9-119">Operación que se está intentando.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-119">The operation that is being attempted.</span></span>
-   <span data-ttu-id="6ebf9-120">Los atributos de las carpetas de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-120">The attributes of the source and destination folders.</span></span>
-   <span data-ttu-id="6ebf9-121">Identificador de ventana que se puede utilizar para mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-121">A window handle that can be used to display a user interface.</span></span>

<span data-ttu-id="6ebf9-122">Cuando se llama al método [**ICopyHook:: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) del controlador, devuelve uno de los tres valores siguientes para indicar al shell cómo debe continuar.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-122">When your handler's [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) method is called, it returns one of the three following values to indicate to the Shell how it should proceed.</span></span>



| <span data-ttu-id="6ebf9-123">Value</span><span class="sxs-lookup"><span data-stu-id="6ebf9-123">Value</span></span>    | <span data-ttu-id="6ebf9-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ebf9-124">Description</span></span>                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ebf9-125">IDYES</span><span class="sxs-lookup"><span data-stu-id="6ebf9-125">IDYES</span></span>    | <span data-ttu-id="6ebf9-126">Permite la operación.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-126">Allows the operation.</span></span>                                                                                                                            |
| <span data-ttu-id="6ebf9-127">IDNO</span><span class="sxs-lookup"><span data-stu-id="6ebf9-127">IDNO</span></span>     | <span data-ttu-id="6ebf9-128">Impide la operación en esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-128">Prevents the operation on this folder.</span></span> <span data-ttu-id="6ebf9-129">El shell puede continuar con cualquier otra operación que se haya aprobado, como una operación de copia por lotes.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-129">The Shell can continue with any other operations that have been approved, such as a batch copy operation.</span></span> |
| <span data-ttu-id="6ebf9-130">IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="6ebf9-130">IDCANCEL</span></span> | <span data-ttu-id="6ebf9-131">Evita la operación actual y cancela las operaciones pendientes.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-131">Prevents the current operation and cancels any pending operations.</span></span>                                                                               |



 

### <a name="step-2-registering-copy-hook-handlers"></a><span data-ttu-id="6ebf9-132">Paso 2: registrar controladores de enlace de copia</span><span class="sxs-lookup"><span data-stu-id="6ebf9-132">Step 2: Registering Copy Hook Handlers</span></span>

<span data-ttu-id="6ebf9-133">Los controladores de enlace de copia para las carpetas se registran en la subclave del directorio **\_ \_ raíz de las clases HKEY** \\  \\ **shellex** \\ **CopyHookHandlers** .</span><span class="sxs-lookup"><span data-stu-id="6ebf9-133">Copy hook handlers for folders are registered under the **HKEY\_CLASSES\_ROOT**\\**Directory**\\**shellex**\\**CopyHookHandlers** subkey.</span></span> <span data-ttu-id="6ebf9-134">Cree una subclave de **CopyHookHandlers** denominada para el controlador y establezca el valor predeterminado de la subclave en la forma de cadena del GUID del identificador de clase (CLSID) del controlador.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-134">Create a subkey of **CopyHookHandlers** named for the handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="6ebf9-135">En el ejemplo siguiente se agrega la subclave **MyCopyHandler** a la lista de controladores del enlace de copia del shell.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-135">The following example adds the **MyCopyHandler** subkey to the Shell's list of copy hook handlers.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         CopyHookHandlers
            MyCopyHandler
               (Default) = {MyCopyHandler CLSID GUID}
```

<span data-ttu-id="6ebf9-136">Los controladores de enlace de copia para objetos de impresora se registran esencialmente de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-136">Copy hook handlers for printer objects are registered in essentially the same way.</span></span> <span data-ttu-id="6ebf9-137">La única diferencia es que debe registrarlos en la subclave de **\_ las impresoras \_ raíz de las clases HKEY** \\  .</span><span class="sxs-lookup"><span data-stu-id="6ebf9-137">The only difference is that you must register them under the **HKEY\_CLASSES\_ROOT**\\**Printers** subkey.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ebf9-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ebf9-138">Remarks</span></span>

<span data-ttu-id="6ebf9-139">Normalmente, los usuarios y las aplicaciones pueden copiar, trasladar, eliminar o cambiar el nombre de las carpetas con pocas restricciones.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-139">Normally, users and applications can copy, move, delete, or rename folders with few restrictions.</span></span> <span data-ttu-id="6ebf9-140">Mediante la implementación de un controlador de enlace de copia, puede controlar si estas operaciones tienen lugar.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-140">By implementing a copy hook handler, you can control whether these operations take place.</span></span> <span data-ttu-id="6ebf9-141">Por ejemplo, la implementación de este tipo de controlador le permite evitar que las carpetas críticas se cambien de nombre o se eliminen.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-141">For instance, implementing such a handler allows you to prevent critical folders from being renamed or deleted.</span></span> <span data-ttu-id="6ebf9-142">Los controladores de enlace de copia también se pueden implementar para objetos de impresora.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-142">Copy hook handlers can also be implemented for printer objects.</span></span>

<span data-ttu-id="6ebf9-143">Los controladores de enlace de copia son globales.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-143">Copy hook handlers are global.</span></span> <span data-ttu-id="6ebf9-144">El shell llama a todos los controladores registrados cada vez que una aplicación o un usuario intenta copiar, quitar, eliminar o cambiar el nombre de una carpeta o un objeto de impresora.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-144">The Shell calls all registered handlers every time an application or user attempts to copy, move, delete, or rename a folder or printer object.</span></span> <span data-ttu-id="6ebf9-145">El controlador no realiza la operación en sí.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-145">The handler does not perform the operation itself.</span></span> <span data-ttu-id="6ebf9-146">Solo lo aprueba o lo veta.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-146">It only approves or vetoes it.</span></span> <span data-ttu-id="6ebf9-147">Si todos los controladores aprueban, el shell realiza la operación.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-147">If all handlers approve, the Shell does the operation.</span></span> <span data-ttu-id="6ebf9-148">Si un controlador veta la operación, se cancela y no se llama a los controladores restantes.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-148">If any handler vetoes the operation, it is canceled and the remaining handlers are not called.</span></span> <span data-ttu-id="6ebf9-149">Los controladores de enlace de copia no se informan de si la operación se ha realizado correctamente o no, por lo que no se pueden usar para supervisar las operaciones de archivos.</span><span class="sxs-lookup"><span data-stu-id="6ebf9-149">Copy hook handlers are not informed of the success or failure of the operation, so they cannot be used to monitor file operations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ebf9-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ebf9-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ebf9-151">Creación de controladores de extensiones de shell</span><span class="sxs-lookup"><span data-stu-id="6ebf9-151">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

<span data-ttu-id="6ebf9-152">[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6ebf9-152">[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))</span></span>
</dt> </dl>

 

 
