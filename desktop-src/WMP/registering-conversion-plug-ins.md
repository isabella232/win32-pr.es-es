---
title: Registrar complementos de conversión
description: Registrar complementos de conversión
ms.assetid: d7d6e733-7288-4707-a54a-dcaa71601646
keywords:
- Windows Media Player, Complementos de conversión
- Complementos de Windows Media Player, conversión
- complementos, conversión
- Complementos de conversión, registrar
- registro, Complementos de conversión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301d24e38cb4672936923cea9edd7fe6b3d2dc5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685512"
---
# <a name="registering-conversion-plug-ins"></a><span data-ttu-id="5cc1f-108">Registrar complementos de conversión</span><span class="sxs-lookup"><span data-stu-id="5cc1f-108">Registering Conversion Plug-ins</span></span>

<span data-ttu-id="5cc1f-109">Los formatos de terceros deben registrarse antes de que Windows Media Player pueda crear instancias y usar el complemento de conversión.</span><span class="sxs-lookup"><span data-stu-id="5cc1f-109">Third-party formats must be registered before Windows Media Player can instantiate and use the conversion plug-in.</span></span> <span data-ttu-id="5cc1f-110">Para registrar el archivo para su conversión, debe registrar la extensión de nombre de archivo asociada con el formato.</span><span class="sxs-lookup"><span data-stu-id="5cc1f-110">To register your file for conversion, you must register the file name extension associated with your format.</span></span>

<span data-ttu-id="5cc1f-111">La lista de extensiones de nombre de archivo registradas se mantiene como un conjunto de claves del registro.</span><span class="sxs-lookup"><span data-stu-id="5cc1f-111">The list of registered file name extensions is maintained as a set of registry keys.</span></span> <span data-ttu-id="5cc1f-112">Para obtener más información sobre el registro de formatos de terceros, consulte [configuración del registro](file-name-extension-registry-settings.md)de la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="5cc1f-112">For details about registering third-party formats, see [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="5cc1f-113">En la tabla siguiente se enumeran los valores del valor del registro para registrar un formato de terceros para la conversión mediante un complemento de conversión.</span><span class="sxs-lookup"><span data-stu-id="5cc1f-113">The following table lists the registry value settings to register a third-party format for conversion by using a conversion plug-in.</span></span>



| <span data-ttu-id="5cc1f-114">Value</span><span class="sxs-lookup"><span data-stu-id="5cc1f-114">Value</span></span>                  | <span data-ttu-id="5cc1f-115">Configuración</span><span class="sxs-lookup"><span data-stu-id="5cc1f-115">Setting</span></span>                                                     |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="5cc1f-116">**Tiempo de ejecución**</span><span class="sxs-lookup"><span data-stu-id="5cc1f-116">**Runtime**</span></span>            | <span data-ttu-id="5cc1f-117">13</span><span class="sxs-lookup"><span data-stu-id="5cc1f-117">13</span></span>                                                          |
| <span data-ttu-id="5cc1f-118">**Permisos**</span><span class="sxs-lookup"><span data-stu-id="5cc1f-118">**Permissions**</span></span>        | <span data-ttu-id="5cc1f-119">8 (permiso para la biblioteca).</span><span class="sxs-lookup"><span data-stu-id="5cc1f-119">8 (Permission for the library).</span></span>                             |
| <span data-ttu-id="5cc1f-120">**ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="5cc1f-120">**ConvertPluginCLSID**</span></span> | <span data-ttu-id="5cc1f-121">IDENTIFICADOR de clase del complemento de conversión, en formato de registro.</span><span class="sxs-lookup"><span data-stu-id="5cc1f-121">The class ID of the conversion plug-in, in registry format.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5cc1f-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5cc1f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cc1f-123">**Referencia de programación de complementos de conversión**</span><span class="sxs-lookup"><span data-stu-id="5cc1f-123">**Conversion Plug-ins Programming Reference**</span></span>](conversion-plug-ins-programming-reference.md)
</dt> </dl>

 

 




