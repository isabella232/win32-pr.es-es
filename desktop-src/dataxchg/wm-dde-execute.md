---
title: Mensaje de WM_DDE_EXECUTE (DDE. h)
description: Una aplicación cliente de Intercambio dinámico de datos (DDE) envía un \_ mensaje de ejecución de WM DDE \_ a una aplicación de servidor DDE para enviar una cadena al servidor que se va a procesar como una serie de comandos.
ms.assetid: 23c18a57-83ee-4fd3-a5bc-71645bda34eb
keywords:
- Intercambio de datos de mensajes de WM_DDE_EXECUTE
topic_type:
- apiref
api_name:
- WM_DDE_EXECUTE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957b5cadcd2383d535aa67258725bafff57ab4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422376"
---
# <a name="wm_dde_execute-message"></a><span data-ttu-id="d615d-104">Mensaje de ejecución de \_ DDE de WM \_</span><span class="sxs-lookup"><span data-stu-id="d615d-104">WM\_DDE\_EXECUTE message</span></span>

<span data-ttu-id="d615d-105">Una aplicación cliente de Intercambio dinámico de datos (DDE) envía un mensaje de **\_ \_ ejecución de WM DDE** a una aplicación de servidor DDE para enviar una cadena al servidor que se va a procesar como una serie de comandos.</span><span class="sxs-lookup"><span data-stu-id="d615d-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_EXECUTE** message to a DDE server application to send a string to the server to be processed as a series of commands.</span></span> <span data-ttu-id="d615d-106">Se espera que la aplicación de servidor publique un mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) en respuesta.</span><span class="sxs-lookup"><span data-stu-id="d615d-106">The server application is expected to post a [**WM\_DDE\_ACK**](wm-dde-ack.md) message in response.</span></span>

