---
description: Si decide implementar el borrado en la aplicación que no sea mediante el objeto InkOverlay, puede hacerlo con uno de los dos métodos siguientes.
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: Borrar con el lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9e71828e826f2d57dd21e57934e12c8de0be03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423788"
---
# <a name="erasing-by-using-the-pen"></a><span data-ttu-id="db5e2-103">Borrar con el lápiz</span><span class="sxs-lookup"><span data-stu-id="db5e2-103">Erasing by Using the Pen</span></span>

<span data-ttu-id="db5e2-104">Si decide implementar el borrado en la aplicación que no sea mediante el objeto [**InkOverlay**](inkoverlay-class.md) , puede hacerlo con uno de los dos métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="db5e2-104">If you choose to implement erasing in your application other than by using the [**InkOverlay**](inkoverlay-class.md) object, you can do so by using one of the following two methods.</span></span>

## <a name="using-the-tip-of-the-pen"></a><span data-ttu-id="db5e2-105">Usar la punta del lápiz</span><span class="sxs-lookup"><span data-stu-id="db5e2-105">Using the Tip of the Pen</span></span>

<span data-ttu-id="db5e2-106">La sugerencia del lápiz de Tablet PC se utiliza generalmente para la escritura a mano y para el dibujo. sin embargo, la sugerencia también puede usarse para borrar la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="db5e2-106">The tip of the tablet pen is generally used for handwriting and drawing; however, the tip can also be used to erase ink.</span></span> <span data-ttu-id="db5e2-107">Para ello, la aplicación debe tener un modo de borrado que los usuarios puedan emplear.</span><span class="sxs-lookup"><span data-stu-id="db5e2-107">To do so, the application must have an erase mode that users can employ.</span></span> <span data-ttu-id="db5e2-108">En este modo, use la prueba de posicionamiento para determinar en qué entrada de lápiz se mueve el cursor.</span><span class="sxs-lookup"><span data-stu-id="db5e2-108">In this mode, use hit testing to determine which ink the cursor is moving over.</span></span> <span data-ttu-id="db5e2-109">Puede establecer el modo de borrado para eliminar solo la tinta que el cursor pasa sobre o trazos completos que forman una intersección con la ruta de acceso del cursor, en función de las consideraciones de diseño o funcionales.</span><span class="sxs-lookup"><span data-stu-id="db5e2-109">You can set the erase mode to delete only the ink that the cursor passes over or whole strokes that intersect the path of the cursor, depending upon design or functional considerations.</span></span>

