---
description: IContextMenu es la interfaz más eficaz, pero también la más complicada de implementar.
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: Cómo implementar la interfaz IContextMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f251b9a64c3f401239eeb7c88286c016f399cc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001905"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a><span data-ttu-id="17c03-103">Cómo implementar la interfaz IContextMenu</span><span class="sxs-lookup"><span data-stu-id="17c03-103">How to Implement the IContextMenu Interface</span></span>

<span data-ttu-id="17c03-104">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) es la interfaz más eficaz, pero también la más complicada de implementar.</span><span class="sxs-lookup"><span data-stu-id="17c03-104">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated interface to implement.</span></span> <span data-ttu-id="17c03-105">Se recomienda encarecidamente implementar un verbo utilizando uno de los métodos estáticos Verb.</span><span class="sxs-lookup"><span data-stu-id="17c03-105">We strongly recommend that you implement a verb by using one of the static verb methods.</span></span> <span data-ttu-id="17c03-106">Para obtener más información, vea [elegir un método de menú contextual estático o dinámico](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="17c03-106">For more information, see [Choosing a Static or Dynamic Shortcut Menu Method](shortcut-choose-method.md).</span></span> <span data-ttu-id="17c03-107">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) tiene tres métodos, [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)y [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), que se describen aquí en detalle.</span><span class="sxs-lookup"><span data-stu-id="17c03-107">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) has three methods, [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand), and [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), which are discussed here in detail.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="17c03-108">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="17c03-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="17c03-109">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="17c03-109">Technologies</span></span>

-   <span data-ttu-id="17c03-110">C++</span><span class="sxs-lookup"><span data-stu-id="17c03-110">C++</span></span>

### <a name="prerequisites"></a><span data-ttu-id="17c03-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="17c03-111">Prerequisites</span></span>

-   <span data-ttu-id="17c03-112">Verbo estático</span><span class="sxs-lookup"><span data-stu-id="17c03-112">Static Verb</span></span>
-   <span data-ttu-id="17c03-113">Menú contextual</span><span class="sxs-lookup"><span data-stu-id="17c03-113">Shortcut Menu</span></span>

## <a name="instructions"></a><span data-ttu-id="17c03-114">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="17c03-114">Instructions</span></span>

### <a name="icontextmenugetcommandstring-method"></a><span data-ttu-id="17c03-115">IContextMenu:: GetCommandString (método)</span><span class="sxs-lookup"><span data-stu-id="17c03-115">IContextMenu::GetCommandString Method</span></span>

<span data-ttu-id="17c03-116">El método [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) del controlador se usa para devolver el nombre canónico de un verbo.</span><span class="sxs-lookup"><span data-stu-id="17c03-116">The handler's [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) method is used to return the canonical name for a verb.</span></span> <span data-ttu-id="17c03-117">Este método es opcional.</span><span class="sxs-lookup"><span data-stu-id="17c03-117">This method is optional.</span></span> <span data-ttu-id="17c03-118">En Windows XP y versiones anteriores de Windows, cuando el explorador de Windows tiene una barra de estado, este método se usa para recuperar el texto de ayuda que se muestra en la barra de estado de un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="17c03-118">In Windows XP and earlier versions of Windows, when Windows Explorer has a Status bar, this method is used to retrieve the help text that is displayed in the Status bar for a menu item.</span></span>

<span data-ttu-id="17c03-119">El parámetro *idCmd* contiene el desplazamiento de identificador del comando que se definió cuando se llamó a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="17c03-119">The *idCmd* parameter holds the identifier offset of the command that was defined when [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) was called.</span></span> <span data-ttu-id="17c03-120">Si se solicita una cadena de ayuda, *uFlags* se establecerá en **GC \_ HELPTEXTW**.</span><span class="sxs-lookup"><span data-stu-id="17c03-120">If a help string is requested, *uFlags* will be set to **GCS\_HELPTEXTW**.</span></span> <span data-ttu-id="17c03-121">Copie la cadena de ayuda en el búfer de *pszName empiezan* , convirtiéndola en un **PWSTR**.</span><span class="sxs-lookup"><span data-stu-id="17c03-121">Copy the help string to the *pszName* buffer, casting it to a **PWSTR**.</span></span> <span data-ttu-id="17c03-122">La cadena de verbo se solicita estableciendo *uFlags* en **GC \_ VERBW**.</span><span class="sxs-lookup"><span data-stu-id="17c03-122">The verb string is requested by setting *uFlags* to **GCS\_VERBW**.</span></span> <span data-ttu-id="17c03-123">Copie la cadena adecuada en *pszName empiezan*, al igual que con la cadena de ayuda.</span><span class="sxs-lookup"><span data-stu-id="17c03-123">Copy the appropriate string to *pszName*, just as with the help string.</span></span> <span data-ttu-id="17c03-124">Los controladores de menú contextual no usan las marcas **GC \_ validatea** y **GC \_ VALIDATEW** .</span><span class="sxs-lookup"><span data-stu-id="17c03-124">The **GCS\_VALIDATEA** and **GCS\_VALIDATEW** flags are not used by shortcut menu handlers.</span></span>

