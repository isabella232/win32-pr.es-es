---
title: Recurso de ACELERAdores
description: Define uno o varios aceleradores para una aplicación. Un acelerador es una pulsación de tecla definida por la aplicación para proporcionar al usuario una forma rápida de realizar una tarea.
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- Menús de recursos de ACELERAdores y otros recursos
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aeb09ca52438f7b2f4903e5403eeb722e5d7d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533136"
---
# <a name="accelerators-resource"></a><span data-ttu-id="26f36-105">Recurso de ACELERAdores</span><span class="sxs-lookup"><span data-stu-id="26f36-105">ACCELERATORS resource</span></span>

<span data-ttu-id="26f36-106">Define uno o varios aceleradores para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="26f36-106">Defines one or more accelerators for an application.</span></span> <span data-ttu-id="26f36-107">Un acelerador es una pulsación de tecla definida por la aplicación para proporcionar al usuario una forma rápida de realizar una tarea.</span><span class="sxs-lookup"><span data-stu-id="26f36-107">An accelerator is a keystroke defined by the application to give the user a quick way to perform a task.</span></span>

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a><span data-ttu-id="26f36-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26f36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f36-109"><span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*</span><span class="sxs-lookup"><span data-stu-id="26f36-109"><span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*</span></span>
</dt> <dd>

<span data-ttu-id="26f36-110">Nombre único o un valor entero sin signo de 16 bits que identifica el recurso.</span><span class="sxs-lookup"><span data-stu-id="26f36-110">Unique name or a 16-bit unsigned integer value that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="26f36-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instrucciones opcionales*</span><span class="sxs-lookup"><span data-stu-id="26f36-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="26f36-112">Cero o más de las instrucciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="26f36-112">Zero or more of the following statements.</span></span>



