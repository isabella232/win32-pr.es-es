---
title: Usar el objeto de Active Desktop
description: Este artículo contiene información sobre el objeto ActiveDesktop que forma parte de la API de Shell de Windows. Este objeto, a través de su interfaz IActiveDesktop, permite agregar, quitar y cambiar elementos en el escritorio.
ms.assetid: 68d72b0f-f5e9-4fff-bb13-4c60d1dd7009
keywords:
- Objeto ActiveDesktop
- Active Desktop
- enumeración, elementos de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e61a4a9145386fc4c84a454aa79558b8d5df79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487566"
---
# <a name="using-the-active-desktop-object"></a><span data-ttu-id="a58bc-107">Usar el objeto de Active Desktop</span><span class="sxs-lookup"><span data-stu-id="a58bc-107">Using the Active Desktop Object</span></span>

<span data-ttu-id="a58bc-108">\[Esta característica solo se admite en Windows XP o versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="a58bc-108">\[This feature is supported only under Windows XP or earlier.</span></span> <span data-ttu-id="a58bc-109">\]</span><span class="sxs-lookup"><span data-stu-id="a58bc-109">\]</span></span>

<span data-ttu-id="a58bc-110">Este artículo contiene información sobre el objeto **ActiveDesktop** que forma parte de la API de Shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="a58bc-110">This article contains information on the **ActiveDesktop** object that is part of the Windows Shell API.</span></span> <span data-ttu-id="a58bc-111">Este objeto, a través de su interfaz [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , permite agregar, quitar y cambiar elementos en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="a58bc-111">This object, through its [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface, enables you to add, remove, and change items on the desktop.</span></span>

## <a name="overview-of-the-active-desktop-interface"></a><span data-ttu-id="a58bc-112">Información general de la interfaz de Active Desktop</span><span class="sxs-lookup"><span data-stu-id="a58bc-112">Overview of the Active Desktop Interface</span></span>

-   [<span data-ttu-id="a58bc-113">Acceso a Active Desktop</span><span class="sxs-lookup"><span data-stu-id="a58bc-113">Accessing the Active Desktop</span></span>](#accessing-the-active-desktop)
-   [<span data-ttu-id="a58bc-114">Agregar un elemento de escritorio</span><span class="sxs-lookup"><span data-stu-id="a58bc-114">Adding a Desktop Item</span></span>](#adding-a-desktop-item)
-   [<span data-ttu-id="a58bc-115">Enumerar los elementos del escritorio</span><span class="sxs-lookup"><span data-stu-id="a58bc-115">Enumerating the Desktop Items</span></span>](#enumerating-the-desktop-items)

<span data-ttu-id="a58bc-116">Active Desktop es una característica incluida en Microsoft Internet Explorer 4,0 que permite incluir documentos y elementos HTML (como los controles ActiveX de Microsoft y applets de Java) directamente en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="a58bc-116">The Active Desktop is a feature introduced with Microsoft Internet Explorer 4.0 that enables you to include HTML documents and items (such as Microsoft ActiveX Controls and Java applets) directly to your desktop.</span></span> <span data-ttu-id="a58bc-117">La interfaz [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , que forma parte de la API de Shell de Windows, se usa para agregar, quitar y modificar elementos en el escritorio mediante programación.</span><span class="sxs-lookup"><span data-stu-id="a58bc-117">The [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface, which is part of the Windows Shell API, is used to programmatically add, remove, and modify the items on the desktop.</span></span> <span data-ttu-id="a58bc-118">Los elementos de Active Desktop también se pueden agregar mediante un archivo de formato de definición de canal (CDF).</span><span class="sxs-lookup"><span data-stu-id="a58bc-118">Active Desktop items can also be added using a Channel Definition Format (CDF) file.</span></span>

### <a name="accessing-the-active-desktop"></a><span data-ttu-id="a58bc-119">Acceso a Active Desktop</span><span class="sxs-lookup"><span data-stu-id="a58bc-119">Accessing the Active Desktop</span></span>

<span data-ttu-id="a58bc-120">Para obtener acceso a Active Desktop, una aplicación cliente necesitaría crear una instancia del objeto ActiveDesktop (CLSID \_ ActiveDesktop) con la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y recuperar un puntero a la interfaz [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) del objeto.</span><span class="sxs-lookup"><span data-stu-id="a58bc-120">To access the Active Desktop, a client application would need to create an instance of the ActiveDesktop object (CLSID\_ActiveDesktop) with the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and retrieve a pointer to the object's [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface.</span></span>

<span data-ttu-id="a58bc-121">En el ejemplo siguiente se muestra cómo recuperar un puntero a la interfaz [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .</span><span class="sxs-lookup"><span data-stu-id="a58bc-121">The following sample shows how to retrieve a pointer to the [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface.</span></span>


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

//Insert code to call the IActiveDesktop methods

// Call the Release method
pActiveDesktop->Release();
```



### <a name="adding-a-desktop-item"></a><span data-ttu-id="a58bc-122">Agregar un elemento de escritorio</span><span class="sxs-lookup"><span data-stu-id="a58bc-122">Adding a Desktop Item</span></span>

<span data-ttu-id="a58bc-123">Hay tres métodos que puede usar para agregar un elemento de escritorio: [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop:: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)y [**IActiveDesktop:: AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl).</span><span class="sxs-lookup"><span data-stu-id="a58bc-123">There are three methods you can use to add a desktop item: [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui), and [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl).</span></span> <span data-ttu-id="a58bc-124">Cada elemento de escritorio agregado a Active Desktop debe tener una dirección URL de origen diferente.</span><span class="sxs-lookup"><span data-stu-id="a58bc-124">Each desktop item added to the Active Desktop must have a different source URL.</span></span>

<span data-ttu-id="a58bc-125">Los métodos [**IActiveDesktop:: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) y [**IActiveDesktop:: AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) proporcionan la opción para mostrar las diversas interfaces de usuario que se pueden mostrar antes de agregar un elemento de escritorio al escritorio activo.</span><span class="sxs-lookup"><span data-stu-id="a58bc-125">The [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) and [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) methods both provide the option to display the various user interfaces that can be displayed before adding a desktop item to the Active Desktop.</span></span> <span data-ttu-id="a58bc-126">Las interfaces de comprueban si los usuarios desean agregar el elemento de escritorio a su escritorio activo.</span><span class="sxs-lookup"><span data-stu-id="a58bc-126">The interfaces verify whether users want to add the desktop item to their Active Desktop.</span></span> <span data-ttu-id="a58bc-127">Las interfaces también notifican a los usuarios los riesgos de seguridad que están garantizados por la configuración de la zona de seguridad de la dirección URL y solicitan a los usuarios si desean crear una suscripción para este elemento de escritorio.</span><span class="sxs-lookup"><span data-stu-id="a58bc-127">The interfaces also notify users of any security risks that are warranted by the URL security zone settings, and they ask users if they would like to create a subscription for this desktop item.</span></span> <span data-ttu-id="a58bc-128">Ambos métodos también proporcionan una manera de suprimir las interfaces de usuario.</span><span class="sxs-lookup"><span data-stu-id="a58bc-128">Both methods also provide a way of suppressing the user interfaces.</span></span> <span data-ttu-id="a58bc-129">El método [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) requiere una llamada a [**IActiveDesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) para actualizar el registro.</span><span class="sxs-lookup"><span data-stu-id="a58bc-129">The [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method requires a call to [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) in order to update the registry.</span></span> <span data-ttu-id="a58bc-130">En el caso de **IActiveDesktop:: AddDesktopItemWithUI**, la aplicación cliente debe liberar inmediatamente la interfaz [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) y, a continuación, utilizar la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar una interfaz en una instancia del objeto **ActiveDesktop** que incluye el elemento de escritorio recién agregado.</span><span class="sxs-lookup"><span data-stu-id="a58bc-130">For the **IActiveDesktop::AddDesktopItemWithUI**, the client application must immediately release the [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface and then use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to retrieve an interface to an instance of the **ActiveDesktop** object that includes the newly added desktop item.</span></span>

<span data-ttu-id="a58bc-131">El método [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) agrega el elemento de escritorio especificado al escritorio activo sin ninguna interfaz de usuario, a menos que la configuración de la zona de seguridad de la dirección URL lo impida.</span><span class="sxs-lookup"><span data-stu-id="a58bc-131">The [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method adds the specified desktop item to the Active Desktop without any user interface, unless the URL security zone settings prevent it.</span></span> <span data-ttu-id="a58bc-132">Si la configuración de la zona de seguridad de la dirección URL no permite agregar el elemento de escritorio sin preguntar al usuario, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="a58bc-132">If the URL security zone settings do not allow the desktop item to be added without prompting the user, the method fails.</span></span> <span data-ttu-id="a58bc-133">**IActiveDesktop:: AddDesktopItem** también requiere una llamada a [**IActiveDesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) para actualizar el registro.</span><span class="sxs-lookup"><span data-stu-id="a58bc-133">**IActiveDesktop::AddDesktopItem** also requires a call to [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) in order to update the registry.</span></span>

<span data-ttu-id="a58bc-134">En el ejemplo siguiente se muestra cómo agregar un elemento de escritorio con el método [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) .</span><span class="sxs-lookup"><span data-stu-id="a58bc-134">The following sample demonstrates how to add a desktop item with the [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method.</span></span>


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

// Initialize the COMPONENT structure
compDesktopItem.dwSize = sizeof(COMPONENT);

// Insert code that adds the information about the desktop item 
// to the COMPONENT structure

// Add the desktop item
pActiveDesktop->AddDesktopItem(&compDesktopItem,0);

// Save the changes to the registry
pActiveDesktop->ApplyChanges(AD_APPLY_ALL);
```



### <a name="enumerating-the-desktop-items"></a><span data-ttu-id="a58bc-135">Enumerar los elementos del escritorio</span><span class="sxs-lookup"><span data-stu-id="a58bc-135">Enumerating the Desktop Items</span></span>

<span data-ttu-id="a58bc-136">Para enumerar los elementos de escritorio instalados actualmente en el escritorio activo, la aplicación cliente debe recuperar el número total de elementos de escritorio instalados mediante el método [**IActiveDesktop:: GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) y, a continuación, crear un bucle que recupere la estructura del [**componente**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) para cada elemento de escritorio mediante una llamada al método [**IActiveDesktop:: GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) mediante el uso del índice de elemento de escritorio.</span><span class="sxs-lookup"><span data-stu-id="a58bc-136">To enumerate the desktop items currently installed on the Active Desktop, the client application needs to retrieve the total number of desktop items installed using the [**IActiveDesktop::GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) method and then creating a loop that retrieves the [**COMPONENT**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) structure for each desktop item by calling the [**IActiveDesktop::GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) method using the desktop item index.</span></span>

<span data-ttu-id="a58bc-137">En el ejemplo siguiente se muestra una manera de enumerar los elementos del escritorio.</span><span class="sxs-lookup"><span data-stu-id="a58bc-137">The following sample demonstrates one way to enumerate the desktop items.</span></span>


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;
int intCount;
int intIndex = 0;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

pActiveDesktop->GetDesktopItemCount(&intCount,0);

compDesktopItem.dwSize = sizeof(COMPONENT);

while(intIndex<=(intCount-1))
{
    //get the COMPONENT structure for the current desktop item
    pActiveDesktop->GetDesktopItem(intIndex, &compDesktopItem,0);

    //Insert code that processes the structure

    //Increment the index
    intIndex++;

    //Insert code to clean-up structure for next component
}

// Call the Release method
pActiveDesktop->Release();
```



 

 