<span data-ttu-id="db5e2-110">Para obtener un ejemplo de cómo usar un modo de borrado para borrar la entrada manuscrita, vea el [ejemplo de borrado de tinta](ink-erasing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="db5e2-110">For an example of how to use an erase mode to erase ink, see the [Ink Erasing Sample](ink-erasing-sample.md).</span></span>

## <a name="using-the-top-of-the-pen"></a><span data-ttu-id="db5e2-111">Usar la parte superior del lápiz</span><span class="sxs-lookup"><span data-stu-id="db5e2-111">Using the Top of the Pen</span></span>

<span data-ttu-id="db5e2-112">Para implementar el borrado con la parte superior del lápiz de Tablet PC, la aplicación debe buscar un cambio en el cursor.</span><span class="sxs-lookup"><span data-stu-id="db5e2-112">To implement erasing with the top of the tablet pen, your application must look for a change in the cursor.</span></span> <span data-ttu-id="db5e2-113">Para buscar el cursor invertido, escuche el evento [**CursorInRange**](inkoverlay-cursorinrange.md) para determinar si el cursor está en el contexto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="db5e2-113">To look for the inverted cursor, listen for the [**CursorInRange**](inkoverlay-cursorinrange.md) event to determine when the cursor is within the context of your application.</span></span> <span data-ttu-id="db5e2-114">Cuando el cursor esté en el intervalo, busque la propiedad [**invertida**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) en el objeto [**cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="db5e2-114">When the cursor is in range, look for the [**Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) property on the [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span> <span data-ttu-id="db5e2-115">Si la propiedad **invertida** es **true**, realice la prueba de posicionamiento para determinar en qué entrada de lápiz se está moviendo el cursor.</span><span class="sxs-lookup"><span data-stu-id="db5e2-115">If the **Inverted** property is **true**, perform hit testing to determine which ink the cursor is moving over.</span></span> <span data-ttu-id="db5e2-116">Borre la tinta o los trazos que forman una intersección con la ruta de acceso del cursor, en función de las consideraciones de diseño o funcionales.</span><span class="sxs-lookup"><span data-stu-id="db5e2-116">Erase either the ink or the strokes that intersect the path of the cursor, depending upon design or functional considerations.</span></span>

<span data-ttu-id="db5e2-117">Para obtener un ejemplo de cómo usar la parte superior del lápiz para borrar la entrada manuscrita, vea el [ejemplo de borrado de tinta](ink-erasing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="db5e2-117">For an example of how to use the top of the pen to erase ink, see the [Ink Erasing Sample](ink-erasing-sample.md).</span></span>

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a><span data-ttu-id="db5e2-118">Determinar si está habilitado el borrado con la parte superior del lápiz</span><span class="sxs-lookup"><span data-stu-id="db5e2-118">Determining if Erasing with the Top of the Pen Is Enabled</span></span>

<span data-ttu-id="db5e2-119">Los usuarios pueden usar la parte superior del lápiz para borrar la entrada manuscrita en aplicaciones diseñadas para Tablet PC, si su hardware determinado lo permite.</span><span class="sxs-lookup"><span data-stu-id="db5e2-119">Users can use the top of the pen to erase ink in applications designed for Tablet PC, if their particular hardware allows for it.</span></span> <span data-ttu-id="db5e2-120">Se tiene acceso a esta funcionalidad mediante una casilla en el cuadro de grupo botones del lápiz de la pestaña Opciones de lápiz del cuadro de diálogo panel de control de configuración de Tablet PC y lápiz.</span><span class="sxs-lookup"><span data-stu-id="db5e2-120">This functionality is accessed by a check box in the Pen buttons group box on the Pen Options tab of the Tablet and Pen Settings control panel dialog.</span></span> <span data-ttu-id="db5e2-121">Para detectar si el usuario ha habilitado el borrado de la parte superior del lápiz, Compruebe la siguiente subclave del registro:</span><span class="sxs-lookup"><span data-stu-id="db5e2-121">To detect if the user has enabled erasing for the top of the pen, check the following registry subkey:</span></span>

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

<span data-ttu-id="db5e2-122">La `EraseEnable` entrada de esta subclave es de tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="db5e2-122">The `EraseEnable` entry of this subkey is of type **REG\_DWORD**.</span></span> <span data-ttu-id="db5e2-123">El valor de esta entrada es 1 para habilitado, o 0 para deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="db5e2-123">The value of this entry is 1 for enabled, or 0 for disabled.</span></span> <span data-ttu-id="db5e2-124">Otros valores se reservan para un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="db5e2-124">Other values are reserved for future use.</span></span>

<span data-ttu-id="db5e2-125">Si la aplicación permite usar la parte superior del lápiz para borrar, debe comprobar y almacenar en caché el valor de la entrada EraseEnable cuando:</span><span class="sxs-lookup"><span data-stu-id="db5e2-125">If your application allows the top of the pen to be used for erasing, you should check and cache the value of the EraseEnable entry when:</span></span>

-   <span data-ttu-id="db5e2-126">Se inicia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="db5e2-126">Your application launches.</span></span>
-   <span data-ttu-id="db5e2-127">Cada vez que la aplicación recibe el foco después de perder el foco.</span><span class="sxs-lookup"><span data-stu-id="db5e2-127">Any time your application receives focus after losing focus.</span></span>

<span data-ttu-id="db5e2-128">Use este valor almacenado en caché para modificar el comportamiento de la aplicación de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="db5e2-128">Use this cached value to modify the behavior of your application appropriately.</span></span>

<span data-ttu-id="db5e2-129">En el siguiente \# ejemplo de C se define un `GetEraseEnabled` método que comprueba el valor de la `EraseEnable` entrada de la `SysEventParameters` subclave.</span><span class="sxs-lookup"><span data-stu-id="db5e2-129">The following C\# example defines a `GetEraseEnabled` method that checks the value of the `EraseEnable` entry of the `SysEventParameters` subkey.</span></span> <span data-ttu-id="db5e2-130">El `GetEraseEnabled` método devuelve **true** si el valor de la entrada es 1; devuelve **false** si el valor de la entrada es 0; o produce una excepción [InvalidOperationException](/dotnet/api/system.invalidoperationexception) si el valor de la entrada es distinto de 1 o 0.</span><span class="sxs-lookup"><span data-stu-id="db5e2-130">The `GetEraseEnabled` method returns **TRUE** if the value of the entry is 1; returns **FALSE** if the value of the entry is 0; or throws an [InvalidOperationException](/dotnet/api/system.invalidoperationexception) exception if the value of the entry is other than 1 or 0.</span></span> <span data-ttu-id="db5e2-131">El `GetEraseEnabled` método devuelve el valor esperado de **true** si la subclave o la entrada no está presente.</span><span class="sxs-lookup"><span data-stu-id="db5e2-131">The `GetEraseEnabled` method returns the expected value of **TRUE** if either the subkey or the entry is not present.</span></span>


```C++
private bool GetEraseEnabled()
{
    // 0 is disabled, 1 is enabled. The default is enabled
    const int Enabled = 1;
    const int Disabled = 0;
    const int DefaultValue = Enabled;

    // Constants for the registry subkey and the entry
    const string Subkey =
                @"SOFTWARE\Microsoft\WISP\PEN\SysEventParameters";
    const string KeyEntry = "EraseEnable";

    // Open the registry subkey.
    Microsoft.Win32.RegistryKey regKey =
        Microsoft.Win32.Registry.CurrentUser.OpenSubKey(Subkey);

    // Retrieve the value of the EraseEnable subkey entry. If either
    // the subkey or the entry does not exist, use the default value.
    object keyValue = (null == regKey) ? DefaultValue :
        regKey.GetValue(KeyEntry,DefaultValue);

    switch((int)keyValue)
    {
        case Enabled:
            // Return true if erasing on pen inversion is enabled. 
            return true;
        case Disabled:
            // Return false if erasing on pen inversion is disabled. 
            return false;
        default:
            // Otherwise, throw an exception. Do not assume this is
            // a Boolean value. Enabled and Disabled are the values
            // defined for this entry at this time. Other values are
            // reserved for future use.
            throw new InvalidOperationException(
                "Unexpected registry subkey value.");
    }
}
```



 

 