<span data-ttu-id="17c03-125">En el ejemplo siguiente se muestra una implementación simple de [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) que corresponde al ejemplo [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) proporcionado en la sección [IContextMenu:: QueryContextMenu Method](shortcut-menu-using-dynamic-verbs.md) de este tema.</span><span class="sxs-lookup"><span data-stu-id="17c03-125">The following example shows a simple implementation of [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) that corresponds to the [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) example given in the [IContextMenu::QueryContextMenu Method](shortcut-menu-using-dynamic-verbs.md) section of this topic.</span></span> <span data-ttu-id="17c03-126">Dado que el controlador solo agrega un elemento de menú, solo hay un conjunto de cadenas que se pueden devolver.</span><span class="sxs-lookup"><span data-stu-id="17c03-126">Because the handler adds only one menu item, there is only one set of strings that can be returned.</span></span> <span data-ttu-id="17c03-127">El método comprueba si *idCmd* es válido y, si es así, devuelve la cadena solicitada.</span><span class="sxs-lookup"><span data-stu-id="17c03-127">The method tests whether *idCmd* is valid and, if it is, returns the requested string.</span></span>

<span data-ttu-id="17c03-128">La función [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) se usa para copiar la cadena solicitada en *pszName empiezan* para asegurarse de que la cadena copiada no supera el tamaño del búfer especificado por *cchName*.</span><span class="sxs-lookup"><span data-stu-id="17c03-128">The [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) function is used to copy the requested string to *pszName* to ensure that the copied string does not exceed the size of the buffer specified by *cchName*.</span></span> <span data-ttu-id="17c03-129">En este ejemplo solo se implementa la compatibilidad con los valores Unicode de *uFlags*, ya que solo se han utilizado en el explorador de Windows desde Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="17c03-129">This example implements support only for the Unicode values of *uFlags*, because only those have been used in Windows Explorer since Windows 2000.</span></span>


