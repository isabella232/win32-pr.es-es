---
title: Recurso de icono
description: Define un mapa de bits que define la forma del icono que se va a utilizar para una aplicación determinada o un Icono animado.
ms.assetid: a8e3205e-e17a-4daf-a599-4dc89cb1e640
keywords:
- Menús de recursos de icono y otros recursos
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f762c4f4b459d51a0243a9cdbd7367deda7b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533118"
---
# <a name="icon-resource"></a><span data-ttu-id="0c4b4-104">Recurso de icono</span><span class="sxs-lookup"><span data-stu-id="0c4b4-104">ICON resource</span></span>

<span data-ttu-id="0c4b4-105">Define un mapa de bits que define la forma del icono que se va a utilizar para una aplicación determinada o un Icono animado.</span><span class="sxs-lookup"><span data-stu-id="0c4b4-105">Defines a bitmap that defines the shape of the icon to be used for a given application or an animated icon.</span></span>

``` syntax
nameID ICON filename
```

## <a name="parameters"></a><span data-ttu-id="0c4b4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c4b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c4b4-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="0c4b4-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="0c4b4-108">Nombre único o un valor entero sin signo de 16 bits que identifica el recurso.</span><span class="sxs-lookup"><span data-stu-id="0c4b4-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="0c4b4-109"><span id="filename"></span><span id="FILENAME"></span>*extensión*</span><span class="sxs-lookup"><span data-stu-id="0c4b4-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="0c4b4-110">Nombre del archivo que contiene el recurso.</span><span class="sxs-lookup"><span data-stu-id="0c4b4-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="0c4b4-111">El nombre debe ser un nombre de archivo válido. debe ser una ruta de acceso completa si el archivo no está en el directorio de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="0c4b4-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="0c4b4-112">La ruta de acceso debe ser una cadena entre comillas.</span><span class="sxs-lookup"><span data-stu-id="0c4b4-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="0c4b4-113">Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="0c4b4-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="0c4b4-114">Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="0c4b4-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0c4b4-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c4b4-115">Remarks</span></span>

<span data-ttu-id="0c4b4-116">Los recursos de icono y cursor pueden contener más de una imagen.</span><span class="sxs-lookup"><span data-stu-id="0c4b4-116">Icon and cursor resources can contain more than one image.</span></span>

## <a name="examples"></a><span data-ttu-id="0c4b4-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0c4b4-117">Examples</span></span>

<span data-ttu-id="0c4b4-118">En el ejemplo siguiente se definen dos recursos de icono:</span><span class="sxs-lookup"><span data-stu-id="0c4b4-118">The following example defines two icon resources:</span></span>

``` syntax
desk1   ICON "desk.ico"
11      ICON "custom.ico"
```

## <a name="see-also"></a><span data-ttu-id="0c4b4-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c4b4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c4b4-120">Usar iconos</span><span class="sxs-lookup"><span data-stu-id="0c4b4-120">Using Icons</span></span>](./using-icons.md)
</dt> </dl>

 

 