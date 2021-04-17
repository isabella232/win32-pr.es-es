---
description: La propiedad ProductLanguage especifica el idioma que debe usar el instalador para cualquier cadena de la interfaz de usuario que no se haya creado en la base de datos.
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: Propiedad ProductLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3199bd2fcef457b40ad98e52f50c595bc424f9a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680660"
---
# <a name="productlanguage-property"></a><span data-ttu-id="567e3-103">Propiedad ProductLanguage</span><span class="sxs-lookup"><span data-stu-id="567e3-103">ProductLanguage property</span></span>

<span data-ttu-id="567e3-104">La propiedad **ProductLanguage** especifica el idioma que debe usar el instalador para cualquier cadena de la interfaz de usuario que no se haya creado en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="567e3-104">The **ProductLanguage** property specifies the language the installer should use for any strings in the user interface that are not authored into the database.</span></span> <span data-ttu-id="567e3-105">Esta propiedad debe ser un identificador de idioma numérico (LANGID).</span><span class="sxs-lookup"><span data-stu-id="567e3-105">This property must be a numeric language identifier (LANGID).</span></span> <span data-ttu-id="567e3-106">Si una transformación cambia el idioma de la interfaz de usuario en la base de datos, también debe cambiar el valor de esta propiedad para que refleje el nuevo lenguaje.</span><span class="sxs-lookup"><span data-stu-id="567e3-106">If a transform changes the language of the user interface in the database, then it should also change the value of this property to reflect the new language.</span></span>

<span data-ttu-id="567e3-107">Esta propiedad es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="567e3-107">This property is REQUIRED.</span></span>

## <a name="remarks"></a><span data-ttu-id="567e3-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="567e3-108">Remarks</span></span>

<span data-ttu-id="567e3-109">El valor de la propiedad **ProductLanguage** debe ser uno de los idiomas enumerados en la propiedad Resumen de la [**plantilla**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="567e3-109">The value of the **ProductLanguage** property must be one of the languages listed in the [**Template Summary**](template-summary.md) property.</span></span>

<span data-ttu-id="567e3-110">Al crear un paquete como independiente del lenguaje, establezca la propiedad **ProductLanguage** en 0 y use la fuente MS Shell Dlg como estilo de texto para todos los diálogos creados.</span><span class="sxs-lookup"><span data-stu-id="567e3-110">When authoring a package as language-neutral, set the **ProductLanguage** property to 0 and use the MS Shell Dlg font as the text style for all authored dialogs.</span></span> <span data-ttu-id="567e3-111">Dado que algunas fuentes no admiten todos los juegos de caracteres, puede asegurarse de que el texto se muestre correctamente en todas las versiones localizadas del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="567e3-111">Because some fonts do not support all the character sets, by using this font you can ensure that the text is correctly displayed on all localized versions of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="567e3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="567e3-112">Requirements</span></span>



| <span data-ttu-id="567e3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="567e3-113">Requirement</span></span> | <span data-ttu-id="567e3-114">Value</span><span class="sxs-lookup"><span data-stu-id="567e3-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="567e3-115">Versión</span><span class="sxs-lookup"><span data-stu-id="567e3-115">Version</span></span><br/> | <span data-ttu-id="567e3-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="567e3-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="567e3-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="567e3-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="567e3-118">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="567e3-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="567e3-119">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="567e3-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="567e3-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="567e3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="567e3-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="567e3-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




