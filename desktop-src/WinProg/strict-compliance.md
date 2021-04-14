---
title: Cumplimiento estricto
description: Algunos códigos fuente que se compilan correctamente pueden generar mensajes de error cuando se habilita la comprobación estricta de tipos.
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d04c3a849dc62647758e3515728e3dd3f65dcb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420977"
---
# <a name="strict-compliance"></a><span data-ttu-id="da933-103">Cumplimiento estricto</span><span class="sxs-lookup"><span data-stu-id="da933-103">STRICT Compliance</span></span>

<span data-ttu-id="da933-104">Algunos códigos fuente que se compilan correctamente pueden generar mensajes de error cuando se habilita la comprobación **estricta** de tipos.</span><span class="sxs-lookup"><span data-stu-id="da933-104">Some source code that compiles successfully might produce error messages when you enable **STRICT** type checking.</span></span> <span data-ttu-id="da933-105">En las secciones siguientes se describen los requisitos mínimos para que el código se compile cuando **STRICT** esté habilitado.</span><span class="sxs-lookup"><span data-stu-id="da933-105">The following sections describe the minimal requirements for making your code compile when **STRICT** is enabled.</span></span> <span data-ttu-id="da933-106">Se recomiendan pasos adicionales, especialmente para generar código portable.</span><span class="sxs-lookup"><span data-stu-id="da933-106">Additional steps are recommended, especially to produce portable code.</span></span>

## <a name="general-requirements"></a><span data-ttu-id="da933-107">Requisitos generales</span><span class="sxs-lookup"><span data-stu-id="da933-107">General Requirements</span></span>

<span data-ttu-id="da933-108">El requisito principal es que debe declarar tipos de control y punteros de función correctos en lugar de confiar en tipos más generales.</span><span class="sxs-lookup"><span data-stu-id="da933-108">The principal requirement is that you must declare correct handle types and function pointers instead of relying on more general types.</span></span> <span data-ttu-id="da933-109">No se puede usar un tipo de identificador en el que se espera otro.</span><span class="sxs-lookup"><span data-stu-id="da933-109">You cannot use one handle type where another is expected.</span></span> <span data-ttu-id="da933-110">Esto también significa que puede que tenga que cambiar las declaraciones de función y utilizar más conversiones de tipos.</span><span class="sxs-lookup"><span data-stu-id="da933-110">This also means that you may have to change function declarations and use more type casts.</span></span>

<span data-ttu-id="da933-111">Para obtener los mejores resultados, el tipo de **identificador** genérico solo debe usarse cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="da933-111">For best results, the generic **HANDLE** type should be used only when necessary.</span></span>

## <a name="declaring-functions-within-your-application"></a><span data-ttu-id="da933-112">Declarar funciones dentro de la aplicación</span><span class="sxs-lookup"><span data-stu-id="da933-112">Declaring Functions Within Your Application</span></span>

<span data-ttu-id="da933-113">Asegúrese de que se declaran todas las funciones de aplicación.</span><span class="sxs-lookup"><span data-stu-id="da933-113">Make sure all application functions are declared.</span></span> <span data-ttu-id="da933-114">Se recomienda colocar todas las declaraciones de función en un archivo de inclusión porque puede examinar fácilmente las declaraciones y buscar los tipos de parámetro y de valor devuelto que se deben cambiar.</span><span class="sxs-lookup"><span data-stu-id="da933-114">Placing all function declarations in an include file is recommended because you can easily scan your declarations and look for parameter and return types that should be changed.</span></span>

<span data-ttu-id="da933-115">Si usa la opción del compilador **/ZG** para crear archivos de encabezado para las funciones, recuerde que obtendrá resultados diferentes en función de si ha habilitado la comprobación **estricta** de tipos.</span><span class="sxs-lookup"><span data-stu-id="da933-115">If you use the **/Zg** compiler option to create header files for your functions, remember that you will get different results depending on whether you have enabled **STRICT** type checking.</span></span> <span data-ttu-id="da933-116">Con **STRICT** deshabilitado, todos los tipos de identificador generan el mismo tipo base.</span><span class="sxs-lookup"><span data-stu-id="da933-116">With **STRICT** disabled, all handle types generate the same base type.</span></span> <span data-ttu-id="da933-117">Con **STRICT** habilitado, generan distintos tipos base.</span><span class="sxs-lookup"><span data-stu-id="da933-117">With **STRICT** enabled, they generate different base types.</span></span> <span data-ttu-id="da933-118">Para evitar conflictos, debe volver a crear el archivo de encabezado cada vez que habilite o deshabilite **STRICT**, o edite el archivo de encabezado para usar los tipos **hWnd**, **HDC**, **Handle**, etc., en lugar de los tipos base.</span><span class="sxs-lookup"><span data-stu-id="da933-118">To avoid conflict, you need to re-create the header file each time you enable or disable **STRICT**, or edit the header file to use the types **HWND**, **HDC**, **HANDLE**, and so on, instead of the base types.</span></span>

