---
title: Cómo admitir elementos de devolución de llamada
description: En este tema se muestra cómo proporcionar compatibilidad para los elementos de devolución de llamada.
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056f64c086aeda94ccf928d93ae2c5db5e2187a4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995742"
---
# <a name="how-to-support-callback-items"></a><span data-ttu-id="c980b-103">Cómo admitir elementos de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="c980b-103">How to Support Callback Items</span></span>

<span data-ttu-id="c980b-104">En este tema se muestra cómo proporcionar compatibilidad para los elementos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="c980b-104">This topic demonstrates how to provide support for callback items.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c980b-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="c980b-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c980b-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="c980b-106">Technologies</span></span>

-   [<span data-ttu-id="c980b-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="c980b-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c980b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c980b-108">Prerequisites</span></span>

-   <span data-ttu-id="c980b-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="c980b-109">C/C++</span></span>
-   <span data-ttu-id="c980b-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="c980b-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c980b-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="c980b-111">Instructions</span></span>


<span data-ttu-id="c980b-112">Si la aplicación va a utilizar elementos de devolución de llamada en un control ComboBoxEx, debe estar preparado para controlar el código de notificación [CBEN \_ GETDISPINFO](cben-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c980b-112">If your application is going to use callback items in a ComboBoxEx control, it must be prepared to handle the [CBEN\_GETDISPINFO](cben-getdispinfo.md) notification code.</span></span> <span data-ttu-id="c980b-113">Un control ComboBoxEx envía esta notificación cada vez que necesita que el propietario proporcione información específica del elemento.</span><span class="sxs-lookup"><span data-stu-id="c980b-113">A ComboBoxEx control sends this notification whenever it needs the owner to provide specific item information.</span></span> <span data-ttu-id="c980b-114">Para obtener más información sobre los elementos de devolución de llamada, vea [elementos de devolución de llamada](comboboxex-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c980b-114">For more information about callback items, see [Callback Items](comboboxex-controls.md).</span></span>

<span data-ttu-id="c980b-115">La siguiente función definida por la aplicación procesa [CBEN \_ GETDISPINFO](cben-getdispinfo.md) proporcionando atributos para un elemento determinado.</span><span class="sxs-lookup"><span data-stu-id="c980b-115">The following application-defined function processes [CBEN\_GETDISPINFO](cben-getdispinfo.md) by providing attributes for a given item.</span></span> <span data-ttu-id="c980b-116">Tenga en cuenta que establece el miembro de **máscara** de la estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) entrante en CBEIF \_ di \_ SETITEM.</span><span class="sxs-lookup"><span data-stu-id="c980b-116">Note that it sets the **mask** member of the incoming [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure to CBEIF\_DI\_SETITEM.</span></span> <span data-ttu-id="c980b-117">Si se establece **Mask** en este valor, el control conserva la información del elemento para que no sea necesario volver a solicitar la información.</span><span class="sxs-lookup"><span data-stu-id="c980b-117">Setting **mask** to this value makes the control retain the item information so that it will not need to request the information again.</span></span>

## <a name="complete-example"></a><span data-ttu-id="c980b-118">Ejemplo completo</span><span class="sxs-lookup"><span data-stu-id="c980b-118">Complete example</span></span>


```C++
// DoItemCallback - Processes CBEN_GETDISPINFO by providing item
// attributes for a given callback item.

void WINAPI DoItemCallback(PNMCOMBOBOXEX pNMCBex)
{
    DWORD dwMask = pNMCBex->ceItem.mask;

    if(dwMask & CBEIF_TEXT)
    {
            // Insert code to provide item text.
    }

    if(dwMask & CBEIF_IMAGE) 
    {
        // Insert code to provide an item image index.
    }

    // Insert code to provide other callback information as desired.

    // Make the ComboBoxEx control hold onto the item information.
    pNMCBex->ceItem.mask = CBEIF_DI_SETITEM;
}
```



## <a name="related-topics"></a><span data-ttu-id="c980b-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c980b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c980b-120">Acerca de los controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="c980b-120">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="c980b-121">Referencia de control ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="c980b-121">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="c980b-122">Usar controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="c980b-122">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="c980b-123">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="c980b-123">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 