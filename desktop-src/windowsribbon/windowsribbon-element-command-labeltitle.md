---
title: Command. LabelTitle (propiedad)
description: Representa un título de etiqueta.
ms.assetid: 97378ec3-7988-4e39-9cf5-c382b246c5c9
keywords:
- Command. LabelTitle (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Command.LabelTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6d6c72ddd60cca63834fdcf21cf8f8b726ad22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535074"
---
# <a name="commandlabeltitle-property"></a><span data-ttu-id="ecb40-104">Command. LabelTitle (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ecb40-104">Command.LabelTitle property</span></span>

<span data-ttu-id="ecb40-105">Representa un título de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="ecb40-105">Represents a label title.</span></span>

## <a name="usage"></a><span data-ttu-id="ecb40-106">Uso</span><span class="sxs-lookup"><span data-stu-id="ecb40-106">Usage</span></span>

``` syntax
<Command.LabelTitle>
  child elements
</Command.LabelTitle>
```

## <a name="attributes"></a><span data-ttu-id="ecb40-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="ecb40-107">Attributes</span></span>

<span data-ttu-id="ecb40-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="ecb40-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ecb40-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ecb40-109">Child elements</span></span>



| <span data-ttu-id="ecb40-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="ecb40-110">Element</span></span>                                                   | <span data-ttu-id="ecb40-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecb40-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="ecb40-112">**String@**</span><span class="sxs-lookup"><span data-stu-id="ecb40-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="ecb40-113">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="ecb40-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ecb40-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="ecb40-114">Parent elements</span></span>



| <span data-ttu-id="ecb40-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="ecb40-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="ecb40-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="ecb40-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ecb40-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecb40-117">Remarks</span></span>

<span data-ttu-id="ecb40-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ecb40-118">Optional.</span></span>

<span data-ttu-id="ecb40-119">Puede producirse al menos una vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="ecb40-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="ecb40-120">**Command. LabelTitle** puede contener un valor de tipo *xs: String* restringido a cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="ecb40-120">**Command.LabelTitle** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="ecb40-121">Use la referencia de caracteres XML del juego de caracteres universal (UCS) `&#xA;` para especificar un salto de línea.</span><span class="sxs-lookup"><span data-stu-id="ecb40-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="ecb40-122">La longitud máxima es sin límite.</span><span class="sxs-lookup"><span data-stu-id="ecb40-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="ecb40-123">Si no se proporciona ningún valor para **Command. LabelTitle**, se requiere el elemento secundario [**String**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="ecb40-123">If no value is supplied for **Command.LabelTitle**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="ecb40-124">Si **Command. LabelTitle** contiene un valor y un elemento secundario de [**cadena**](windowsribbon-element-string.md) , la **cadena** tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="ecb40-124">If **Command.LabelTitle** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="ecb40-125">**Command. LabelTitle** solo admite la alineación izquierda.</span><span class="sxs-lookup"><span data-stu-id="ecb40-125">**Command.LabelTitle** only supports left alignment.</span></span>

<span data-ttu-id="ecb40-126">Si un comando se expone a través de un elemento de menú y el valor de la [ \_ \_ etiqueta](windowsribbon-reference-properties-uipkey-label.md) **Command. LabelTitle** o UI PKEY contiene una letra precedida por un símbolo de y comercial, como se muestra en el ejemplo siguiente, esta letra se trata como un KeyTip y una tecla de aceleración para ese comando por el marco de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="ecb40-126">If a Command is exposed through a menu item and the value of **Command.LabelTitle** or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md) contains a letter preceded by an ampersand, as shown in the following example, this letter is treated as both a keytip and a keyboard accelerator for that Command by the Ribbon framework.</span></span>


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



<span data-ttu-id="ecb40-127">Para mostrar una y comercial en una etiqueta, escape la designación de carácter especial con un signo de y comercial ( `&&` ), tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="ecb40-127">To display an ampersand in a label, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="examples"></a><span data-ttu-id="ecb40-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ecb40-128">Examples</span></span>

<span data-ttu-id="ecb40-129">En el ejemplo siguiente se muestra el marcado de un elemento [**Command**](windowsribbon-element-command.md) con una declaración **Command. LabelTitle** .</span><span class="sxs-lookup"><span data-stu-id="ecb40-129">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.LabelTitle** declaration.</span></span>


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="ecb40-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecb40-130">Requirements</span></span>



| <span data-ttu-id="ecb40-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecb40-131">Requirement</span></span> | <span data-ttu-id="ecb40-132">Value</span><span class="sxs-lookup"><span data-stu-id="ecb40-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ecb40-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecb40-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ecb40-134">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ecb40-134">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ecb40-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecb40-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ecb40-136">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ecb40-136">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ecb40-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecb40-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb40-138">\_Etiqueta PKEY de IU \_</span><span class="sxs-lookup"><span data-stu-id="ecb40-138">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 





