---
title: Cómo procesar la notificación de DTN_WMKEYDOWN
description: En este tema se muestra cómo procesar una \_ notificación de WMKEYDOWN de DTN. El control de este código de notificación permite que el propietario del control proporcione respuestas específicas a las pulsaciones de teclas dentro de los campos de devolución de llamada del control.
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec97ffc5853743c357081b974d155ee0e0977d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103904912"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a><span data-ttu-id="9a555-104">Cómo procesar la notificación de \_ WMKEYDOWN de DTN</span><span class="sxs-lookup"><span data-stu-id="9a555-104">How to Process the DTN\_WMKEYDOWN Notification</span></span>

<span data-ttu-id="9a555-105">En este tema se muestra cómo procesar una notificación de [ \_ WMKEYDOWN de DTN](dtn-wmkeydown.md) .</span><span class="sxs-lookup"><span data-stu-id="9a555-105">This topic demonstrates how to process a [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification.</span></span> <span data-ttu-id="9a555-106">El control de este código de notificación permite que el propietario del control proporcione respuestas específicas a las pulsaciones de teclas dentro de los campos de devolución de llamada del control.</span><span class="sxs-lookup"><span data-stu-id="9a555-106">Handling this notification code allows the owner of the control to provide specific responses to keystrokes within the callback fields of the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="9a555-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="9a555-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="9a555-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="9a555-108">Technologies</span></span>

-   [<span data-ttu-id="9a555-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="9a555-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="9a555-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9a555-110">Prerequisites</span></span>

-   <span data-ttu-id="9a555-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="9a555-111">C/C++</span></span>
-   <span data-ttu-id="9a555-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="9a555-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="9a555-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="9a555-113">Instructions</span></span>


<span data-ttu-id="9a555-114">Los controles de selector de fecha y hora (DTP) envían el mensaje [ \_ WMKEYDOWN de DTN](dtn-wmkeydown.md) para informar de que el usuario ha escrito entradas en un campo de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="9a555-114">Date and time picker (DTP) controls send the [DTN\_WMKEYDOWN](dtn-wmkeydown.md) message to report that the user has typed input in a callback field.</span></span> <span data-ttu-id="9a555-115">Si desea emular las mismas respuestas del teclado que se admiten para los campos de DTP estándar o proporcionar respuestas personalizadas, la aplicación debe incluir código para controlar esta notificación.</span><span class="sxs-lookup"><span data-stu-id="9a555-115">If you want to emulate the same keyboard responses that are supported for standard DTP fields or provide custom responses, your application must include code to handle this notification.</span></span>

<span data-ttu-id="9a555-116">El siguiente ejemplo de código C++ es una función definida por la aplicación que procesa la notificación [ \_ WMKEYDOWN de DTN](dtn-wmkeydown.md) .</span><span class="sxs-lookup"><span data-stu-id="9a555-116">The following C++ code example is an application-defined function that processes the [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification.</span></span>

<span data-ttu-id="9a555-117">**Advertencia de seguridad:** El uso incorrecto de **lstrcmp** puede poner en peligro la seguridad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a555-117">**Security Warning:** Using **lstrcmp** incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="9a555-118">Por ejemplo, antes de llamar a **lstrcmp** en el ejemplo de código siguiente, debe asegurarse de que las dos cadenas terminan en NULL.</span><span class="sxs-lookup"><span data-stu-id="9a555-118">For example, before calling **lstrcmp** in the following code example, you should make sure the two strings are null-terminated.</span></span> <span data-ttu-id="9a555-119">Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="9a555-119">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>



```C++
//  DoWMKeydown increments or decrements the day of month according 
//  to user keyboard input.

void WINAPI DoWMKeydown(
 HWND hwndDP,
 LPNMDATETIMEWMKEYDOWN lpDTKeystroke)
{
    int delta =1;
    if(!lstrcmp(lpDTKeystroke->pszFormat,L"XX")){
        switch(lpDTKeystroke->nVirtKey){
            case VK_DOWN:
            case VK_SUBTRACT:
                delta = -1;  // fall through

            case VK_UP:
            case VK_ADD:
                lpDTKeystroke->st.wDay += (WORD) delta;
                break;
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="9a555-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a555-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a555-121">Usar controles de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="9a555-121">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="9a555-122">Referencia de control de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="9a555-122">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="9a555-123">Selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="9a555-123">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




