---
description: La propiedad DVDAdm. BookmarkOnStop establece o recupera un valor que indica al objeto MSWebDVD si se debe guardar automáticamente un marcador de la configuración y la ubicación actuales cuando el usuario hace clic en el botón detener.
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: Propiedad BookmarkOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355ae01c43ef28a086c76f4716fe3d46d250fbe4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152514"
---
# <a name="bookmarkonstop-property"></a><span data-ttu-id="7daeb-103">Propiedad BookmarkOnStop</span><span class="sxs-lookup"><span data-stu-id="7daeb-103">BookmarkOnStop Property</span></span>

<span data-ttu-id="7daeb-104">La `DVDAdm.BookmarkOnStop` propiedad establece o recupera un valor que indica al objeto MSWebDVD si desea guardar automáticamente un marcador de la configuración y la ubicación actuales cuando el usuario hace clic en el botón **detener** .</span><span class="sxs-lookup"><span data-stu-id="7daeb-104">The `DVDAdm.BookmarkOnStop` property sets or retrieves a value that tells the MSWebDVD object whether to automatically save a bookmark of the current location and settings when the user clicks the **Stop** button.</span></span>

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a><span data-ttu-id="7daeb-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7daeb-105">Return Value</span></span>

<span data-ttu-id="7daeb-106">Devuelve un valor booleano que indica si el objeto MSDVDAdm guardará un marcador de toda la configuración de DVD, incluida la posición en el disco, el nivel parental y el país o región parental.</span><span class="sxs-lookup"><span data-stu-id="7daeb-106">Returns a Boolean value indicating whether the MSDVDAdm object will save a bookmark of all DVD settings including position on disc, parental level and parental country/region.</span></span>

## <a name="remarks"></a><span data-ttu-id="7daeb-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7daeb-107">Remarks</span></span>

<span data-ttu-id="7daeb-108">Esta propiedad es de lectura/escritura y su valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="7daeb-108">This property is read/write with a default value of false.</span></span>

<span data-ttu-id="7daeb-109">Los marcadores solo son válidos para un equipo determinado.</span><span class="sxs-lookup"><span data-stu-id="7daeb-109">Bookmarks are valid only for a particular machine.</span></span> <span data-ttu-id="7daeb-110">Un usuario no puede guardar un marcador y, a continuación, enviarlo a otra persona para que lo lea en otro equipo.</span><span class="sxs-lookup"><span data-stu-id="7daeb-110">A user cannot save a bookmark and then send it to someone else to read on a different machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="7daeb-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="7daeb-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7daeb-112">**BookmarkOnClose**</span><span class="sxs-lookup"><span data-stu-id="7daeb-112">**BookmarkOnClose**</span></span>](bookmarkonclose-property.md)
</dt> <dt>

[<span data-ttu-id="7daeb-113">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="7daeb-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



