---
title: Parámetros de control comunes
description: A continuación se describe la sintaxis general de una instrucción de definición de recursos de control.
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261c71163276ed39841d6f6d7e125d4eb5420072
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358900"
---
# <a name="common-control-parameters"></a><span data-ttu-id="11add-103">Parámetros de control comunes</span><span class="sxs-lookup"><span data-stu-id="11add-103">Common Control Parameters</span></span>

<span data-ttu-id="11add-104">A continuación se describe la sintaxis general de una instrucción de definición de recursos de control.</span><span class="sxs-lookup"><span data-stu-id="11add-104">The following describes the general syntax for a control resource-definition statement.</span></span> <span data-ttu-id="11add-105">A continuación se proporciona el significado de cada parámetro.</span><span class="sxs-lookup"><span data-stu-id="11add-105">The meaning of each parameter is given below.</span></span> <span data-ttu-id="11add-106">En ocasiones, una instrucción usará un parámetro de manera diferente o puede omitir un parámetro.</span><span class="sxs-lookup"><span data-stu-id="11add-106">Occasionally, a statement will use a parameter differently, or may ignore a parameter.</span></span> <span data-ttu-id="11add-107">La variación específica de la instrucción se describe en la documentación de la instrucción.</span><span class="sxs-lookup"><span data-stu-id="11add-107">The statement-specific variation is described in the documentation for the statement.</span></span>

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span data-ttu-id="11add-108"><span id="text"></span><span id="TEXT"></span>*negrita*</span><span class="sxs-lookup"><span data-stu-id="11add-108"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="11add-109">Texto que se va a mostrar con el control.</span><span class="sxs-lookup"><span data-stu-id="11add-109">Text that is to be displayed with the control.</span></span> <span data-ttu-id="11add-110">El texto se coloca dentro del control o junto al control.</span><span class="sxs-lookup"><span data-stu-id="11add-110">The text is positioned within the control or adjacent to the control.</span></span>

<span data-ttu-id="11add-111">Este parámetro debe contener cero o más caracteres entre comillas dobles (").</span><span class="sxs-lookup"><span data-stu-id="11add-111">This parameter must contain zero or more characters enclosed in double quotation marks (").</span></span> <span data-ttu-id="11add-112">Las cadenas terminan automáticamente en NULL y se convierten en Unicode en el archivo de recursos resultante.</span><span class="sxs-lookup"><span data-stu-id="11add-112">Strings are automatically null-terminated and converted to Unicode in the resulting resource file.</span></span>

<span data-ttu-id="11add-113">De forma predeterminada, los caracteres enumerados entre comillas dobles son caracteres ANSI y las secuencias de escape se interpretan como secuencias de escape de bytes.</span><span class="sxs-lookup"><span data-stu-id="11add-113">By default, the characters listed between the double quotation marks are ANSI characters, and escape sequences are interpreted as byte escape sequences.</span></span> <span data-ttu-id="11add-114">Si la cadena está precedida por el prefijo "L", la cadena es una cadena de caracteres anchos y las secuencias de escape se interpretan como secuencias de escape de 2 bytes que especifican caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="11add-114">If the string is preceded by the "L" prefix, the string is a wide-character string and escape sequences are interpreted as 2-byte escape sequences that specify Unicode characters.</span></span> <span data-ttu-id="11add-115">Si se requiere una comilla doble en el texto, debe incluir las comillas dobles dos veces.</span><span class="sxs-lookup"><span data-stu-id="11add-115">If a double quotation mark is required in the text, you must include the double quotation mark twice.</span></span>

<span data-ttu-id="11add-116">Un carácter de y comercial (&) en el texto indica que el siguiente carácter se utiliza como carácter de tecla de mnemotécnico para el control.</span><span class="sxs-lookup"><span data-stu-id="11add-116">An ampersand (&) character in the text indicates that the following character is used as a mnemonic character for the control.</span></span> <span data-ttu-id="11add-117">Cuando se muestra el control, no se muestra el símbolo de y comercial, pero el carácter de la tecla de tecla está subrayado.</span><span class="sxs-lookup"><span data-stu-id="11add-117">When the control is displayed, the ampersand is not shown, but the mnemonic character is underlined.</span></span> <span data-ttu-id="11add-118">El usuario puede elegir el control presionando la tecla correspondiente al carácter mnemotécnico subrayado.</span><span class="sxs-lookup"><span data-stu-id="11add-118">The user can choose the control by pressing the key corresponding to the underlined mnemonic character.</span></span> <span data-ttu-id="11add-119">Para usar la y comercial como carácter en una cadena, inserte dos símbolos de y comercial (&&).</span><span class="sxs-lookup"><span data-stu-id="11add-119">To use the ampersand as a character in a string, insert two ampersands (&&).</span></span>