```
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb that is passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a><span data-ttu-id="17c03-130">IContextMenu:: InvokeCommand (método)</span><span class="sxs-lookup"><span data-stu-id="17c03-130">IContextMenu::InvokeCommand Method</span></span>

<span data-ttu-id="17c03-131">Se llama a este método cuando un usuario hace clic en un elemento de menú para indicar al controlador que ejecute el comando asociado.</span><span class="sxs-lookup"><span data-stu-id="17c03-131">This method is called when a user clicks a menu item to tell the handler to run the associated command.</span></span> <span data-ttu-id="17c03-132">El parámetro *pici* apunta a una estructura que contiene la información necesaria para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="17c03-132">The *pici* parameter points to a structure that contains the information required to run the command.</span></span>

<span data-ttu-id="17c03-133">Aunque *pici* se declara en ShlObj. h como una estructura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , en la práctica suele apuntar a una estructura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) .</span><span class="sxs-lookup"><span data-stu-id="17c03-133">Although *pici* is declared in Shlobj.h as a [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) structure, in practice it often points to a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure.</span></span> <span data-ttu-id="17c03-134">Esta estructura es una versión extendida de **CMINVOKECOMMANDINFO** y tiene varios miembros adicionales que permiten pasar cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="17c03-134">This structure is an extended version of **CMINVOKECOMMANDINFO** and has several additional members that make it possible to pass Unicode strings.</span></span>

<span data-ttu-id="17c03-135">Compruebe el miembro **cbSize** de *pici* para determinar la estructura que se ha pasado.</span><span class="sxs-lookup"><span data-stu-id="17c03-135">Check the **cbSize** member of *pici* to determine which structure was passed in.</span></span> <span data-ttu-id="17c03-136">Si es una estructura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) y el miembro **fMask** tiene establecida la **marca \_ \_ Unicode CMIC Mask** , convierta *pici* en **CMINVOKECOMMANDINFOEX**.</span><span class="sxs-lookup"><span data-stu-id="17c03-136">If it is a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure and the **fMask** member has the **CMIC\_MASK\_UNICODE** flag set, cast *pici* to **CMINVOKECOMMANDINFOEX**.</span></span> <span data-ttu-id="17c03-137">Esto permite que la aplicación use la información Unicode contenida en los cinco últimos miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="17c03-137">This enables your application to use the Unicode information that is contained in the last five members of the structure.</span></span>

<span data-ttu-id="17c03-138">El miembro **lpVerb** o **lpVerbW** de la estructura se usa para identificar el comando que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="17c03-138">The structure's **lpVerb** or **lpVerbW** member is used to identify the command to be executed.</span></span> <span data-ttu-id="17c03-139">Los comandos se identifican de una de las dos maneras siguientes:</span><span class="sxs-lookup"><span data-stu-id="17c03-139">Commands are identified in one of the following two ways:</span></span>

-   <span data-ttu-id="17c03-140">Por la cadena de verbo del comando</span><span class="sxs-lookup"><span data-stu-id="17c03-140">By the command's verb string</span></span>
-   <span data-ttu-id="17c03-141">Por el desplazamiento del identificador del comando</span><span class="sxs-lookup"><span data-stu-id="17c03-141">By the command's identifier offset</span></span>

<span data-ttu-id="17c03-142">Para distinguir entre estos dos casos, Compruebe la palabra de orden superior de **lpVerb** para el caso ANSI o **lpVerbW** para el caso de Unicode.</span><span class="sxs-lookup"><span data-stu-id="17c03-142">To distinguish between these two cases, check the high-order word of **lpVerb** for the ANSI case or **lpVerbW** for the Unicode case.</span></span> <span data-ttu-id="17c03-143">Si la palabra de orden superior es distinto de cero, **lpVerb** o **lpVerbW** contiene una cadena de verbo.</span><span class="sxs-lookup"><span data-stu-id="17c03-143">If the high-order word is nonzero, **lpVerb** or **lpVerbW** holds a verb string.</span></span> <span data-ttu-id="17c03-144">Si la palabra de orden superior es cero, el desplazamiento del comando se encuentra en la palabra de orden inferior de **lpVerb**.</span><span class="sxs-lookup"><span data-stu-id="17c03-144">If the high-order word is zero, the command offset is in the low-order word of **lpVerb**.</span></span>

<span data-ttu-id="17c03-145">En el ejemplo siguiente se muestra una implementación simple de [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) que corresponde a los ejemplos [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) y [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) especificados antes y después de esta sección.</span><span class="sxs-lookup"><span data-stu-id="17c03-145">The following example shows a simple implementation of [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) and [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) examples given before and after this section.</span></span> <span data-ttu-id="17c03-146">El método determina primero la estructura que se va a pasar.</span><span class="sxs-lookup"><span data-stu-id="17c03-146">The method first determines which structure is being passed in.</span></span> <span data-ttu-id="17c03-147">A continuación, determina si el comando se identifica por su desplazamiento o por su verbo.</span><span class="sxs-lookup"><span data-stu-id="17c03-147">It then determines whether the command is identified by its offset or its verb.</span></span> <span data-ttu-id="17c03-148">Si **lpVerb** o **lpVerbW** contiene un verbo o desplazamiento válido, el método muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="17c03-148">If **lpVerb** or **lpVerbW** holds a valid verb or offset, the method displays a message box.</span></span>


```
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a><span data-ttu-id="17c03-149">IContextMenu:: QueryContextMenu (método)</span><span class="sxs-lookup"><span data-stu-id="17c03-149">IContextMenu::QueryContextMenu Method</span></span>

