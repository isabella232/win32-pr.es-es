---
title: Recurso DIALOGEX
description: Define un cuadro de diálogo. | Recurso DIALOGEX
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- Menús de recursos de DIALOGEX y otros recursos
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd55bfb06b678742aa5e356c9e62b14229aa8d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280116"
---
# <a name="dialogex-resource"></a><span data-ttu-id="9d360-105">Recurso DIALOGEX</span><span class="sxs-lookup"><span data-stu-id="9d360-105">DIALOGEX resource</span></span>

<span data-ttu-id="9d360-106">Define un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-106">Defines a dialog box.</span></span> <span data-ttu-id="9d360-107">La instrucción define la posición y las dimensiones del cuadro de diálogo en la pantalla, así como el estilo del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-107">The statement defines the position and dimensions of the dialog box on the screen as well as the dialog box style.</span></span> <span data-ttu-id="9d360-108">También define lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9d360-108">It also defines the following:</span></span>

-   <span data-ttu-id="9d360-109">Los identificadores de la ayuda en el cuadro de diálogo en sí, así como en los controles del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-109">Help IDs on the dialog itself as well as on controls within the dialog box.</span></span>
-   <span data-ttu-id="9d360-110">Uso de la instrucción de [**ExStyle**](exstyle-statement.md) para el cuadro de diálogo en sí, así como en los controles del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-110">Use of the [**EXSTYLE**](exstyle-statement.md) statement for the dialog box itself as well as on controls within the dialog box.</span></span>
-   <span data-ttu-id="9d360-111">Configuración de espesor de fuente y cursiva para la fuente que se va a utilizar en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-111">Font weight and italic settings for the font to be used in the dialog box.</span></span>
-   <span data-ttu-id="9d360-112">Datos específicos del control para los controles del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-112">Control-specific data for controls within the dialog box.</span></span>
-   <span data-ttu-id="9d360-113">Uso de los nombres de clase del sistema predefinido **BEDIT**, **IEDIT** y **HEDIT** .</span><span class="sxs-lookup"><span data-stu-id="9d360-113">Use of the **BEDIT**, **IEDIT**, and **HEDIT** predefined system class names.</span></span>

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a><span data-ttu-id="9d360-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d360-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d360-115"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="9d360-115"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-116">Nombre único o un valor entero de 16 bits sin signo único que identifica el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-116">Unique name or a unique 16-bit unsigned integer value that identifies the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="9d360-117"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="9d360-117"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-118">Ubicación en la pantalla del lado izquierdo del cuadro de diálogo, en unidades de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-118">Location on the screen of the left side of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="9d360-119"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="9d360-119"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-120">Ubicación en la pantalla de la parte superior del cuadro de diálogo, en unidades de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-120">Location on the screen of the top of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="9d360-121"><span id="width"></span><span id="WIDTH"></span>*Ancho*</span><span class="sxs-lookup"><span data-stu-id="9d360-121"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-122">Ancho del cuadro de diálogo, en unidades de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-122">Width of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="9d360-123"><span id="height"></span><span id="HEIGHT"></span>*alto*</span><span class="sxs-lookup"><span data-stu-id="9d360-123"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-124">Alto del cuadro de diálogo, en unidades de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-124">Height of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="9d360-125"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span><span class="sxs-lookup"><span data-stu-id="9d360-125"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-126">Expresión numérica que indica el identificador usado para identificar el cuadro de diálogo durante el procesamiento de la [**\_ ayuda de WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="9d360-126">Numeric expression indicating the ID used to identify the dialog box during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> <dt>

<span data-ttu-id="9d360-127"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instrucciones opcionales*</span><span class="sxs-lookup"><span data-stu-id="9d360-127"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-128">Opciones del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-128">Options for the dialog box.</span></span> <span data-ttu-id="9d360-129">Puede ser cero o más de las instrucciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="9d360-129">This can be zero or more of the following statements.</span></span>



