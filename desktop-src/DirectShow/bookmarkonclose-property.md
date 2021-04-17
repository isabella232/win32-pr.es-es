---
description: La propiedad DVDAdm. BookmarkOnClose establece o recupera un valor que indica al objeto MSDVDAdm si se debe guardar automáticamente un marcador de la configuración y la ubicación actuales cuando el usuario cierra la aplicación.
ms.assetid: 54901ad6-7989-4fb3-bb28-f54c7a2bca44
title: Propiedad BookmarkOnClose
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfbbfe194a496dba3568b7dfa4d75b97d4ed57c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359984"
---
# <a name="bookmarkonclose-property"></a><span data-ttu-id="d23d9-103">Propiedad BookmarkOnClose</span><span class="sxs-lookup"><span data-stu-id="d23d9-103">BookmarkOnClose Property</span></span>

> [!Note]  
> <span data-ttu-id="d23d9-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d23d9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d23d9-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="d23d9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d23d9-106">La `DVDAdm.BookmarkOnClose` propiedad establece o recupera un valor que indica al objeto MSDVDAdm si se debe guardar automáticamente un marcador de la configuración y la ubicación actuales cuando el usuario cierra la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d23d9-106">The `DVDAdm.BookmarkOnClose` property sets or retrieves a value that tells the MSDVDAdm object whether to automatically save a bookmark of the current location and settings when the user closes the application.</span></span>

``` syntax
[ bBookmarkOnClose = ] DVD.DVDAdm.BookmarkOnClose
```

## <a name="return-value"></a><span data-ttu-id="d23d9-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d23d9-107">Return Value</span></span>

<span data-ttu-id="d23d9-108">Devuelve un valor booleano que, si es true, indica que el control MSDVDAdm guardará un marcador de toda la configuración de DVD, incluida la posición en el disco, el nivel parental y el país o la región parental cuando el usuario cierra la aplicación del reproductor de DVD.</span><span class="sxs-lookup"><span data-stu-id="d23d9-108">Returns a Boolean value, which if true, indicates that the MSDVDAdm control will save a bookmark of all DVD settings, including position on disc, parental level, and parental country/region when the user closes the DVD player application.</span></span>

## <a name="remarks"></a><span data-ttu-id="d23d9-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d23d9-109">Remarks</span></span>

<span data-ttu-id="d23d9-110">Esta propiedad es de lectura/escritura y su valor predeterminado es true.</span><span class="sxs-lookup"><span data-stu-id="d23d9-110">This property is read/write with a default value of true.</span></span>

## <a name="see-also"></a><span data-ttu-id="d23d9-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="d23d9-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d23d9-112">**BookmarkOnStop**</span><span class="sxs-lookup"><span data-stu-id="d23d9-112">**BookmarkOnStop**</span></span>](bookmarkonstop-property.md)
</dt> <dt>

[<span data-ttu-id="d23d9-113">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="d23d9-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



