---
title: Clave de file_extension
description: Asocia una extensión de nombre de archivo a un ProgID.
ms.assetid: 018998a8-c0da-43ea-bae2-3b184897eb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e602266f3c851975c2f8e008ced5dfc8e2d40b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903857"
---
# <a name="file_extension-key"></a><span data-ttu-id="42a93-103">Clave de> de extensión de archivo <\_</span><span class="sxs-lookup"><span data-stu-id="42a93-103"><file\_extension> Key</span></span>

<span data-ttu-id="42a93-104">Asocia una extensión de nombre de archivo a un ProgID.</span><span class="sxs-lookup"><span data-stu-id="42a93-104">Associates a file name extension with a ProgID.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="42a93-105">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="42a93-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a><span data-ttu-id="42a93-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42a93-106">Remarks</span></span>

<span data-ttu-id="42a93-107">La información contenida en la clave de extensión de nombre de archivo la usan el explorador de Windows y los monikers de archivo.</span><span class="sxs-lookup"><span data-stu-id="42a93-107">The information contained in the file name extension key is used by both the Windows Explorer and file monikers.</span></span> <span data-ttu-id="42a93-108">[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) usa la clave de extensión de nombre de archivo para proporcionar el CLSID asociado.</span><span class="sxs-lookup"><span data-stu-id="42a93-108">[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) uses the file name extension key to supply the associated CLSID.</span></span>

<span data-ttu-id="42a93-109">La clave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde a la clave **\_ \_ raíz de las clases HKEY** , que se conserva por compatibilidad con versiones anteriores de com.</span><span class="sxs-lookup"><span data-stu-id="42a93-109">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42a93-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42a93-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42a93-111">**FileType**</span><span class="sxs-lookup"><span data-stu-id="42a93-111">**FileType**</span></span>](filetype-key.md)
</dt> <dt>

[<span data-ttu-id="42a93-112">**GetClassFile**</span><span class="sxs-lookup"><span data-stu-id="42a93-112">**GetClassFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