| <span data-ttu-id="9d360-130">.</span><span class="sxs-lookup"><span data-stu-id="9d360-130">Statement</span></span>                                                         | <span data-ttu-id="9d360-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d360-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d360-132">**Título** de "*texto*"</span><span class="sxs-lookup"><span data-stu-id="9d360-132">**CAPTION** "*text*"</span></span>                                              | <span data-ttu-id="9d360-133">Título del cuadro de diálogo si tiene una barra de título.</span><span class="sxs-lookup"><span data-stu-id="9d360-133">Caption of the dialog box if it has a title bar.</span></span> <span data-ttu-id="9d360-134">Para obtener más información, vea la [**instrucción Caption**](caption-statement.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-134">For more information, see [**CAPTION Statement**](caption-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="9d360-135">**Características** *DWORD*</span><span class="sxs-lookup"><span data-stu-id="9d360-135">**CHARACTERISTICS** *dword*</span></span>                                       | <span data-ttu-id="9d360-136">Valor **DWORD** definido por el usuario para que lo usen las herramientas de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d360-136">User-defined **DWORD** value for use by resource tools.</span></span> <span data-ttu-id="9d360-137">El sistema no utiliza este valor.</span><span class="sxs-lookup"><span data-stu-id="9d360-137">This value is not used by the system.</span></span> <span data-ttu-id="9d360-138">Para obtener más información, vea la [**instrucción Characteristics**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-138">For more information, see [**CHARACTERISTICS Statement**](characteristics-statement.md).</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="9d360-139">_Clase de_ clase</span><span class="sxs-lookup"><span data-stu-id="9d360-139">**CLASS**_class_</span></span>                                                  | <span data-ttu-id="9d360-140">Entero de 16 bits sin signo o cadena, entre comillas dobles ("), que identifica la clase del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-140">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="9d360-141">Para obtener más información, vea [**Class (instrucción**](class-statement.md)).</span><span class="sxs-lookup"><span data-stu-id="9d360-141">For more information, see [**CLASS Statement**](class-statement.md).</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="9d360-142">**EXstyle** =  *estilos extendidos*</span><span class="sxs-lookup"><span data-stu-id="9d360-142">**EXSTYLE**= *extended-styles*</span></span>                                    | <span data-ttu-id="9d360-143">Estilo de ventana extendida del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-143">Extended window style of the dialog box.</span></span> <span data-ttu-id="9d360-144">Para obtener más información, vea la [**instrucción de ExStyle**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-144">For more information, see [**EXSTYLE Statement**](exstyle-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="9d360-145"> *Puntuación* de fuente, "tipo de *letra*", *peso*, *cursiva*, *juego de caracteres*</span><span class="sxs-lookup"><span data-stu-id="9d360-145">**FONT** *pointsize*, "*typeface*", *weight*, *italic*, *charset*</span></span> | <span data-ttu-id="9d360-146">Tamaño de punto y tipo de letra de la fuente.</span><span class="sxs-lookup"><span data-stu-id="9d360-146">Point size and typeface for the font.</span></span> <span data-ttu-id="9d360-147">En *peso*, use los valores \*\* \_ \* FW\* _ definidos en WinGDI. h.</span><span class="sxs-lookup"><span data-stu-id="9d360-147">For *weight*, use the \**FW\_\** _ values defined in WinGDI.h.</span></span> <span data-ttu-id="9d360-148">En _italic \*, especifique TRUE para utilizar una fuente en cursiva; de lo contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="9d360-148">For _italic\*, specify TRUE to use an italic font, FALSE otherwise.</span></span> <span data-ttu-id="9d360-149">Para *CharSet*, use el valor definido en el miembro **lfCharSet** de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="9d360-149">For *charset*, use the value defined in the **lfCharSet** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="9d360-150">Para obtener la fuente definitiva de un cuadro de diálogo, una aplicación debe especificar *CharSet* junto con otras propiedades de fuente.</span><span class="sxs-lookup"><span data-stu-id="9d360-150">To get the definitive font for a dialog box, an application should specify *charset* along with other font properties.</span></span> <span data-ttu-id="9d360-151">Para obtener más información, vea la [**instrucción Font**](font-statement.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-151">For more information, see [**FONT Statement**](font-statement.md).</span></span> |
| <span data-ttu-id="9d360-152"> *Idioma* del idioma, *subidioma*</span><span class="sxs-lookup"><span data-stu-id="9d360-152">**LANGUAGE** *language*, *sublanguage*</span></span>                            | <span data-ttu-id="9d360-153">Idioma del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-153">Language of the dialog box.</span></span> <span data-ttu-id="9d360-154">Para obtener más información, vea [**Language Statement**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-154">For more information, see [**LANGUAGE Statement**](language-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="9d360-155"> *NombreMenú* de menú</span><span class="sxs-lookup"><span data-stu-id="9d360-155">**MENU** *menuname*</span></span>                                               | <span data-ttu-id="9d360-156">Menú que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="9d360-156">Menu to be used.</span></span> <span data-ttu-id="9d360-157">Este valor es el nombre del menú o su identificador entero.</span><span class="sxs-lookup"><span data-stu-id="9d360-157">This value is either the name of the menu or its integer identifier.</span></span> <span data-ttu-id="9d360-158">Para obtener más información, vea [**instrucción de menú**](menu-statement.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-158">For more information, see [**MENU Statement**](menu-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="9d360-159"> *Estilos* de estilo</span><span class="sxs-lookup"><span data-stu-id="9d360-159">**STYLE** *styles*</span></span>                                                | <span data-ttu-id="9d360-160">Estilos del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d360-160">Styles of the dialog box.</span></span> <span data-ttu-id="9d360-161">Para obtener más información, vea [**Style (instrucción**](style-statement.md)).</span><span class="sxs-lookup"><span data-stu-id="9d360-161">For more information, see [**STYLE Statement**](style-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9d360-162">**Versión** *DWORD*</span><span class="sxs-lookup"><span data-stu-id="9d360-162">**VERSION** *dword*</span></span>                                               | <span data-ttu-id="9d360-163">Valor **DWORD** definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="9d360-163">User-defined **DWORD** value.</span></span> <span data-ttu-id="9d360-164">Esta instrucción está pensada para su uso por parte de herramientas de recursos adicionales y el sistema no la utiliza.</span><span class="sxs-lookup"><span data-stu-id="9d360-164">This statement is intended for use by additional resource tools and is not used by the system.</span></span> <span data-ttu-id="9d360-165">Para obtener más información, vea la [**instrucción version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-165">For more information, see [**VERSION Statement**](version-statement.md).</span></span>                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="9d360-166"><span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*instrucciones de control*</span><span class="sxs-lookup"><span data-stu-id="9d360-166"><span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*control-statements*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-167">El cuerpo del recurso **DIALOGEX** se compone de cualquier número de instrucciones de control.</span><span class="sxs-lookup"><span data-stu-id="9d360-167">Body of the **DIALOGEX** resource is made up of any number of control statements.</span></span> <span data-ttu-id="9d360-168">Hay cuatro familias de instrucciones de control: genérica, estática, de botón y de edición.</span><span class="sxs-lookup"><span data-stu-id="9d360-168">There are four families of control statements: generic, static, button, and edit.</span></span> <span data-ttu-id="9d360-169">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="9d360-169">For more information, see Remarks.</span></span>

</dd> </dl>

<span data-ttu-id="9d360-170">Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="9d360-170">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="9d360-171">Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-171">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9d360-172">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d360-172">Remarks</span></span>

<span data-ttu-id="9d360-173">Las operaciones válidas que pueden incluirse en cualquiera de las expresiones numéricas de las instrucciones de **DIALOGEX** son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="9d360-173">The valid operations that may be contained in any of the numeric expressions in the statements of **DIALOGEX** are as follows:</span></span>

-   <span data-ttu-id="9d360-174">Agregar (' + ')</span><span class="sxs-lookup"><span data-stu-id="9d360-174">Add ('+')</span></span>
-   <span data-ttu-id="9d360-175">Resta ('-')</span><span class="sxs-lookup"><span data-stu-id="9d360-175">Subtract ('-')</span></span>
-   <span data-ttu-id="9d360-176">Unario menos ('-')</span><span class="sxs-lookup"><span data-stu-id="9d360-176">Unary minus ('-')</span></span>
-   <span data-ttu-id="9d360-177">Unario no (' ~ ')</span><span class="sxs-lookup"><span data-stu-id="9d360-177">Unary NOT ('~')</span></span>
-   <span data-ttu-id="9d360-178">Y (' & ')</span><span class="sxs-lookup"><span data-stu-id="9d360-178">AND ('&')</span></span>
-   <span data-ttu-id="9d360-179">O (' \| ')</span><span class="sxs-lookup"><span data-stu-id="9d360-179">OR ('\|')</span></span>

<span data-ttu-id="9d360-180">El cuerpo del recurso se compone de instrucciones de control genérico, estático, de botón y de edición.</span><span class="sxs-lookup"><span data-stu-id="9d360-180">The body of the resource is made up of generic, static, button, and edit control statements.</span></span> <span data-ttu-id="9d360-181">Aunque cada una de estas familias de instrucciones usa una sintaxis diferente para definir características específicas de sus controles, todos comparten una sintaxis común para definir la posición, el tamaño, los estilos extendidos, el número de identificación de la ayuda y los datos específicos del control.</span><span class="sxs-lookup"><span data-stu-id="9d360-181">While each of these families of statements uses a different syntax for defining specific features of its controls, they all share a common syntax for defining the position, size, extended styles, help identification number, and control-specific data.</span></span> <span data-ttu-id="9d360-182">Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-182">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

### <a name="generic-control-statements"></a><span data-ttu-id="9d360-183">Instrucciones de control genérico</span><span class="sxs-lookup"><span data-stu-id="9d360-183">Generic Control Statements</span></span>

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span data-ttu-id="9d360-184"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span><span class="sxs-lookup"><span data-stu-id="9d360-184"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-185">Texto de la ventana para el control.</span><span class="sxs-lookup"><span data-stu-id="9d360-185">Window text for the control.</span></span> <span data-ttu-id="9d360-186">Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-186">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d360-187"><span id="id"></span><span id="ID"></span>*sesión*</span><span class="sxs-lookup"><span data-stu-id="9d360-187"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-188">Identificador de control.</span><span class="sxs-lookup"><span data-stu-id="9d360-188">Control identifier.</span></span> <span data-ttu-id="9d360-189">Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-189">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d360-190"><span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*</span><span class="sxs-lookup"><span data-stu-id="9d360-190"><span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-191">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="9d360-191">Name of the class.</span></span> <span data-ttu-id="9d360-192">Puede ser una cadena entre comillas dobles (") o una de las siguientes clases del sistema predefinidas: **Button**, **static**, **Edit**, **ListBox**, **ScrollBar** o **ComboBox**.</span><span class="sxs-lookup"><span data-stu-id="9d360-192">This may be either a string enclosed in double quotation marks (") or one of the following predefined system classes: **BUTTON**, **STATIC**, **EDIT**, **LISTBOX**, **SCROLLBAR**, or **COMBOBOX**.</span></span>

</dd> <dt>

<span data-ttu-id="9d360-193"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="9d360-193"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-194">Los estilos de ventana (valores explícitos **WS \_ \* *_, _* BS \_ \* *_, _* SS \_ \* *_, _* es \_ \* *_, _* lb \_ \* *_, _* SBS \_ \* *_ y _* \_ \*** valor de estilo CBS definidos en Winuser. H se pueden usar agregando una inclusión al archivo. RC: `#include "winuser.h"` ).</span><span class="sxs-lookup"><span data-stu-id="9d360-194">Window styles (explicit **WS\_\**_, _\* BS\_\**_, _\* SS\_\*\*_, _\* ES\_\*\*_, _\* LBS\_\*\*_, _\* SBS\_\*\*_, and _\* CBS\_\*\*\* style values defined in Winuser.H can be used by adding an include to the .rc file: `#include "winuser.h"`).</span></span> <span data-ttu-id="9d360-195">Para obtener más información, consulte [estilos de ventana](/windows/desktop/winmsg/window-styles).</span><span class="sxs-lookup"><span data-stu-id="9d360-195">For more information, see [Window Styles](/windows/desktop/winmsg/window-styles).</span></span>

</dd> </dl>

### <a name="static-control-statements"></a><span data-ttu-id="9d360-196">Instrucciones de control estático</span><span class="sxs-lookup"><span data-stu-id="9d360-196">Static Control Statements</span></span>

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span data-ttu-id="9d360-197"><span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*</span><span class="sxs-lookup"><span data-stu-id="9d360-197"><span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-198">**LTEXT**, **RText** o **CTEXT**.</span><span class="sxs-lookup"><span data-stu-id="9d360-198">**LTEXT**, **RTEXT**, or **CTEXT**.</span></span>

</dd> <dt>

<span data-ttu-id="9d360-199"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span><span class="sxs-lookup"><span data-stu-id="9d360-199"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-200">Texto de la ventana para el control.</span><span class="sxs-lookup"><span data-stu-id="9d360-200">Window text for the control.</span></span> <span data-ttu-id="9d360-201">Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-201">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d360-202"><span id="id"></span><span id="ID"></span>*sesión*</span><span class="sxs-lookup"><span data-stu-id="9d360-202"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-203">Identificador de control.</span><span class="sxs-lookup"><span data-stu-id="9d360-203">Control identifier.</span></span> <span data-ttu-id="9d360-204">Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-204">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

### <a name="button-control-statements"></a><span data-ttu-id="9d360-205">Instrucciones de control de botón</span><span class="sxs-lookup"><span data-stu-id="9d360-205">Button Control Statements</span></span>

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span data-ttu-id="9d360-206"><span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*</span><span class="sxs-lookup"><span data-stu-id="9d360-206"><span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-207">**AUTO3STATE**, **autocheckbox**, **autoradiobutton**, **CheckBox**, **PUSHBOX**, **PUSHBUTTON**, **RADIOBUTTON**, **STATE3** o **USERBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="9d360-207">**AUTO3STATE**, **AUTOCHECKBOX**, **AUTORADIOBUTTON**, **CHECKBOX**, **PUSHBOX**, **PUSHBUTTON**, **RADIOBUTTON**, **STATE3**, or **USERBUTTON**.</span></span>

</dd> <dt>

<span data-ttu-id="9d360-208"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span><span class="sxs-lookup"><span data-stu-id="9d360-208"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-209">Texto de la ventana para el control.</span><span class="sxs-lookup"><span data-stu-id="9d360-209">Window text for the control.</span></span> <span data-ttu-id="9d360-210">Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-210">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d360-211"><span id="id"></span><span id="ID"></span>*sesión*</span><span class="sxs-lookup"><span data-stu-id="9d360-211"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-212">Identificador de control.</span><span class="sxs-lookup"><span data-stu-id="9d360-212">Control identifier.</span></span> <span data-ttu-id="9d360-213">Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-213">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

### <a name="edit-control-statements"></a><span data-ttu-id="9d360-214">Editar instrucciones de control</span><span class="sxs-lookup"><span data-stu-id="9d360-214">Edit Control Statements</span></span>

``` syntax
editClass id
```

<dl> <dt>

<span data-ttu-id="9d360-215"><span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*</span><span class="sxs-lookup"><span data-stu-id="9d360-215"><span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-216">**EDITTEXT**, **BEDIT**, **HEDIT** o **IEDIT**.</span><span class="sxs-lookup"><span data-stu-id="9d360-216">**EDITTEXT**, **BEDIT**, **HEDIT**, or **IEDIT**.</span></span>

</dd> <dt>

<span data-ttu-id="9d360-217"><span id="id"></span><span id="ID"></span>*sesión*</span><span class="sxs-lookup"><span data-stu-id="9d360-217"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="9d360-218">Identificador de control.</span><span class="sxs-lookup"><span data-stu-id="9d360-218">Control identifier.</span></span> <span data-ttu-id="9d360-219">Para obtener más información, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9d360-219">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="9d360-220">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d360-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d360-221">Usar cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="9d360-221">Using Dialog Boxes</span></span>](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[<span data-ttu-id="9d360-222">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="9d360-222">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="9d360-223">**SUS**</span><span class="sxs-lookup"><span data-stu-id="9d360-223">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="9d360-224">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="9d360-224">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="9d360-225">**CreateDialog**</span><span class="sxs-lookup"><span data-stu-id="9d360-225">**CreateDialog**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[<span data-ttu-id="9d360-226">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="9d360-226">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="9d360-227">**DialogBox**</span><span class="sxs-lookup"><span data-stu-id="9d360-227">**DialogBox**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[<span data-ttu-id="9d360-228">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="9d360-228">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="9d360-229">**MÓDULO**</span><span class="sxs-lookup"><span data-stu-id="9d360-229">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="9d360-230">**NDPTECGDI**</span><span class="sxs-lookup"><span data-stu-id="9d360-230">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[<span data-ttu-id="9d360-231">MENU</span><span class="sxs-lookup"><span data-stu-id="9d360-231">MENU</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="9d360-232">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="9d360-232">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="9d360-233">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="9d360-233">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="9d360-234">**Versión**</span><span class="sxs-lookup"><span data-stu-id="9d360-234">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