</dd> <dt>

<span data-ttu-id="11add-120"><span id="id"></span><span id="ID"></span>*sesión*</span><span class="sxs-lookup"><span data-stu-id="11add-120"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="11add-121">Identificador de control.</span><span class="sxs-lookup"><span data-stu-id="11add-121">Control identifier.</span></span> <span data-ttu-id="11add-122">Este valor debe ser un entero sin signo de 16 bits en el intervalo comprendido entre 0 y 65.535 o una expresión aritmética simple que se evalúe como un valor de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="11add-122">This value must be a 16-bit unsigned integer in the range 0 through 65,535 or a simple arithmetic expression that evaluates to a value in that range.</span></span>

</dd> <dt>

<span data-ttu-id="11add-123"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="11add-123"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="11add-124">Coordenada X del lado izquierdo del control en relación con el lado izquierdo del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="11add-124">X-coordinate of the left side of the control relative to the left side of the dialog box.</span></span> <span data-ttu-id="11add-125">Este valor debe ser un entero sin signo de 16 bits en el intervalo comprendido entre 0 y 65.535.</span><span class="sxs-lookup"><span data-stu-id="11add-125">This value must be a 16-bit unsigned integer in the range 0 through 65,535.</span></span> <span data-ttu-id="11add-126">La coordenada está en unidades de cuadro de diálogo y es relativa al origen del cuadro de diálogo, ventana o control que contiene el control especificado.</span><span class="sxs-lookup"><span data-stu-id="11add-126">The coordinate is in dialog units and is relative to the origin of the dialog box, window, or control containing the specified control.</span></span>

</dd> <dt>

<span data-ttu-id="11add-127"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="11add-127"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="11add-128">Coordenada Y del lado superior del control en relación con la parte superior del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="11add-128">Y-coordinate of the top side of the control relative to the top of the dialog box.</span></span> <span data-ttu-id="11add-129">Este valor debe ser un entero sin signo de 16 bits en el intervalo comprendido entre 0 y 65.535.</span><span class="sxs-lookup"><span data-stu-id="11add-129">This value must be a 16-bit unsigned integer in the range 0 through 65,535.</span></span> <span data-ttu-id="11add-130">La coordenada está en unidades de diálogo relativas al origen del cuadro de diálogo, ventana o control que contiene el control especificado.</span><span class="sxs-lookup"><span data-stu-id="11add-130">The coordinate is in dialog units relative to the origin of the dialog box, window, or control containing the specified control.</span></span>

</dd> <dt>

<span data-ttu-id="11add-131"><span id="width"></span><span id="WIDTH"></span>*Ancho*</span><span class="sxs-lookup"><span data-stu-id="11add-131"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="11add-132">Ancho del control.</span><span class="sxs-lookup"><span data-stu-id="11add-132">Width of the control.</span></span> <span data-ttu-id="11add-133">Este valor debe ser un entero sin signo de 16 bits en el intervalo comprendido entre 1 y 65.535.</span><span class="sxs-lookup"><span data-stu-id="11add-133">This value must be a 16-bit unsigned integer in the range 1 through 65,535.</span></span> <span data-ttu-id="11add-134">El ancho está en unidades de 1/4 caracteres.</span><span class="sxs-lookup"><span data-stu-id="11add-134">The width is in 1/4-character units.</span></span>

</dd> <dt>

<span data-ttu-id="11add-135"><span id="height"></span><span id="HEIGHT"></span>*alto*</span><span class="sxs-lookup"><span data-stu-id="11add-135"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="11add-136">Alto del control.</span><span class="sxs-lookup"><span data-stu-id="11add-136">Height of the control.</span></span> <span data-ttu-id="11add-137">Este valor debe ser un entero sin signo de 16 bits en el intervalo comprendido entre 1 y 65.535.</span><span class="sxs-lookup"><span data-stu-id="11add-137">This value must be a 16-bit unsigned integer in the range 1 through 65,535.</span></span> <span data-ttu-id="11add-138">El alto está en unidades de 1/8 caracteres.</span><span class="sxs-lookup"><span data-stu-id="11add-138">The height is in 1/8-character units.</span></span>