<span data-ttu-id="d615d-107">Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="d615d-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_EXECUTE     0x03E8
```



## <a name="parameters"></a><span data-ttu-id="d615d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d615d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d615d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d615d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d615d-110">Identificador de la ventana de cliente que publica el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d615d-110">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="d615d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d615d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d615d-112">Contiene un objeto de memoria global que hace referencia a una cadena de comandos ANSI o Unicode, en función de los tipos de ventanas que participan en la conversación.</span><span class="sxs-lookup"><span data-stu-id="d615d-112">Contains a global memory object that references an ANSI or Unicode command string, depending on the types of windows involved in the conversation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d615d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d615d-113">Remarks</span></span>

<span data-ttu-id="d615d-114">La cadena de comandos es una cadena terminada en null que consta de una o varias cadenas de código de operación entre corchetes ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="d615d-114">The command string is a null-terminated string consisting of one or more opcode strings enclosed in single brackets (\[ \]).</span></span> <span data-ttu-id="d615d-115">Cada cadena de código de operación tiene la sintaxis siguiente, donde la lista de *parámetros* es opcional:</span><span class="sxs-lookup"><span data-stu-id="d615d-115">Each opcode string has the following syntax, where the *parameters* list is optional:</span></span>

<span data-ttu-id="d615d-116">*parámetros de código de operación*</span><span class="sxs-lookup"><span data-stu-id="d615d-116">*opcode parameters*</span></span>

<span data-ttu-id="d615d-117">El *código de operación* es cualquier token único definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d615d-117">The *opcode* is any application-defined single token.</span></span> <span data-ttu-id="d615d-118">No puede incluir espacios, comas, paréntesis, corchetes ni comillas.</span><span class="sxs-lookup"><span data-stu-id="d615d-118">It cannot include spaces, commas, parentheses, brackets, or quotation marks.</span></span>

<span data-ttu-id="d615d-119">La lista de *parámetros* puede contener cualquier valor definido por la aplicación o valores.</span><span class="sxs-lookup"><span data-stu-id="d615d-119">The *parameters* list can contain any application-defined value or values.</span></span> <span data-ttu-id="d615d-120">Varios parámetros se separan mediante comas y la lista completa de parámetros se incluye entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="d615d-120">Multiple parameters are separated by commas, and the entire parameter list is enclosed in parentheses.</span></span> <span data-ttu-id="d615d-121">Los parámetros no pueden incluir comas ni paréntesis, excepto dentro de una cadena entrecomillada.</span><span class="sxs-lookup"><span data-stu-id="d615d-121">Parameters cannot include commas or parentheses except inside a quoted string.</span></span> <span data-ttu-id="d615d-122">Si un corchete o un paréntesis van a aparecer en una cadena entrecomillada, no es necesario doblarlo, como era el caso de las reglas anteriores.</span><span class="sxs-lookup"><span data-stu-id="d615d-122">If a bracket or parenthesis character is to appear in a quoted string, it need not be doubled, as was the case under the old rules.</span></span>

<span data-ttu-id="d615d-123">Las siguientes son cadenas de comandos válidas:</span><span class="sxs-lookup"><span data-stu-id="d615d-123">The following are valid command strings:</span></span>


```
[connect][download(query1,results.txt)][disconnect] 
[query("sales per employee for each district")] 
[open("sample.xlm")][run("r1c1")] 
[quote_case("This is a "" character")] 
[bracket_or_paren_case("()s or []s should be no problem.")] 
```



<span data-ttu-id="d615d-124">Tenga en cuenta que, en las reglas anteriores, los paréntesis y corchetes tenían que doblarse, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="d615d-124">Note that, under the old rules, parentheses and brackets had to be doubled, as follows:</span></span>


```
[bracket_or_paren_case("(())s or [[]]s should be no problem.")] 
```



<span data-ttu-id="d615d-125">Los servidores deben ser capaces de analizar los comandos de cualquier forma.</span><span class="sxs-lookup"><span data-stu-id="d615d-125">Servers should be able to parse commands in either form.</span></span>

<span data-ttu-id="d615d-126">Las cadenas de ejecución Unicode solo deben usarse cuando los identificadores de la ventana de cliente y de servidor hacen que la función [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) devuelva **true**.</span><span class="sxs-lookup"><span data-stu-id="d615d-126">Unicode execute strings should be used only when both the client and server window handles cause the [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) function to return **TRUE**.</span></span>

### <a name="posting"></a><span data-ttu-id="d615d-127">Config</span><span class="sxs-lookup"><span data-stu-id="d615d-127">Posting</span></span>

<span data-ttu-id="d615d-128">La aplicación cliente asigna el objeto de memoria global mediante una llamada a la función [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="d615d-128">The client application allocates the global memory object by calling the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span>

<span data-ttu-id="d615d-129">Al procesar el mensaje de [**\_ \_ confirmación de DDE de WM**](wm-dde-ack.md) que el servidor envía en respuesta a un mensaje de **\_ \_ ejecución de WM DDE** , la aplicación cliente debe eliminar el objeto devuelto por el mensaje de **\_ \_ confirmación de DDE de WM** .</span><span class="sxs-lookup"><span data-stu-id="d615d-129">When processing the [**WM\_DDE\_ACK**](wm-dde-ack.md) message that the server posts in reply to a **WM\_DDE\_EXECUTE** message, the client application must delete the object returned by the **WM\_DDE\_ACK** message.</span></span>

### <a name="receiving"></a><span data-ttu-id="d615d-130">Recepción</span><span class="sxs-lookup"><span data-stu-id="d615d-130">Receiving</span></span>

<span data-ttu-id="d615d-131">La aplicación de servidor envía el mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) para responder de forma positiva o negativa.</span><span class="sxs-lookup"><span data-stu-id="d615d-131">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="d615d-132">El servidor debe volver a usar el objeto de memoria global.</span><span class="sxs-lookup"><span data-stu-id="d615d-132">The server should reuse the global memory object.</span></span>

<span data-ttu-id="d615d-133">A menos que un subprotocolo especifique lo contrario, el servidor no debe exponer el mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) hasta que se completen todas las acciones especificadas por la cadena de comando Execute.</span><span class="sxs-lookup"><span data-stu-id="d615d-133">Unless specified otherwise by a sub-protocol, the server should not post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message until all the actions specified by the execute command string are completed.</span></span> <span data-ttu-id="d615d-134">La única excepción a esta regla es cuando la cadena hace que el servidor finalice la conversación.</span><span class="sxs-lookup"><span data-stu-id="d615d-134">The one exception to this rule is when the string causes the server to terminate the conversation.</span></span>

## <a name="requirements"></a><span data-ttu-id="d615d-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d615d-135">Requirements</span></span>



| <span data-ttu-id="d615d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d615d-136">Requirement</span></span> | <span data-ttu-id="d615d-137">Value</span><span class="sxs-lookup"><span data-stu-id="d615d-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d615d-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d615d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d615d-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d615d-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d615d-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d615d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d615d-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d615d-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d615d-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d615d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d615d-143"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d615d-143"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d615d-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="d615d-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="d615d-145">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d615d-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d615d-146">**IsWindowUnicode**</span><span class="sxs-lookup"><span data-stu-id="d615d-146">**IsWindowUnicode**</span></span>](/windows/desktop/api/winuser/nf-winuser-iswindowunicode)
</dt> <dt>

[<span data-ttu-id="d615d-147">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="d615d-147">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="d615d-148">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="d615d-148">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="d615d-149">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="d615d-149">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="d615d-150">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="d615d-150">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="d615d-151">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="d615d-151">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="d615d-152">**\_confirmación de DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d615d-152">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="d615d-153">**Vista**</span><span class="sxs-lookup"><span data-stu-id="d615d-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d615d-154">Acerca de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="d615d-154">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