<span data-ttu-id="17c03-150">El shell llama a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) para habilitar el controlador de menú contextual para agregar sus elementos de menú al menú.</span><span class="sxs-lookup"><span data-stu-id="17c03-150">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) to enable the shortcut menu handler to add its menu items to the menu.</span></span> <span data-ttu-id="17c03-151">Pasa el identificador **HMENU** en el parámetro *HMENU* .</span><span class="sxs-lookup"><span data-stu-id="17c03-151">It passes in the **HMENU** handle in the *hmenu* parameter.</span></span> <span data-ttu-id="17c03-152">El parámetro *indexMenu* se establece en el índice que se va a usar para el primer elemento de menú que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="17c03-152">The *indexMenu* parameter is set to the index to be used for the first menu item that is to be added.</span></span>

<span data-ttu-id="17c03-153">Los elementos de menú que agregue el controlador deben tener identificadores que se encuentren entre los valores de los parámetros *idCmdFirst* y *idCmdLast* .</span><span class="sxs-lookup"><span data-stu-id="17c03-153">Any menu items that are added by the handler must have identifiers that fall between the values in the *idCmdFirst* and *idCmdLast* parameters.</span></span> <span data-ttu-id="17c03-154">Normalmente, el primer identificador de comando se establece en *idCmdFirst*, que se incrementa en uno (1) para cada comando adicional.</span><span class="sxs-lookup"><span data-stu-id="17c03-154">Typically, the first command identifier is set to *idCmdFirst*, which is incremented by one (1) for each additional command.</span></span> <span data-ttu-id="17c03-155">Esta práctica le ayuda a evitar superar *idCmdLast* y maximiza el número de identificadores disponibles en caso de que el shell llame a más de un controlador.</span><span class="sxs-lookup"><span data-stu-id="17c03-155">This practice helps you to avoid exceeding *idCmdLast* and maximizes the number of available identifiers in case the Shell calls more than one handler.</span></span>

<span data-ttu-id="17c03-156">El *desplazamiento de comandos* de un identificador de elemento es la diferencia entre el identificador y el valor de *idCmdFirst*.</span><span class="sxs-lookup"><span data-stu-id="17c03-156">An item identifier's *command offset* is the difference between the identifier and the value in *idCmdFirst*.</span></span> <span data-ttu-id="17c03-157">Almacene el desplazamiento de cada elemento que el controlador agrega al menú contextual, porque el shell podría usar el desplazamiento para identificar el elemento si después llama a [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) o [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span><span class="sxs-lookup"><span data-stu-id="17c03-157">Store the offset of each item that your handler adds to the shortcut menu, because the Shell might use the offset to identify the item if it subsequently calls [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) or [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span>

