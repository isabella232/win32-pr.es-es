---
title: Personalizar el complemento de la interfaz de usuario
description: Personalizar el complemento de la interfaz de usuario
ms.assetid: d961ed18-ba14-45af-90d3-b1e38dc53180
keywords:
- Complementos de Windows Media Player, personalizar
- complementos, personalizar
- Complementos de la interfaz de usuario, personalizar
- Complementos de la interfaz de usuario, personalizar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4572c4ce5102443c3100ddd20719fe17fe62ffc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076131"
---
# <a name="customizing-the-ui-plug-in"></a><span data-ttu-id="924cb-107">Personalizar el complemento de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="924cb-107">Customizing the UI Plug-in</span></span>

<span data-ttu-id="924cb-108">En este momento, el proyecto está listo para la personalización.</span><span class="sxs-lookup"><span data-stu-id="924cb-108">At this point, your project is ready for customization.</span></span> <span data-ttu-id="924cb-109">Puede modificar la implementación generada por el Asistente de la interfaz **IWMPPluginUI** , puede Agregar una interfaz de usuario a la clase **CPluginWindow** y puede implementar una página de propiedades en la clase **CPropertyDialog** .</span><span class="sxs-lookup"><span data-stu-id="924cb-109">You can modify the wizard-generated implementation of the **IWMPPluginUI** interface, you can add a user interface to the **CPluginWindow** class, and you can implement a property page in the **CPropertyDialog** class.</span></span> <span data-ttu-id="924cb-110">Si el complemento está configurado para escuchar eventos de Media Player de Windows, el asistente habrá generado implementaciones predeterminadas o vacías de todos los controladores de eventos necesarios, que también se modifican o se crean.</span><span class="sxs-lookup"><span data-stu-id="924cb-110">If your plug-in is configured to listen to Windows Media Player events, the wizard will have generated default or empty implementations of all the necessary event handlers, which you also modify or create.</span></span>

<span data-ttu-id="924cb-111">El tipo de complemento y las características que admite se indican mediante un valor que se almacena en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="924cb-111">The type of plug-in and the features it supports are indicated by a value which is stored in the Windows registry.</span></span> <span data-ttu-id="924cb-112">El asistente genera un archivo con la extensión de nombre de archivo. RGS que contiene la información para registrar el complemento.</span><span class="sxs-lookup"><span data-stu-id="924cb-112">The wizard generates a file with a .rgs file name extension that contains the information to register the plug-in with.</span></span> <span data-ttu-id="924cb-113">El valor "Capabilities" de este archivo es el equivalente decimal de un booleano o de las constantes de tipo de complemento y las marcas de complemento definidas en wmpplug. h.</span><span class="sxs-lookup"><span data-stu-id="924cb-113">The "Capabilities" value in this file is the decimal equivalent of a Boolean OR of the plug-in type constants and plug-in flags defined in wmpplug.h.</span></span> <span data-ttu-id="924cb-114">Aunque este valor está determinado por las opciones que seleccione en el asistente, debe modificarlo Si desea crear un complemento con varios valores preestablecidos o uno al que se puedan enviar los elementos multimedia o listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="924cb-114">Although this value is determined by the options you select in the wizard, you must modify it if you want to create a plug-in with multiple presets or one that media items or playlists can be sent to.</span></span>

<span data-ttu-id="924cb-115">A medida que modifica y extiende el código de complemento, puede compilar y registrar el archivo DLL para que pueda probar el complemento en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="924cb-115">As you modify and extend your plug-in code, you can build and register your DLL so that you can test your plug-in in Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="924cb-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="924cb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="924cb-117">**Compilar un complemento de IU**</span><span class="sxs-lookup"><span data-stu-id="924cb-117">**Building a UI Plug-in**</span></span>](building-a-ui-plug-in.md)
</dt> </dl>

 

 




