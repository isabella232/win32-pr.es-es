---
title: Acerca del objeto de configuración
description: Acerca del objeto de configuración
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Media Player de Windows, objeto de configuración
- Modelo de objetos de Windows Media Player, objeto de configuración
- modelo de objetos, objeto de configuración
- Control ActiveX de Windows Media Player, objeto de configuración
- Control ActiveX, objeto Settings
- Control ActiveX móvil de Windows Media Player, objeto de configuración
- Windows Media Player Mobile, objeto de configuración
- Objeto de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20dae51d42e6c67a59ddc23dca19bc7f4180001
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903186"
---
# <a name="about-the-settings-object"></a><span data-ttu-id="5f610-111">Acerca del objeto de configuración</span><span class="sxs-lookup"><span data-stu-id="5f610-111">About the Settings Object</span></span>

<span data-ttu-id="5f610-112">El objeto de **configuración** rige los valores del control, como el volumen, el recuento de reproducción, el silencia, etc.</span><span class="sxs-lookup"><span data-stu-id="5f610-112">The **Settings** object governs the settings of the control such as volume, play count, mute, and so on.</span></span> <span data-ttu-id="5f610-113">Solo se tiene acceso a ella a través de la propiedad **Settings** del objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="5f610-113">It is accessed only through the **Settings** property of the **Player** object.</span></span> <span data-ttu-id="5f610-114">La propiedad **Settings** devuelve el objeto de **configuración** .</span><span class="sxs-lookup"><span data-stu-id="5f610-114">The **Settings** property returns the **Settings** object.</span></span> <span data-ttu-id="5f610-115">Solo se puede tener acceso a las propiedades del objeto de **configuración** después de que se haya creado.</span><span class="sxs-lookup"><span data-stu-id="5f610-115">You can only access the properties of the **Settings** object after you have created it.</span></span> <span data-ttu-id="5f610-116">Por ejemplo, para obtener el valor de la propiedad **Volume** , debe usar el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="5f610-116">For example, to get the value of the **Volume** property, you must use the following code:</span></span>


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a><span data-ttu-id="5f610-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f610-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f610-118">**Modelo de objetos del reproductor para lenguajes de scripting**</span><span class="sxs-lookup"><span data-stu-id="5f610-118">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="5f610-119">**Objeto de configuración**</span><span class="sxs-lookup"><span data-stu-id="5f610-119">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 




