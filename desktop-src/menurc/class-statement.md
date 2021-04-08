---
title: CLASS (instrucción)
description: Define la clase del cuadro de diálogo.
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- Menús de instrucciones de clase y otros recursos
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d31eba66a1e4527a24a55a24e4623f3c49dc204
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995188"
---
# <a name="class-statement"></a><span data-ttu-id="38b44-104">CLASS (instrucción)</span><span class="sxs-lookup"><span data-stu-id="38b44-104">CLASS statement</span></span>

<span data-ttu-id="38b44-105">Define la clase del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="38b44-105">Defines the class of the dialog box.</span></span>

<span data-ttu-id="38b44-106">La instrucción de **clase** aparece en la sección opcional antes de la principal de una instrucción de [**cuadro de diálogo**](dialog-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="38b44-106">The **CLASS** statement appears in the optional section before a [**DIALOG**](dialog-resource.md) statement's main.</span></span> <span data-ttu-id="38b44-107">Si no se especifica ninguna clase, se utiliza la clase de cuadro de diálogo estándar.</span><span class="sxs-lookup"><span data-stu-id="38b44-107">If no class is given, the standard dialog class is used.</span></span>

``` syntax
CLASS class
```

<dl> <dt>

<span data-ttu-id="38b44-108"><span id="class"></span><span id="CLASS"></span>*las*</span><span class="sxs-lookup"><span data-stu-id="38b44-108"><span id="class"></span><span id="CLASS"></span>*class*</span></span>
</dt> <dd>

<span data-ttu-id="38b44-109">Entero de 16 bits sin signo o cadena, entre comillas dobles ("), que identifica la clase del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="38b44-109">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="38b44-110">Si el procedimiento de ventana para la clase no procesa un mensaje que se le ha enviado, debe llamar a la función [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) para asegurarse de que todos los mensajes se controlan correctamente para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="38b44-110">If the window procedure for the class does not process a message sent to it, it must call the [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) function to ensure that all messages are handled properly for the dialog box.</span></span> <span data-ttu-id="38b44-111">Una clase privada puede usar **DefDlgProc** como el procedimiento de ventana predeterminado.</span><span class="sxs-lookup"><span data-stu-id="38b44-111">A private class can use **DefDlgProc** as the default window procedure.</span></span> <span data-ttu-id="38b44-112">La clase se debe registrar con el miembro **cbWndExtra** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) establecida en **DLGWINDOWEXTRA**.</span><span class="sxs-lookup"><span data-stu-id="38b44-112">The class must be registered with the **cbWndExtra** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure set to **DLGWINDOWEXTRA**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38b44-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38b44-113">Remarks</span></span>

<span data-ttu-id="38b44-114">La instrucción de **clase** solo se debe utilizar con casos especiales, ya que reemplaza el procesamiento normal de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="38b44-114">The **CLASS** statement should only be used with special cases, because it overrides the normal processing of a dialog box.</span></span> <span data-ttu-id="38b44-115">La instrucción de **clase** convierte un cuadro de diálogo en una ventana de la clase especificada; dependiendo de la clase, esto podría dar resultados no deseados.</span><span class="sxs-lookup"><span data-stu-id="38b44-115">The **CLASS** statement converts a dialog box to a window of the specified class; depending on the class, this could give undesirable results.</span></span> <span data-ttu-id="38b44-116">No use los nombres de clase de control redefinidos con esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="38b44-116">Do not use the redefined control-class names with this statement.</span></span>

## <a name="examples"></a><span data-ttu-id="38b44-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="38b44-117">Examples</span></span>

<span data-ttu-id="38b44-118">En el ejemplo siguiente se muestra el uso de la instrucción de **clase** :</span><span class="sxs-lookup"><span data-stu-id="38b44-118">The following example demonstrates the use of the **CLASS** statement:</span></span>

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a><span data-ttu-id="38b44-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="38b44-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38b44-120">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="38b44-120">**DefDlgProc**</span></span>](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="38b44-121">**DIÁLOGO**</span><span class="sxs-lookup"><span data-stu-id="38b44-121">**DIALOG**</span></span>](dialog-resource.md)
</dt> </dl>

 

 