| <span data-ttu-id="26f36-113">.</span><span class="sxs-lookup"><span data-stu-id="26f36-113">Statement</span></span>                                                        | <span data-ttu-id="26f36-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="26f36-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f36-115">[**Características**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="26f36-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="26f36-116">Información definida por el usuario sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="26f36-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="26f36-117">Para obtener más información, vea [**características**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="26f36-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="26f36-118">[](language-statement.md) *Idioma* del idioma, *subidioma*</span><span class="sxs-lookup"><span data-stu-id="26f36-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="26f36-119">Especifica el idioma del recurso.</span><span class="sxs-lookup"><span data-stu-id="26f36-119">Specifies the language for the resource.</span></span> <span data-ttu-id="26f36-120">Para obtener más información, vea [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="26f36-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                              |
| <span data-ttu-id="26f36-121">[**Versión**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="26f36-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="26f36-122">Número de versión definido por el usuario para el recurso que pueden usar las herramientas que leen y escriben archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="26f36-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="26f36-123">Para obtener más información, vea [**versión**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="26f36-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="26f36-124"><span id="event"></span><span id="EVENT"></span>*ceso*</span><span class="sxs-lookup"><span data-stu-id="26f36-124"><span id="event"></span><span id="EVENT"></span>*event*</span></span>
</dt> <dd>

<span data-ttu-id="26f36-125">Pulsación de tecla que se va a usar como acelerador.</span><span class="sxs-lookup"><span data-stu-id="26f36-125">Keystroke to be used as an accelerator.</span></span> <span data-ttu-id="26f36-126">Puede ser cualquiera de los siguientes tipos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="26f36-126">It can be any one of the following character types.</span></span>



| <span data-ttu-id="26f36-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="26f36-127">Type</span></span>                    | <span data-ttu-id="26f36-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="26f36-128">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f36-129">"*Char*"</span><span class="sxs-lookup"><span data-stu-id="26f36-129">"*char*"</span></span>                | <span data-ttu-id="26f36-130">Un solo carácter entre comillas dobles (").</span><span class="sxs-lookup"><span data-stu-id="26f36-130">A single character enclosed in double quotation marks (").</span></span> <span data-ttu-id="26f36-131">El carácter puede ir precedido de un símbolo de intercalación (^), lo que significa que el carácter es un carácter de control.</span><span class="sxs-lookup"><span data-stu-id="26f36-131">The character can be preceded by a caret (^), meaning that the character is a control character.</span></span>                                                                                  |
| <span data-ttu-id="26f36-132">*Carácter*</span><span class="sxs-lookup"><span data-stu-id="26f36-132">*Character*</span></span>             | <span data-ttu-id="26f36-133">Valor entero que representa un carácter.</span><span class="sxs-lookup"><span data-stu-id="26f36-133">An integer value representing a character.</span></span> <span data-ttu-id="26f36-134">El parámetro de *tipo* debe ser **ASCII**.</span><span class="sxs-lookup"><span data-stu-id="26f36-134">The *type* parameter must be **ASCII**.</span></span>                                                                                                                                                           |
| <span data-ttu-id="26f36-135">*carácter de clave virtual*</span><span class="sxs-lookup"><span data-stu-id="26f36-135">*virtual-key character*</span></span> | <span data-ttu-id="26f36-136">Un valor entero que representa una clave virtual.</span><span class="sxs-lookup"><span data-stu-id="26f36-136">An integer value representing a virtual key.</span></span> <span data-ttu-id="26f36-137">La clave virtual de las claves alfanuméricas se puede especificar colocando la letra mayúscula o el número entre comillas dobles (por ejemplo, "9" o "C").</span><span class="sxs-lookup"><span data-stu-id="26f36-137">The virtual key for alphanumeric keys can be specified by placing the uppercase letter or number in double quotation marks (for example, "9" or "C").</span></span> <span data-ttu-id="26f36-138">El parámetro de *tipo* debe ser **VIRTKEY**.</span><span class="sxs-lookup"><span data-stu-id="26f36-138">The *type* parameter must be **VIRTKEY**.</span></span> |



 

</dd> <dt>

<span data-ttu-id="26f36-139"><span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*</span><span class="sxs-lookup"><span data-stu-id="26f36-139"><span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*</span></span>
</dt> <dd>

<span data-ttu-id="26f36-140">valor entero sin signo de 16 bits que identifica el acelerador.</span><span class="sxs-lookup"><span data-stu-id="26f36-140">a 16-bit unsigned integer value that identifies the accelerator.</span></span>

</dd> <dt>

<span data-ttu-id="26f36-141"><span id="type"></span><span id="TYPE"></span>*automáticamente*</span><span class="sxs-lookup"><span data-stu-id="26f36-141"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="26f36-142">Solo se requiere cuando el parámetro de *evento* es un *carácter o un* *carácter de tecla virtual*.</span><span class="sxs-lookup"><span data-stu-id="26f36-142">Required only when the *event* parameter is a *character* or a *virtual-key character*.</span></span> <span data-ttu-id="26f36-143">El parámetro de *tipo* especifica **ASCII** o **VIRTKEY**; el valor entero del *evento* se interpreta en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="26f36-143">The *type* parameter specifies either **ASCII** or **VIRTKEY**; the integer value of *event* is interpreted accordingly.</span></span> <span data-ttu-id="26f36-144">Cuando se especifica **VIRTKEY** y el *evento* contiene una cadena, el *evento* debe estar en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="26f36-144">When **VIRTKEY** is specified and *event* contains a string, *event* must be uppercase.</span></span>

</dd> <dt>

<span data-ttu-id="26f36-145"><span id="options"></span><span id="OPTIONS"></span>*Opciones*</span><span class="sxs-lookup"><span data-stu-id="26f36-145"><span id="options"></span><span id="OPTIONS"></span>*options*</span></span>
</dt> <dd>

<span data-ttu-id="26f36-146">opciones que definen el acelerador.</span><span class="sxs-lookup"><span data-stu-id="26f36-146">options that define the accelerator.</span></span> <span data-ttu-id="26f36-147">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="26f36-147">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="26f36-148">Opción</span><span class="sxs-lookup"><span data-stu-id="26f36-148">Option</span></span>                             | <span data-ttu-id="26f36-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="26f36-149">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f36-150">**Noinvertir**</span><span class="sxs-lookup"><span data-stu-id="26f36-150">**NOINVERT**</span></span>                       | <span data-ttu-id="26f36-151">Especifica que no se resalta ningún elemento de menú de nivel superior cuando se utiliza el acelerador.</span><span class="sxs-lookup"><span data-stu-id="26f36-151">Specifies that no top-level menu item is highlighted when the accelerator is used.</span></span> <span data-ttu-id="26f36-152">Esto resulta útil al definir aceleradores para acciones como el desplazamiento que no se corresponden con un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="26f36-152">This is useful when defining accelerators for actions such as scrolling that do not correspond to a menu item.</span></span> <span data-ttu-id="26f36-153">Si se omite **Revert** , se resaltará un elemento de menú de nivel superior (si es posible) cuando se use el acelerador.</span><span class="sxs-lookup"><span data-stu-id="26f36-153">If **NOINVERT** is omitted, a top-level menu item will be highlighted (if possible) when the accelerator is used.</span></span> <span data-ttu-id="26f36-154">Este atributo está obsoleto y solo se conserva por compatibilidad con versiones anteriores de los archivos de recursos diseñados para Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="26f36-154">This attribute is obsolete and retained only for backward compatibility with resource files designed for 16-bit Windows.</span></span> |
| <span data-ttu-id="26f36-155">**ALTERNATIVA**</span><span class="sxs-lookup"><span data-stu-id="26f36-155">**ALT**</span></span>                            | <span data-ttu-id="26f36-156">Hace que el acelerador se active solo si la tecla ALT está presionada.</span><span class="sxs-lookup"><span data-stu-id="26f36-156">Causes the accelerator to be activated only if the ALT key is down.</span></span> <span data-ttu-id="26f36-157">Solo se aplica a las claves virtuales.</span><span class="sxs-lookup"><span data-stu-id="26f36-157">Applies only to virtual keys.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="26f36-158">**MOVER**</span><span class="sxs-lookup"><span data-stu-id="26f36-158">**SHIFT**</span></span>                          | <span data-ttu-id="26f36-159">Hace que el acelerador se active solo si la tecla Mayús está presionada.</span><span class="sxs-lookup"><span data-stu-id="26f36-159">Causes the accelerator to be activated only if the SHIFT key is down.</span></span> <span data-ttu-id="26f36-160">Solo se aplica a las claves virtuales</span><span class="sxs-lookup"><span data-stu-id="26f36-160">Applies only to virtual keys</span></span>                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="26f36-161">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="26f36-161">**CONTROL**</span></span>](control-control.md) | <span data-ttu-id="26f36-162">Define el carácter como un carácter de control (el acelerador solo se activa si la tecla CONTROL está inactiva).</span><span class="sxs-lookup"><span data-stu-id="26f36-162">Defines the character as a control character (the accelerator is only activated if the CONTROL key is down).</span></span> <span data-ttu-id="26f36-163">Esto tiene el mismo efecto que el uso de un símbolo de intercalación (^) antes del carácter de acelerador en el parámetro de *evento* .</span><span class="sxs-lookup"><span data-stu-id="26f36-163">This has the same effect as using a caret (^) before the accelerator character in the *event* parameter.</span></span> <span data-ttu-id="26f36-164">Solo se aplica a las claves virtuales</span><span class="sxs-lookup"><span data-stu-id="26f36-164">Applies only to virtual keys</span></span>                                                                                                                                                                                           |



 

</dd> </dl>

<span data-ttu-id="26f36-165">Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="26f36-165">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="26f36-166">Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="26f36-166">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26f36-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26f36-167">Remarks</span></span>

<span data-ttu-id="26f36-168">La función [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) se usa para convertir los mensajes de acelerador de la cola de la aplicación en [**mensajes de WM o de \_**](./wm-command.md) [**WM \_ SYSCOMMAND**](./wm-syscommand.md) .</span><span class="sxs-lookup"><span data-stu-id="26f36-168">The [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) function is used to translate accelerator messages from the application queue into [**WM\_COMMAND**](./wm-command.md) or [**WM\_SYSCOMMAND**](./wm-syscommand.md) messages.</span></span>

## <a name="examples"></a><span data-ttu-id="26f36-169">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="26f36-169">Examples</span></span>

<span data-ttu-id="26f36-170">En el siguiente ejemplo se muestra el uso de las teclas de aceleración.</span><span class="sxs-lookup"><span data-stu-id="26f36-170">The following example demonstrates the use of accelerator keys.</span></span>

``` syntax
1 ACCELERATORS
{
  "^C",  IDDCLEAR         ; control C
  "K",   IDDCLEAR         ; shift K
  "k",   IDDELLIPSE, ALT  ; alt k
  98,    IDDRECT, ASCII   ; b
  66,    IDDSTAR, ASCII   ; B (shift b)
  "g",   IDDRECT          ; g
  "G",   IDDSTAR          ; G (shift G)
  VK_F1, IDDCLEAR, VIRTKEY                ; F1
  VK_F1, IDDSTAR, CONTROL, VIRTKEY        ; control F1
  VK_F1, IDDELLIPSE, SHIFT, VIRTKEY       ; shift F1
  VK_F1, IDDRECT, ALT, VIRTKEY            ; alt F1
  VK_F2, IDDCLEAR, ALT, SHIFT, VIRTKEY    ; alt shift F2
  VK_F2, IDDSTAR, CONTROL, SHIFT, VIRTKEY ; ctrl shift F2
  VK_F2, IDDRECT, ALT, CONTROL, VIRTKEY   ; alt control F2
}
```

## <a name="see-also"></a><span data-ttu-id="26f36-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="26f36-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f36-172">Usar aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="26f36-172">Using Keyboard Accelerators</span></span>](./using-keyboard-accelerators.md)
</dt> <dt>

[<span data-ttu-id="26f36-173">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="26f36-173">**TranslateAccelerator**</span></span>](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="26f36-174">**SUS**</span><span class="sxs-lookup"><span data-stu-id="26f36-174">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="26f36-175">**DIÁLOGO**</span><span class="sxs-lookup"><span data-stu-id="26f36-175">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="26f36-176">**MÓDULO**</span><span class="sxs-lookup"><span data-stu-id="26f36-176">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="26f36-177">**MENU**</span><span class="sxs-lookup"><span data-stu-id="26f36-177">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="26f36-178">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="26f36-178">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="26f36-179">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="26f36-179">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="26f36-180">**Versión**</span><span class="sxs-lookup"><span data-stu-id="26f36-180">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 