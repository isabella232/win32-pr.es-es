---
title: Agregar caracteres de copyright a los metaarchivos
description: Es posible que los caracteres de los símbolos de copyright y de registro de marcas comerciales (\ 169; o \ 174;) no se muestren correctamente si el metarchivo no está codificado con el esquema de codificación UTF-8.
ms.assetid: 9124c8d4-1fc1-4163-ada9-d96af58f8b98
keywords:
- Agregar caracteres de copyright a los metaarchivos de Windows Media Player
topic_type:
- apiref
api_name:
- Adding Copyright Characters to Metafiles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e71b116a3500fdb4217613c81bd4f041af75a66
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358095"
---
# <a name="adding-copyright-characters-to-metafiles"></a><span data-ttu-id="e0e20-104">Agregar caracteres de copyright a los metaarchivos</span><span class="sxs-lookup"><span data-stu-id="e0e20-104">Adding Copyright Characters to Metafiles</span></span>

<span data-ttu-id="e0e20-105">Es posible que los caracteres de los símbolos de copyright y de registro de marcas comerciales (© o®) no se muestren correctamente si el metarchivo no se codifica mediante el esquema de codificación UTF-8.</span><span class="sxs-lookup"><span data-stu-id="e0e20-105">The characters for copyright and trademark registration symbols ( © or ® ) may not display correctly if the metafile is not encoded using the UTF-8 encoding scheme.</span></span> <span data-ttu-id="e0e20-106">En este caso, para mostrar correctamente cualquiera de estos símbolos para todos los usuarios, puede usar los equivalentes ASCII (c) y (r) dentro del elemento **Copyright** , tal como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="e0e20-106">In this case, to display either of these symbols properly for all users, you can use the ASCII equivalents (c) and (r) inside the **COPYRIGHT** element, as shown in the following code.</span></span>


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



<span data-ttu-id="e0e20-107">Si el metarchivo está codificado con UTF-8, los símbolos de copyright y marca comercial se mostrarán correctamente.</span><span class="sxs-lookup"><span data-stu-id="e0e20-107">If the metafile is encoded using UTF-8, copyright and trademark symbols will display correctly.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0e20-108">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0e20-108">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e20-109">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e0e20-109">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




