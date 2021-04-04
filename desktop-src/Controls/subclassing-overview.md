---
title: Subclase de controles
description: Si un control hace casi todo lo que desea, pero necesita algunas características más, puede cambiar o agregar características al control original mediante su subclase.
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c013ee317ddeee6ff80dc4a26982d40d7117950
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078468"
---
# <a name="subclassing-controls"></a><span data-ttu-id="aa098-103">Subclase de controles</span><span class="sxs-lookup"><span data-stu-id="aa098-103">Subclassing Controls</span></span>

<span data-ttu-id="aa098-104">Si un control hace casi todo lo que desea, pero necesita algunas características más, puede cambiar o agregar características al control original mediante su subclase.</span><span class="sxs-lookup"><span data-stu-id="aa098-104">If a control does almost everything you want, but you need a few more features, you can change or add features to the original control by subclassing it.</span></span> <span data-ttu-id="aa098-105">Una subclase puede tener todas las características de una clase existente, así como las características adicionales que desee proporcionar.</span><span class="sxs-lookup"><span data-stu-id="aa098-105">A subclass can have all the features of an existing class as well as any additional features you want to give it.</span></span>

<span data-ttu-id="aa098-106">En este documento se explica cómo se crean las subclases e incluye los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="aa098-106">This document discusses how subclasses are created and includes the following topics.</span></span>

