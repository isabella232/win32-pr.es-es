---
title: El método SetInfo
description: El método SetInfo de IADs guarda los valores actuales de las propiedades de este Active Directory objeto desde la memoria caché de propiedades hasta el almacén de directorios subyacente. Esto es análogo a vaciar un búfer en el disco.
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- SetInfo ADSI, usar
- propiedades ADSI, guardar los valores actuales de las propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5965a46e5accd2a00adc006fe37511de13ff0df3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356690"
---
# <a name="the-setinfo-method"></a><span data-ttu-id="ac8bd-106">El método SetInfo</span><span class="sxs-lookup"><span data-stu-id="ac8bd-106">The SetInfo Method</span></span>

<span data-ttu-id="ac8bd-107">El método [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) guarda los valores actuales de las propiedades de este objeto Active Directory de la caché de propiedades en el almacén de directorios subyacente.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-107">The [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method saves the current values for the properties for this Active Directory object from the property cache to the underlying directory store.</span></span> <span data-ttu-id="ac8bd-108">Esto es análogo a vaciar un búfer en el disco.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-108">This is analogous to flushing a buffer out to disk.</span></span>

<span data-ttu-id="ac8bd-109">[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) actualiza los objetos que ya existen en el directorio o crea una nueva entrada de directorio para los objetos recién creados.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-109">[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) updates objects that already exist in the directory, or create a new directory entry for newly created objects.</span></span>

<span data-ttu-id="ac8bd-110">En el momento de la llamada a [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , si se ha escrito algún valor de la caché de propiedades con un código de control [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) , como la propiedad ADS \_ \_ Update o la \_ propiedad ADS \_ Clear, se pasan las solicitudes adecuadas al servicio de directorio subyacente.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-110">At the time of the [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) call, if any property cache values have been written with a [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) control code, such as ADS\_PROPERTY\_UPDATE or ADS\_PROPERTY\_CLEAR, then the appropriate requests are passed on to the underlying directory service.</span></span>

 

 




