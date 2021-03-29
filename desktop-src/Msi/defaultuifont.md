---
description: La propiedad DefaultUIFont establece el estilo de fuente predeterminado que se usa para los controles. Para especificar el valor predeterminado, establezca DefaultUIFont en uno de los estilos predefinidos de la tabla TextStyle en la tabla de propiedades.
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: Propiedad DefaultUIFont
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3791219dcef84253280fec3c797f2035afd239f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654024"
---
# <a name="defaultuifont-property"></a><span data-ttu-id="da5d3-104">Propiedad DefaultUIFont</span><span class="sxs-lookup"><span data-stu-id="da5d3-104">DefaultUIFont property</span></span>

<span data-ttu-id="da5d3-105">La propiedad **DefaultUIFont** establece el estilo de fuente predeterminado que se usa para los controles.</span><span class="sxs-lookup"><span data-stu-id="da5d3-105">The **DefaultUIFont** property sets the default font style used for controls.</span></span> <span data-ttu-id="da5d3-106">Para especificar el valor predeterminado, establezca **DefaultUIFont** en uno de los estilos predefinidos de la [tabla TextStyle](textstyle-table.md) en la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="da5d3-106">To specify the default, set **DefaultUIFont** to one of the predefined styles in the [TextStyle table](textstyle-table.md) in the [Property table](property-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="da5d3-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da5d3-107">Remarks</span></span>

<span data-ttu-id="da5d3-108">La propiedad **DefaultUIFont** de cada paquete de instalación con una interfaz de usuario debe establecerse en la [tabla de propiedades](property-table.md) en uno de los estilos predefinidos enumerados en la [tabla TextStyle](textstyle-table.md).</span><span class="sxs-lookup"><span data-stu-id="da5d3-108">The **DefaultUIFont** property of every installation package with a UI should be set in the [Property table](property-table.md) to one of the predefined styles listed in the [TextStyle table](textstyle-table.md).</span></span> <span data-ttu-id="da5d3-109">Si no se especifica esta propiedad, el instalador utiliza la fuente del sistema.</span><span class="sxs-lookup"><span data-stu-id="da5d3-109">If this property is not specified, the installer uses the System font.</span></span> <span data-ttu-id="da5d3-110">Esto puede hacer que el instalador muestre de forma incorrecta cadenas de texto cuando la página de códigos del paquete es diferente de la página de códigos de la interfaz de usuario predeterminada del usuario.</span><span class="sxs-lookup"><span data-stu-id="da5d3-110">This can cause the installer to improperly display text strings when the package's code page is different from the user's default UI code page.</span></span>

<span data-ttu-id="da5d3-111">El estilo de texto y fuente de un control se puede establecer tal y como se describe en [Agregar controles y texto](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="da5d3-111">The text and font style of a control can be set as described in [Adding Controls and Text](adding-controls-and-text.md).</span></span> <span data-ttu-id="da5d3-112">Si la cadena de caracteres que se muestra en la columna de texto de la tabla de [control](control-table.md) o de la [tabla BBControl](bbcontrol-table.md) no especifica el estilo de fuente, el control utiliza el valor de la propiedad **DefaultUIFont** como estilo de fuente.</span><span class="sxs-lookup"><span data-stu-id="da5d3-112">If the character string listed in the Text column of the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md) does not specify the font style, the control uses the value of the **DefaultUIFont** property as the font style.</span></span>

## <a name="requirements"></a><span data-ttu-id="da5d3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da5d3-113">Requirements</span></span>



| <span data-ttu-id="da5d3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="da5d3-114">Requirement</span></span> | <span data-ttu-id="da5d3-115">Value</span><span class="sxs-lookup"><span data-stu-id="da5d3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da5d3-116">Versión</span><span class="sxs-lookup"><span data-stu-id="da5d3-116">Version</span></span><br/> | <span data-ttu-id="da5d3-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="da5d3-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="da5d3-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="da5d3-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="da5d3-119">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="da5d3-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="da5d3-120">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="da5d3-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da5d3-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="da5d3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da5d3-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="da5d3-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