<span data-ttu-id="da933-119">Es posible que las declaraciones de función que copió de Windows. h en el código fuente hayan cambiado y que la declaración local no esté actualizada.</span><span class="sxs-lookup"><span data-stu-id="da933-119">Any function declarations that you copied from Windows.h into your source code may have changed, and your local declaration may be out of date.</span></span> <span data-ttu-id="da933-120">Quite la declaración local.</span><span class="sxs-lookup"><span data-stu-id="da933-120">Remove your local declaration.</span></span>

## <a name="types-that-require-casts"></a><span data-ttu-id="da933-121">Tipos que requieren conversiones</span><span class="sxs-lookup"><span data-stu-id="da933-121">Types that Require Casts</span></span>

<span data-ttu-id="da933-122">Algunas funciones tienen tipos de valor devueltos o parámetros genéricos.</span><span class="sxs-lookup"><span data-stu-id="da933-122">Some functions have generic return types or parameters.</span></span> <span data-ttu-id="da933-123">Por ejemplo, la función [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) devuelve datos que pueden ser cualquier número de tipos, dependiendo del contexto.</span><span class="sxs-lookup"><span data-stu-id="da933-123">For example, the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function returns data that may be any number of types, depending on the context.</span></span> <span data-ttu-id="da933-124">Cuando vea cualquiera de estas funciones en el código fuente, asegúrese de usar la conversión de tipos correcta y de que sea lo más específica posible.</span><span class="sxs-lookup"><span data-stu-id="da933-124">When you see any of these functions in your source code, make sure that you use the correct type cast and that it is as specific as possible.</span></span> <span data-ttu-id="da933-125">La lista siguiente es un ejemplo de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="da933-125">The following list is an example of these functions.</span></span>