<span data-ttu-id="17c03-158">También debe asignar un [verbo](launch.md) a cada comando que agregue.</span><span class="sxs-lookup"><span data-stu-id="17c03-158">You should also assign a [verb](launch.md) to each command that you add.</span></span> <span data-ttu-id="17c03-159">Un verbo es una cadena que se puede utilizar en lugar del desplazamiento para identificar el comando cuando se llama a [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .</span><span class="sxs-lookup"><span data-stu-id="17c03-159">A verb is a string that can be used instead of the offset to identify the command when [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) is called.</span></span> <span data-ttu-id="17c03-160">También lo usan funciones como [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para ejecutar comandos de menú contextual.</span><span class="sxs-lookup"><span data-stu-id="17c03-160">It is also used by functions such as [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to execute shortcut menu commands.</span></span>

<span data-ttu-id="17c03-161">Hay tres marcas que se pueden pasar a través del parámetro *uFlags* que son relevantes para los controladores de menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="17c03-161">There are three flags that can be passed in through the *uFlags* parameter that are relevant to shortcut menu handlers.</span></span> <span data-ttu-id="17c03-162">Se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="17c03-162">They are described in the following table.</span></span>



| <span data-ttu-id="17c03-163">Marca</span><span class="sxs-lookup"><span data-stu-id="17c03-163">Flag</span></span>             | <span data-ttu-id="17c03-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="17c03-164">Description</span></span>                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17c03-165">CMF \_ DEFAULTONLY</span><span class="sxs-lookup"><span data-stu-id="17c03-165">CMF\_DEFAULTONLY</span></span> | <span data-ttu-id="17c03-166">El usuario ha seleccionado el comando predeterminado, normalmente haciendo doble clic en el objeto.</span><span class="sxs-lookup"><span data-stu-id="17c03-166">The user has selected the default command, usually by double-clicking the object.</span></span> <span data-ttu-id="17c03-167">[**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) debe devolver el control al shell sin modificar el menú.</span><span class="sxs-lookup"><span data-stu-id="17c03-167">[**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) should return control to the Shell without modifying the menu.</span></span> |
| <span data-ttu-id="17c03-168">CMF \_ NOdefault</span><span class="sxs-lookup"><span data-stu-id="17c03-168">CMF\_NODEFAULT</span></span>   | <span data-ttu-id="17c03-169">Ningún elemento del menú debe ser el elemento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="17c03-169">No item in the menu should be the default item.</span></span> <span data-ttu-id="17c03-170">El método debe agregar sus comandos al menú.</span><span class="sxs-lookup"><span data-stu-id="17c03-170">The method should add its commands to the menu.</span></span>                                                                                                                          |
| <span data-ttu-id="17c03-171">CMF \_ normal</span><span class="sxs-lookup"><span data-stu-id="17c03-171">CMF\_NORMAL</span></span>      | <span data-ttu-id="17c03-172">El menú contextual se mostrará normalmente.</span><span class="sxs-lookup"><span data-stu-id="17c03-172">The shortcut menu will be displayed normally.</span></span> <span data-ttu-id="17c03-173">El método debe agregar sus comandos al menú.</span><span class="sxs-lookup"><span data-stu-id="17c03-173">The method should add its commands to the menu.</span></span>                                                                                                                            |



 

<span data-ttu-id="17c03-174">Use [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) o [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) para agregar elementos de menú a la lista.</span><span class="sxs-lookup"><span data-stu-id="17c03-174">Use either [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) or [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) to add menu items to the list.</span></span> <span data-ttu-id="17c03-175">A continuación, devuelva un valor **HRESULT** con la gravedad establecida en Severity \_ Success.</span><span class="sxs-lookup"><span data-stu-id="17c03-175">Then return an **HRESULT** value with the severity set to SEVERITY\_SUCCESS.</span></span> <span data-ttu-id="17c03-176">Establezca el valor del código en el desplazamiento del identificador de comando más grande que se asignó, más uno (1).</span><span class="sxs-lookup"><span data-stu-id="17c03-176">Set the code value to the offset of the largest command identifier that was assigned, plus one (1).</span></span> <span data-ttu-id="17c03-177">Por ejemplo, supongamos que *idCmdFirst* está establecido en 5 y agrega tres elementos al menú con identificadores de comando de 5, 7 y 8.</span><span class="sxs-lookup"><span data-stu-id="17c03-177">For example, assume that *idCmdFirst* is set to 5 and you add three items to the menu with command identifiers of 5, 7, and 8.</span></span> <span data-ttu-id="17c03-178">El valor devuelto debe ser MAKE \_ HRESULT (Severity \_ Success, 0, 8 + 1).</span><span class="sxs-lookup"><span data-stu-id="17c03-178">The return value should be MAKE\_HRESULT(SEVERITY\_SUCCESS, 0, 8 + 1).</span></span>

<span data-ttu-id="17c03-179">En el ejemplo siguiente se muestra una implementación simple de [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) que inserta un solo comando.</span><span class="sxs-lookup"><span data-stu-id="17c03-179">The following example shows a simple implementation of [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) that inserts a single command.</span></span> <span data-ttu-id="17c03-180">El desplazamiento de identificador del comando es la visualización de IDM \_ , que se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="17c03-180">The identifier offset for the command is IDM\_DISPLAY, which is set to zero.</span></span> <span data-ttu-id="17c03-181">Las variables **m \_ pszVerb** y **m \_ pwszVerb** son variables privadas que se usan para almacenar la cadena de verbo independiente del lenguaje asociada en los formatos ANSI y Unicode.</span><span class="sxs-lookup"><span data-stu-id="17c03-181">The **m\_pszVerb** and **m\_pwszVerb** variables are private variables that are used to store the associated language-independent verb string in both ANSI and Unicode formats.</span></span>


```
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));}
```



## <a name="remarks"></a><span data-ttu-id="17c03-182">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17c03-182">Remarks</span></span>

<span data-ttu-id="17c03-183">Para otras tareas de implementación de verbos, vea [crear controladores de menús contextuales](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="17c03-183">For other verb implementation tasks, see [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>

 

 