</dd> <dt>

<span data-ttu-id="11add-139"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="11add-139"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="11add-140">Estilos de control.</span><span class="sxs-lookup"><span data-stu-id="11add-140">Control styles.</span></span> <span data-ttu-id="11add-141">Use el operador OR bit \| a bit () para combinar estilos.</span><span class="sxs-lookup"><span data-stu-id="11add-141">Use the bitwise OR (\|) operator to combine styles.</span></span> <span data-ttu-id="11add-142">Para obtener más información, consulte [estilos de ventana](../winmsg/window-styles.md).</span><span class="sxs-lookup"><span data-stu-id="11add-142">For more information, see [Window Styles](../winmsg/window-styles.md).</span></span>

</dd> <dt>

<span data-ttu-id="11add-143"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*estilo extendido*</span><span class="sxs-lookup"><span data-stu-id="11add-143"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*extended-style*</span></span>
</dt> <dd>

<span data-ttu-id="11add-144">Estilos de ventana extendidos.</span><span class="sxs-lookup"><span data-stu-id="11add-144">Extended window styles.</span></span> <span data-ttu-id="11add-145">Debe especificar el *estilo* para especificar *el estilo extendido*.</span><span class="sxs-lookup"><span data-stu-id="11add-145">You must specify *style* to specify *extended-style*.</span></span> <span data-ttu-id="11add-146">Para obtener más información, vea [**ExStyle**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="11add-146">For more information, see [**EXSTYLE**](exstyle-statement.md).</span></span>

</dd> <dt>

<span data-ttu-id="11add-147"><span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*</span><span class="sxs-lookup"><span data-stu-id="11add-147"><span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*</span></span>
</dt> <dd>

<span data-ttu-id="11add-148">Expresión numérica que indica el identificador usado para identificar el control durante el procesamiento de la [**\_ ayuda de WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="11add-148">Numeric expression indicating the ID used to identify the control during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> <dt>

<span data-ttu-id="11add-149"><span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*</span><span class="sxs-lookup"><span data-stu-id="11add-149"><span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*</span></span>
</dt> <dd>

<span data-ttu-id="11add-150">Datos específicos del control para el control.</span><span class="sxs-lookup"><span data-stu-id="11add-150">Control-specific data for the control.</span></span> <span data-ttu-id="11add-151">Cuando se crea un cuadro de diálogo y se crea un control en ese cuadro de diálogo con datos específicos del control, se pasa un puntero a esos datos en el procedimiento de ventana del control a través del *lParam* del mensaje de [**\_ creación de WM**](../winmsg/wm-create.md) para ese control.</span><span class="sxs-lookup"><span data-stu-id="11add-151">When a dialog is created, and a control in that dialog which has control-specific data is created, a pointer to that data is passed into the control's window procedure through the *lParam* of the [**WM\_CREATE**](../winmsg/wm-create.md) message for that control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11add-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11add-152">Remarks</span></span>

<span data-ttu-id="11add-153">Las unidades de cuadro de diálogo horizontales son 1/4 de la unidad de ancho base del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="11add-153">Horizontal dialog units are 1/4 of the dialog base width unit.</span></span> <span data-ttu-id="11add-154">Las unidades verticales son 1/8 de la unidad de alto del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="11add-154">Vertical units are 1/8 of the dialog base height unit.</span></span> <span data-ttu-id="11add-155">Las unidades base de diálogo actuales se calculan a partir del alto y el ancho de la fuente del sistema actual.</span><span class="sxs-lookup"><span data-stu-id="11add-155">The current dialog base units are computed from the height and width of the current system font.</span></span> <span data-ttu-id="11add-156">La función [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) devuelve las unidades base de cuadro de diálogo en píxeles.</span><span class="sxs-lookup"><span data-stu-id="11add-156">The [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) function returns the dialog base units in pixels.</span></span> <span data-ttu-id="11add-157">Las coordenadas son relativas al origen del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="11add-157">The coordinates are relative to the origin of the dialog box.</span></span>

 

 