-   [<span data-ttu-id="da933-126">**LocalLock**</span><span class="sxs-lookup"><span data-stu-id="da933-126">**LocalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [<span data-ttu-id="da933-127">**GlobalLock**</span><span class="sxs-lookup"><span data-stu-id="da933-127">**GlobalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [<span data-ttu-id="da933-128">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="da933-128">**GetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [<span data-ttu-id="da933-129">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="da933-129">**SetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [<span data-ttu-id="da933-130">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="da933-130">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [<span data-ttu-id="da933-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="da933-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [<span data-ttu-id="da933-132">**SendDlgItemMessage**</span><span class="sxs-lookup"><span data-stu-id="da933-132">**SendDlgItemMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

<span data-ttu-id="da933-133">Al llamar a [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)o [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), primero debe convertir el resultado al tipo **uint \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="da933-133">When you call [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), or [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), you should first cast the result to type **UINT\_PTR**.</span></span> <span data-ttu-id="da933-134">Debe realizar pasos similares para cualquier función que devuelva un valor **LRESULT** o **Long \_ ptr** , donde el resultado contiene un identificador.</span><span class="sxs-lookup"><span data-stu-id="da933-134">You need to take similar steps for any function that returns an **LRESULT** or **LONG\_PTR** value, where the result contains a handle.</span></span> <span data-ttu-id="da933-135">Esto es necesario para escribir código portable, ya que el tamaño de un identificador varía en función de la versión de Windows.</span><span class="sxs-lookup"><span data-stu-id="da933-135">This is necessary for writing portable code because the size of a handle varies, depending on the version of Windows.</span></span> <span data-ttu-id="da933-136">La conversión (**uint \_ ptr**) garantiza una conversión correcta.</span><span class="sxs-lookup"><span data-stu-id="da933-136">The (**UINT\_PTR**) cast ensures proper conversion.</span></span> <span data-ttu-id="da933-137">En el código siguiente se muestra un ejemplo en el que **SendMessage** devuelve un identificador a un pincel:</span><span class="sxs-lookup"><span data-stu-id="da933-137">The following code shows an example in which **SendMessage** returns a handle to a brush:</span></span>


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



<span data-ttu-id="da933-138">A veces, el parámetro **CreateWindow** y **CreateWindowEx** *HMENU* se usa para pasar un identificador de control de tipo entero (ID).</span><span class="sxs-lookup"><span data-stu-id="da933-138">The **CreateWindow** and **CreateWindowEx** parameter *hmenu* is sometimes used to pass an integer control identifier (ID).</span></span> <span data-ttu-id="da933-139">En este caso, debe convertir el identificador en un tipo **HMENU** :</span><span class="sxs-lookup"><span data-stu-id="da933-139">In this case, you must cast the ID to an **HMENU** type:</span></span>


```C++
HWND hwnd;
int id;

hwnd = CreateWindow(
        TEXT("Button"), TEXT("OK"), BS_PUSHBUTTON,
        x, y, cx, cy, hwndParent,
        (HMENU)id,    // Cast required here
        hinst,
        NULL);
```



## <a name="additional-considerations"></a><span data-ttu-id="da933-140">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="da933-140">Additional Considerations</span></span>

<span data-ttu-id="da933-141">Para sacar el máximo partido de la comprobación **estricta** de tipos, debe seguir instrucciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="da933-141">To get the most benefit from **STRICT** type checking, there are additional guidelines you should follow.</span></span> <span data-ttu-id="da933-142">El código será más portátil en versiones futuras de Windows si realiza los siguientes cambios.</span><span class="sxs-lookup"><span data-stu-id="da933-142">Your code will be more portable in future versions of Windows if you make the following changes.</span></span>

<span data-ttu-id="da933-143">Los tipos **wParam**, **lParam**, **LRESULT** y **LPVOID** son *tipos de datos polimórficos*.</span><span class="sxs-lookup"><span data-stu-id="da933-143">The types **WPARAM**, **LPARAM**, **LRESULT**, and **LPVOID** are *polymorphic data types*.</span></span> <span data-ttu-id="da933-144">Contienen distintos tipos de datos en momentos diferentes, incluso cuando está habilitada la comprobación **estricta** de tipos.</span><span class="sxs-lookup"><span data-stu-id="da933-144">They hold different kinds of data at different times, even when **STRICT** type checking is enabled.</span></span> <span data-ttu-id="da933-145">Para aprovechar las ventajas de la comprobación de tipos, debe convertir los valores de estos tipos lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="da933-145">To get the benefit of type checking, you should cast values of these types as soon as possible.</span></span> <span data-ttu-id="da933-146">(Tenga en cuenta que los atacantes de mensajes reconvierten *wParam* y *lParam* automáticamente de forma portátil).</span><span class="sxs-lookup"><span data-stu-id="da933-146">(Note that message crackers automatically recast *wParam* and *lParam* for you in a portable way.)</span></span>

<span data-ttu-id="da933-147">Tenga especial cuidado para distinguir entre los tipos de **HMODULE** y **hInstance** .</span><span class="sxs-lookup"><span data-stu-id="da933-147">Take special care to distinguish **HMODULE** and **HINSTANCE** types.</span></span> <span data-ttu-id="da933-148">Incluso con **STRICT** Enabled, se definen como el mismo tipo base.</span><span class="sxs-lookup"><span data-stu-id="da933-148">Even with **STRICT** enabled, they are defined as the same base type.</span></span> <span data-ttu-id="da933-149">La mayoría de las funciones de administración de módulos de kernel usan tipos **hInstance** , pero hay algunas funciones que devuelven o aceptan solo tipos **HMODULE** .</span><span class="sxs-lookup"><span data-stu-id="da933-149">Most kernel module management functions use **HINSTANCE** types, but there are a few functions that return or accept only **HMODULE** types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da933-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="da933-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da933-151">Deshabilitar STRICT</span><span class="sxs-lookup"><span data-stu-id="da933-151">Disabling STRICT</span></span>](disabling-strict.md)
</dt> <dt>

[<span data-ttu-id="da933-152">Habilitar STRICT</span><span class="sxs-lookup"><span data-stu-id="da933-152">Enabling STRICT</span></span>](enabling-strict.md)
</dt> </dl>

 

 