---
title: Recurso de mapa de bits
description: Define un mapa de bits que utiliza una aplicación en su presentación en pantalla o como un elemento de un menú o control.
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- Menús de recursos de mapa de bits y otros recursos
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5bed33fb66d9deb85e1f25165f3f7a0f664961
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420608"
---
# <a name="bitmap-resource"></a><span data-ttu-id="7451c-104">Recurso de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="7451c-104">BITMAP resource</span></span>

<span data-ttu-id="7451c-105">Define un mapa de bits que utiliza una aplicación en su presentación en pantalla o como un elemento de un menú o control.</span><span class="sxs-lookup"><span data-stu-id="7451c-105">Defines a bitmap that an application uses in its screen display or as an item in a menu or control.</span></span>

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a><span data-ttu-id="7451c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7451c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7451c-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="7451c-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="7451c-108">Nombre único o un valor entero sin signo de 16 bits que identifica el recurso.</span><span class="sxs-lookup"><span data-stu-id="7451c-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="7451c-109"><span id="filename"></span><span id="FILENAME"></span>*extensión*</span><span class="sxs-lookup"><span data-stu-id="7451c-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="7451c-110">Nombre del archivo que contiene el recurso.</span><span class="sxs-lookup"><span data-stu-id="7451c-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="7451c-111">El nombre debe ser un nombre de archivo válido. debe ser una ruta de acceso completa si el archivo no está en el directorio de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="7451c-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="7451c-112">La ruta de acceso debe ser una cadena entre comillas.</span><span class="sxs-lookup"><span data-stu-id="7451c-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="7451c-113">Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="7451c-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="7451c-114">Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="7451c-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7451c-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7451c-115">Examples</span></span>

<span data-ttu-id="7451c-116">En el ejemplo siguiente se definen dos recursos de mapa de bits:</span><span class="sxs-lookup"><span data-stu-id="7451c-116">The following example defines two bitmap resources:</span></span>

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a><span data-ttu-id="7451c-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="7451c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7451c-118">Usar mapas de bits</span><span class="sxs-lookup"><span data-stu-id="7451c-118">Using Bitmaps</span></span>](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[<span data-ttu-id="7451c-119">**LoadBitmap**</span><span class="sxs-lookup"><span data-stu-id="7451c-119">**LoadBitmap**</span></span>](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[<span data-ttu-id="7451c-120">**LoadImage**</span><span class="sxs-lookup"><span data-stu-id="7451c-120">**LoadImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 