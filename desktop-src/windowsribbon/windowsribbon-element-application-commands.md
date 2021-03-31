---
title: Application. Commands (propiedad)
description: Representa un contenedor para todos los comandos definidos por la aplicación.
ms.assetid: 160d7d28-2d64-4cbc-b2b9-2da6b2f5b3c8
keywords:
- Propiedad Application. Commands (cinta de Windows)
topic_type:
- apiref
api_name:
- Application.Commands
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8de2b88b97dda96636a9c5da3ad078f678091d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490559"
---
# <a name="applicationcommands-property"></a><span data-ttu-id="9615d-104">Application. Commands (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9615d-104">Application.Commands property</span></span>

<span data-ttu-id="9615d-105">Representa un contenedor para todos los comandos definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9615d-105">Represents a container for all the Commands that are defined by the application.</span></span>

## <a name="usage"></a><span data-ttu-id="9615d-106">Uso</span><span class="sxs-lookup"><span data-stu-id="9615d-106">Usage</span></span>

``` syntax
<Application.Commands>
  child elements
</Application.Commands>
```

## <a name="attributes"></a><span data-ttu-id="9615d-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="9615d-107">Attributes</span></span>

<span data-ttu-id="9615d-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="9615d-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9615d-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9615d-109">Child elements</span></span>



| <span data-ttu-id="9615d-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="9615d-110">Element</span></span>                                                     | <span data-ttu-id="9615d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9615d-111">Description</span></span>                                        |
|-------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="9615d-112">**Command**</span><span class="sxs-lookup"><span data-stu-id="9615d-112">**Command**</span></span>](windowsribbon-element-command.md)<br/> | <span data-ttu-id="9615d-113">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="9615d-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="9615d-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="9615d-114">Parent elements</span></span>



| <span data-ttu-id="9615d-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="9615d-115">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="9615d-116">**Aplicación**</span><span class="sxs-lookup"><span data-stu-id="9615d-116">**Application**</span></span>](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="9615d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9615d-117">Remarks</span></span>

<span data-ttu-id="9615d-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9615d-118">Optional.</span></span>

<span data-ttu-id="9615d-119">Puede producirse al menos una vez para cada elemento de la [**aplicación**](windowsribbon-element-application.md) .</span><span class="sxs-lookup"><span data-stu-id="9615d-119">May occur at most once for each [**Application**](windowsribbon-element-application.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="9615d-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9615d-120">Examples</span></span>

<span data-ttu-id="9615d-121">En el ejemplo siguiente se muestra un elemento **Application. Commands** que contiene un manifiesto de comandos del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="9615d-121">The following example shows an **Application.Commands** element that contains a manifest of clipboard Commands.</span></span>


```C++
<Application.Commands>
```




```C++
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




```C++
</Application.Commands>
```



## <a name="requirements"></a><span data-ttu-id="9615d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9615d-122">Requirements</span></span>



| <span data-ttu-id="9615d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9615d-123">Requirement</span></span> | <span data-ttu-id="9615d-124">Value</span><span class="sxs-lookup"><span data-stu-id="9615d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9615d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9615d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9615d-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9615d-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="9615d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9615d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9615d-128">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9615d-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9615d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9615d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9615d-130">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="9615d-130">**Application.Views**</span></span>](windowsribbon-element-application-views.md)
</dt> </dl>

 

 





