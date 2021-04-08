---
title: Command. LabelDescription (propiedad)
description: Representa una descripción de etiqueta.
ms.assetid: 6c683e9e-0742-466e-9fdd-3d29f8ccb9ff
keywords:
- Command. LabelDescription (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Command.LabelDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f748425b4c8363feee737d18c750b3a1d91121b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996941"
---
# <a name="commandlabeldescription-property"></a><span data-ttu-id="5037d-104">Command. LabelDescription (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5037d-104">Command.LabelDescription property</span></span>

<span data-ttu-id="5037d-105">Representa una descripción de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="5037d-105">Represents a label description.</span></span>

## <a name="usage"></a><span data-ttu-id="5037d-106">Uso</span><span class="sxs-lookup"><span data-stu-id="5037d-106">Usage</span></span>

``` syntax
<Command.LabelDescription>
  child elements
</Command.LabelDescription>
```

## <a name="attributes"></a><span data-ttu-id="5037d-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="5037d-107">Attributes</span></span>

<span data-ttu-id="5037d-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="5037d-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5037d-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5037d-109">Child elements</span></span>



| <span data-ttu-id="5037d-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="5037d-110">Element</span></span>                                                   | <span data-ttu-id="5037d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5037d-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="5037d-112">**String@**</span><span class="sxs-lookup"><span data-stu-id="5037d-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="5037d-113">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="5037d-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="5037d-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="5037d-114">Parent elements</span></span>



| <span data-ttu-id="5037d-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="5037d-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="5037d-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="5037d-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="5037d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5037d-117">Remarks</span></span>

<span data-ttu-id="5037d-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5037d-118">Optional.</span></span>

<span data-ttu-id="5037d-119">Puede producirse al menos una vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="5037d-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="5037d-120">**Command. LabelDescription** puede contener un valor de *tipo XS: String* restringido a cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="5037d-120">**Command.LabelDescription** can contain a value of *type xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="5037d-121">Use la referencia de caracteres XML del juego de caracteres universal (UCS) `&#xA;` para especificar un salto de línea.</span><span class="sxs-lookup"><span data-stu-id="5037d-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="5037d-122">La longitud máxima es sin límite.</span><span class="sxs-lookup"><span data-stu-id="5037d-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="5037d-123">Si no se proporciona ningún valor para **Command. LabelDescription**, se requiere el elemento secundario [**String**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="5037d-123">If no value is supplied for **Command.LabelDescription**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="5037d-124">Si **Command. LabelDescription** contiene un valor y un elemento secundario de [**cadena**](windowsribbon-element-string.md) , la **cadena** tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="5037d-124">If **Command.LabelDescription** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="5037d-125">**Command. LabelDescription** solo admite la alineación izquierda.</span><span class="sxs-lookup"><span data-stu-id="5037d-125">**Command.LabelDescription** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="5037d-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5037d-126">Examples</span></span>

<span data-ttu-id="5037d-127">En el ejemplo siguiente se muestra un manifiesto de comandos del Portapapeles con varias declaraciones **Command. LabelDescription** .</span><span class="sxs-lookup"><span data-stu-id="5037d-127">The following example shows a manifest of clipboard Commands with various **Command.LabelDescription** declarations.</span></span>


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



## <a name="requirements"></a><span data-ttu-id="5037d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5037d-128">Requirements</span></span>



| <span data-ttu-id="5037d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5037d-129">Requirement</span></span> | <span data-ttu-id="5037d-130">Value</span><span class="sxs-lookup"><span data-stu-id="5037d-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5037d-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5037d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5037d-132">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5037d-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5037d-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5037d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5037d-134">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5037d-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5037d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="5037d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5037d-136">UI \_ PKEY \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="5037d-136">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 





