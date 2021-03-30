---
description: Explica cómo crear un control de entrada matemática.
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: Crear un control de entrada matemática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5084f29943395bc6781fe20598f86bdc08c6c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553304"
---
# <a name="creating-a-math-input-control"></a><span data-ttu-id="2ca1b-103">Crear un control de entrada matemática</span><span class="sxs-lookup"><span data-stu-id="2ca1b-103">Creating a Math Input Control</span></span>

<span data-ttu-id="2ca1b-104">Para crear el control de entrada matemática, debe:</span><span class="sxs-lookup"><span data-stu-id="2ca1b-104">To create the math input control, you must:</span></span>

-   [<span data-ttu-id="2ca1b-105">Incluir encabezados y bibliotecas para el control de entrada matemática</span><span class="sxs-lookup"><span data-stu-id="2ca1b-105">Include Headers and Libraries for the Math Input Control</span></span>](#include-headers-and-libraries-for-the-math-input-control)
-   [<span data-ttu-id="2ca1b-106">Declare el puntero de control y llame a CoInitialize en el puntero de control</span><span class="sxs-lookup"><span data-stu-id="2ca1b-106">Declare the Control Pointer and Call CoInitialize on the Control Pointer</span></span>](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [<span data-ttu-id="2ca1b-107">Mostrar el control</span><span class="sxs-lookup"><span data-stu-id="2ca1b-107">Show the Control</span></span>](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a><span data-ttu-id="2ca1b-108">Incluir encabezados y bibliotecas para el control de entrada matemática</span><span class="sxs-lookup"><span data-stu-id="2ca1b-108">Include Headers and Libraries for the Math Input Control</span></span>

<span data-ttu-id="2ca1b-109">El código siguiente debe colocarse en la parte superior del código donde se va a usar el control de entrada matemática.</span><span class="sxs-lookup"><span data-stu-id="2ca1b-109">The following code should be placed at the top of your code where you will be using the math input control.</span></span>


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



<span data-ttu-id="2ca1b-110">Este código agregará compatibilidad para el control de entrada matemática a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ca1b-110">This code will add support for the math input control to your application.</span></span>

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a><span data-ttu-id="2ca1b-111">Declare el puntero de control y llame a CoInitialize en el puntero de control</span><span class="sxs-lookup"><span data-stu-id="2ca1b-111">Declare the Control Pointer and Call CoInitialize on the Control Pointer</span></span>

<span data-ttu-id="2ca1b-112">Una vez incluidos los encabezados para el control, puede declarar el puntero de control y puede llamar a CoInitialize en él para crear un identificador de la interfaz de control de entrada matemática.</span><span class="sxs-lookup"><span data-stu-id="2ca1b-112">After you have included the headers for your control, you can declare the control pointer and can call CoInitialize on it to create a handle to the math input control interface.</span></span> <span data-ttu-id="2ca1b-113">El siguiente código se puede colocar en una clase o como una variable global en la implementación de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="2ca1b-113">The following code can be placed in a class or as a global variable in your application's implementation:</span></span>


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



<span data-ttu-id="2ca1b-114">En el código siguiente se muestra cómo se puede llamar a CoInitialize en el puntero de control.</span><span class="sxs-lookup"><span data-stu-id="2ca1b-114">The following code shows how you can call CoInitialize on the control pointer.</span></span>


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



<span data-ttu-id="2ca1b-115">Después de llamar a CoInitialize en el puntero de control, tiene una referencia al control y puede tener acceso a los métodos del control.</span><span class="sxs-lookup"><span data-stu-id="2ca1b-115">After calling CoInitialize on the control pointer, you have a reference to the control and can access the control's methods.</span></span> <span data-ttu-id="2ca1b-116">Por ejemplo, podría habilitar el conjunto extendido de controles tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="2ca1b-116">For example, you could enable the extended set of controls as shown in the following example.</span></span>


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a><span data-ttu-id="2ca1b-117">Mostrar el control</span><span class="sxs-lookup"><span data-stu-id="2ca1b-117">Show the Control</span></span>

<span data-ttu-id="2ca1b-118">El control no aparecerá automáticamente después de crearlo.</span><span class="sxs-lookup"><span data-stu-id="2ca1b-118">The control will not automatically appear after you create it.</span></span> <span data-ttu-id="2ca1b-119">Para mostrar el control, llame al método [**Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) en la referencia de control que creó en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="2ca1b-119">To show the control, call the [**Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) method on the control reference that you created in the previous step.</span></span> <span data-ttu-id="2ca1b-120">En el código siguiente se muestra cómo se puede llamar al método [**Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) .</span><span class="sxs-lookup"><span data-stu-id="2ca1b-120">The following code demonstrates how the [**Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) method can be called.</span></span>


```
   hr = g_spMIC->Show();
   
```



<span data-ttu-id="2ca1b-121">Una vez que se muestre el control, tendrá un aspecto similar al de la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="2ca1b-121">After the control shows, it will look something like the following illustration.</span></span>

![captura de pantalla que muestra el control de entrada matemática](images/mic.png)

<span data-ttu-id="2ca1b-123">Tenga en cuenta que he habilitado el conjunto extendido de botones para que las operaciones de **rehacer** y **Deshacer** estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="2ca1b-123">Note that I have enabled the extended set of buttons so that **Redo** and **Undo** are available.</span></span>

 

 