-   [<span data-ttu-id="aa098-107">Subclase de controles anteriores a ComCtl32.dll versión 6</span><span class="sxs-lookup"><span data-stu-id="aa098-107">Subclassing Controls Prior to ComCtl32.dll version 6</span></span>](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [<span data-ttu-id="aa098-108">Almacenar datos de usuario</span><span class="sxs-lookup"><span data-stu-id="aa098-108">Storing User Data</span></span>](#storing-user-data)
    -   [<span data-ttu-id="aa098-109">Desventajas del enfoque de subclases anterior</span><span class="sxs-lookup"><span data-stu-id="aa098-109">Disadvantages of the Old Subclassing Approach</span></span>](#disadvantages-of-the-old-subclassing-approach)
-   [<span data-ttu-id="aa098-110">Subclase de controles con ComCtl32.dll versión 6</span><span class="sxs-lookup"><span data-stu-id="aa098-110">Subclassing Controls Using ComCtl32.dll version 6</span></span>](#subclassing-controls-using-comctl32dll-version-6)
    -   [<span data-ttu-id="aa098-111">SetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="aa098-111">SetWindowSubclass</span></span>](#setwindowsubclass)
    -   [<span data-ttu-id="aa098-112">GetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="aa098-112">GetWindowSubclass</span></span>](#getwindowsubclass)
    -   [<span data-ttu-id="aa098-113">RemoveWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="aa098-113">RemoveWindowSubclass</span></span>](#removewindowsubclass)
    -   [<span data-ttu-id="aa098-114">DefSubclassProc</span><span class="sxs-lookup"><span data-stu-id="aa098-114">DefSubclassProc</span></span>](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a><span data-ttu-id="aa098-115">Subclase de controles anteriores a ComCtl32.dll versión 6</span><span class="sxs-lookup"><span data-stu-id="aa098-115">Subclassing Controls Prior to ComCtl32.dll version 6</span></span>

<span data-ttu-id="aa098-116">Puede colocar un control en una subclase y almacenar los datos de usuario dentro de un control.</span><span class="sxs-lookup"><span data-stu-id="aa098-116">You can put a control in a subclass and store user data within a control.</span></span> <span data-ttu-id="aa098-117">Esto se hace al usar versiones de ComCtl32.dll anteriores a la versión 6.</span><span class="sxs-lookup"><span data-stu-id="aa098-117">You do this when you use versions of ComCtl32.dll prior to version 6.</span></span> <span data-ttu-id="aa098-118">La creación de subclases con versiones anteriores de ComCtl32.dll tiene algunas desventajas.</span><span class="sxs-lookup"><span data-stu-id="aa098-118">There are some disadvantages in creating subclasses with earlier versions of ComCtl32.dll.</span></span>

<span data-ttu-id="aa098-119">Para crear un nuevo control, es mejor empezar con uno de los controles comunes de Windows y extenderlo para que se ajuste a una necesidad concreta.</span><span class="sxs-lookup"><span data-stu-id="aa098-119">To make a new control, it is best to start with one of the Windows common controls and extend it to fit a particular need.</span></span> <span data-ttu-id="aa098-120">Para extender un control, cree un control y reemplace su procedimiento de ventana existente por uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="aa098-120">To extend a control, create a control and replace its existing window procedure with a new one.</span></span> <span data-ttu-id="aa098-121">El nuevo procedimiento intercepta los mensajes del control y actúa en ellos o los pasa al procedimiento original para el procesamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="aa098-121">The new procedure intercepts the control's messages and either acts on them or passes them to the original procedure for default processing.</span></span> <span data-ttu-id="aa098-122">Utilice la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) o [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) para reemplazar el WndProc del control.</span><span class="sxs-lookup"><span data-stu-id="aa098-122">Use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) or [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) function to replace the WNDPROC of the control.</span></span> <span data-ttu-id="aa098-123">En el ejemplo de código siguiente se muestra cómo reemplazar un WNDPROC.</span><span class="sxs-lookup"><span data-stu-id="aa098-123">The following code sample shows how to replace a WNDPROC.</span></span>


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a><span data-ttu-id="aa098-124">Almacenar datos de usuario</span><span class="sxs-lookup"><span data-stu-id="aa098-124">Storing User Data</span></span>

<span data-ttu-id="aa098-125">Es posible que desee almacenar los datos de usuario con una ventana individual.</span><span class="sxs-lookup"><span data-stu-id="aa098-125">You might want to store user data with an individual window.</span></span> <span data-ttu-id="aa098-126">El nuevo procedimiento de ventana puede usar estos datos para determinar cómo dibujar el control o dónde enviar determinados mensajes.</span><span class="sxs-lookup"><span data-stu-id="aa098-126">This data can be used by the new window procedure to determine how to draw the control or where to send certain messages.</span></span> <span data-ttu-id="aa098-127">Por ejemplo, puede usar los datos para almacenar un puntero de clase de C++ en la clase que representa el control.</span><span class="sxs-lookup"><span data-stu-id="aa098-127">For example, you might use data to store a C++ class pointer to the class that represents the control.</span></span> <span data-ttu-id="aa098-128">En el ejemplo de código siguiente se muestra cómo usar [**SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) para almacenar datos con una ventana.</span><span class="sxs-lookup"><span data-stu-id="aa098-128">The following code sample shows how to use [**SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) to store data with a window.</span></span>


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a><span data-ttu-id="aa098-129">Desventajas del enfoque de subclases anterior</span><span class="sxs-lookup"><span data-stu-id="aa098-129">Disadvantages of the Old Subclassing Approach</span></span>

<span data-ttu-id="aa098-130">En la lista siguiente se indican algunas de las desventajas del uso del enfoque descrito anteriormente para subclases de un control.</span><span class="sxs-lookup"><span data-stu-id="aa098-130">The following list points out some of the disadvantages of using the previously described approach to subclassing a control.</span></span>

-   <span data-ttu-id="aa098-131">El procedimiento de ventana solo se puede reemplazar una vez.</span><span class="sxs-lookup"><span data-stu-id="aa098-131">The window procedure can only be replaced once.</span></span>
-   <span data-ttu-id="aa098-132">Es difícil quitar una subclase una vez creada.</span><span class="sxs-lookup"><span data-stu-id="aa098-132">It is difficult to remove a subclass after it is created.</span></span>
-   <span data-ttu-id="aa098-133">La Asociación de datos privados con una ventana es ineficaz.</span><span class="sxs-lookup"><span data-stu-id="aa098-133">Associating private data with a window is inefficient.</span></span>
-   <span data-ttu-id="aa098-134">Para llamar al siguiente procedimiento en una cadena de subclases, no puede convertir el procedimiento de ventana anterior y llamarlo; debe llamarlo mediante la función [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="aa098-134">To call the next procedure in a subclass chain, you cannot cast the old window procedure and call it, you must call it by using the [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) function.</span></span>

## <a name="subclassing-controls-using-comctl32dll-version-6"></a><span data-ttu-id="aa098-135">Subclase de controles con ComCtl32.dll versión 6</span><span class="sxs-lookup"><span data-stu-id="aa098-135">Subclassing Controls Using ComCtl32.dll version 6</span></span>

> [!Note]  
> <span data-ttu-id="aa098-136">ComCtl32.dll versión 6 solo es Unicode.</span><span class="sxs-lookup"><span data-stu-id="aa098-136">ComCtl32.dll version 6 is Unicode only.</span></span> <span data-ttu-id="aa098-137">Los controles comunes admitidos por ComCtl32.dll versión 6 no deben ser subclases (o superclase) con procedimientos de ventana ANSI.</span><span class="sxs-lookup"><span data-stu-id="aa098-137">The common controls supported by ComCtl32.dll version 6 should not be subclassed (or superclassed) with ANSI window procedures.</span></span>

 

<span data-ttu-id="aa098-138">ComCtl32.dll versión 6 contiene cuatro funciones que facilitan la creación de subclases y eliminan las desventajas descritas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="aa098-138">ComCtl32.dll version 6 contains four functions that make creating subclasses easier and eliminate the disadvantages previously discussed.</span></span> <span data-ttu-id="aa098-139">Las nuevas funciones encapsulan la administración implicada en varios conjuntos de datos de referencia, por lo que el desarrollador puede centrarse en las características de programación y no en la administración de subclases.</span><span class="sxs-lookup"><span data-stu-id="aa098-139">The new functions encapsulate the management involved with multiple sets of reference data, therefore the developer can focus on programming features and not on managing subclasses.</span></span> <span data-ttu-id="aa098-140">Las funciones de subclase son:</span><span class="sxs-lookup"><span data-stu-id="aa098-140">The subclassing functions are:</span></span>

-   [<span data-ttu-id="aa098-141">**SetWindowSubclass**</span><span class="sxs-lookup"><span data-stu-id="aa098-141">**SetWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [<span data-ttu-id="aa098-142">**GetWindowSubclass**</span><span class="sxs-lookup"><span data-stu-id="aa098-142">**GetWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [<span data-ttu-id="aa098-143">**RemoveWindowSubclass**</span><span class="sxs-lookup"><span data-stu-id="aa098-143">**RemoveWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [<span data-ttu-id="aa098-144">**DefSubclassProc**</span><span class="sxs-lookup"><span data-stu-id="aa098-144">**DefSubclassProc**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a><span data-ttu-id="aa098-145">SetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="aa098-145">SetWindowSubclass</span></span>

<span data-ttu-id="aa098-146">Esta función se usa para subclaser inicialmente una ventana.</span><span class="sxs-lookup"><span data-stu-id="aa098-146">This function is used to initially subclass a window.</span></span> <span data-ttu-id="aa098-147">Cada subclase se identifica de forma única mediante la dirección de *pfnSubclass* y su *uIdSubclass*.</span><span class="sxs-lookup"><span data-stu-id="aa098-147">Each subclass is uniquely identified by the address of the *pfnSubclass* and its *uIdSubclass*.</span></span> <span data-ttu-id="aa098-148">Ambos son parámetros de la función [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) .</span><span class="sxs-lookup"><span data-stu-id="aa098-148">Both of these are parameters of the [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) function.</span></span> <span data-ttu-id="aa098-149">Varias subclases pueden compartir el mismo procedimiento de subclase y el identificador puede identificar cada llamada.</span><span class="sxs-lookup"><span data-stu-id="aa098-149">Several subclasses can share the same subclass procedure and the ID can identify each call.</span></span> <span data-ttu-id="aa098-150">Para cambiar los datos de referencia, puede realizar llamadas subsiguientes a **SetWindowSubclass**.</span><span class="sxs-lookup"><span data-stu-id="aa098-150">To change reference data you can make subsequent calls to **SetWindowSubclass**.</span></span> <span data-ttu-id="aa098-151">La ventaja importante es que cada instancia de la subclase tiene sus propios datos de referencia.</span><span class="sxs-lookup"><span data-stu-id="aa098-151">The important advantage is that each subclass instance has its own reference data.</span></span>

<span data-ttu-id="aa098-152">La declaración de un procedimiento de subclase es ligeramente diferente de un procedimiento de ventana normal porque tiene dos elementos de datos adicionales: el identificador de la subclase y los datos de referencia.</span><span class="sxs-lookup"><span data-stu-id="aa098-152">The declaration of a subclass procedure is slightly different from a regular window procedure because it has two additional pieces of data: the subclass ID and the reference data.</span></span> <span data-ttu-id="aa098-153">Los dos últimos parámetros de la declaración de función siguiente muestran esto.</span><span class="sxs-lookup"><span data-stu-id="aa098-153">The last two parameters of the following function declaration show this.</span></span>


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



<span data-ttu-id="aa098-154">Cada vez que el nuevo procedimiento de ventana recibe un mensaje, se incluyen un identificador de subclase y datos de referencia.</span><span class="sxs-lookup"><span data-stu-id="aa098-154">Every time a message is received by the new window procedure, a subclass ID and reference data are included.</span></span>

> [!Note]  
> <span data-ttu-id="aa098-155">Todas las cadenas que se pasan al procedimiento son cadenas Unicode incluso si no se especifica Unicode como definición del preprocesador.</span><span class="sxs-lookup"><span data-stu-id="aa098-155">All strings passed to the procedure are Unicode strings even if Unicode is not specified as a preprocessor definition.</span></span>

 

<span data-ttu-id="aa098-156">En el ejemplo siguiente se muestra una implementación esqueleto de un procedimiento de ventana para un control de subclase.</span><span class="sxs-lookup"><span data-stu-id="aa098-156">The following example shows a skeleton implementation of a window procedure for a subclassed control.</span></span>


```
LRESULT CALLBACK OwnerDrawButtonProc(HWND hWnd, UINT uMsg, WPARAM wParam,
                               LPARAM lParam, UINT_PTR uIdSubclass, DWORD_PTR dwRefData)
{
    switch (uMsg)
    {
    case WM_PAINT:
        .
        .
        .
        return TRUE;
    // Other cases...
    } 
    return DefSubclassProc(hWnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="aa098-157">El procedimiento de ventana se puede adjuntar al control en el controlador [**\_ INITDIALOG de WM**](/windows/desktop/dlgbox/wm-initdialog) del procedimiento del cuadro de diálogo, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="aa098-157">The window procedure can be attached to the control in the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) handler of the dialog procedure, as shown in the following example.</span></span>


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a><span data-ttu-id="aa098-158">GetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="aa098-158">GetWindowSubclass</span></span>

<span data-ttu-id="aa098-159">Esta función recupera información sobre una subclase.</span><span class="sxs-lookup"><span data-stu-id="aa098-159">This function retrieves information about a subclass.</span></span> <span data-ttu-id="aa098-160">Por ejemplo, puede usar [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) para tener acceso a los datos de referencia.</span><span class="sxs-lookup"><span data-stu-id="aa098-160">For example, you can use [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) to access the reference data.</span></span>

### <a name="removewindowsubclass"></a><span data-ttu-id="aa098-161">RemoveWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="aa098-161">RemoveWindowSubclass</span></span>

<span data-ttu-id="aa098-162">Esta función quita las subclases.</span><span class="sxs-lookup"><span data-stu-id="aa098-162">This function removes subclasses.</span></span> <span data-ttu-id="aa098-163">[**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) en combinación con [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) permite agregar y quitar de forma dinámica las subclases.</span><span class="sxs-lookup"><span data-stu-id="aa098-163">[**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) in combination with [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) allows you to dynamically add and remove subclasses.</span></span>

### <a name="defsubclassproc"></a><span data-ttu-id="aa098-164">DefSubclassProc</span><span class="sxs-lookup"><span data-stu-id="aa098-164">DefSubclassProc</span></span>

<span data-ttu-id="aa098-165">La función [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) llama al siguiente controlador de la cadena de subclases.</span><span class="sxs-lookup"><span data-stu-id="aa098-165">The [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) function calls the next handler in the subclass chain.</span></span> <span data-ttu-id="aa098-166">La función también recupera el identificador y los datos de referencia apropiados y pasa la información al procedimiento de ventana siguiente.</span><span class="sxs-lookup"><span data-stu-id="aa098-166">The function also retrieves the proper ID and reference data and passes the information to the next window procedure.</span></span>

 

 