---
title: Configuración del registro de la adquisición silenciosa
description: Configuración del registro de la adquisición silenciosa
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a00bbb6d930cb137ed12ffbcb05af31cee3c99c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704726"
---
# <a name="silent-acquisition-registry-setting"></a><span data-ttu-id="7c91e-103">Configuración del registro de la adquisición silenciosa</span><span class="sxs-lookup"><span data-stu-id="7c91e-103">Silent Acquisition Registry Setting</span></span>

<span data-ttu-id="7c91e-104">Microsoft Windows Media Player usa el siguiente valor del registro para determinar si se debe habilitar la adquisición silenciosa, un estado en el que el reproductor descarga los derechos de uso automáticamente cuando el usuario reproduce o sincroniza el contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="7c91e-104">Microsoft Windows Media Player uses the following registry value to determine whether to enable silent acquisition, a state in which the player downloads usage rights automatically when the user plays or syncs protected content.</span></span>

<span data-ttu-id="7c91e-105">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **MediaPlayer** \\ **Preferences** \\ **SilentAcquisition**</span><span class="sxs-lookup"><span data-stu-id="7c91e-105">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**MediaPlayer**\\**Preferences**\\**SilentAcquisition**</span></span>

<span data-ttu-id="7c91e-106">El valor de SilentAcquisition tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="7c91e-106">The SilentAcquisition value has the following form:</span></span>



| <span data-ttu-id="7c91e-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="7c91e-107">Name</span></span>              | <span data-ttu-id="7c91e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c91e-108">Type</span></span>           | <span data-ttu-id="7c91e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c91e-109">Description</span></span>                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c91e-110">SilentAcquisition</span><span class="sxs-lookup"><span data-stu-id="7c91e-110">SilentAcquisition</span></span> | <span data-ttu-id="7c91e-111">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="7c91e-111">**REG\_DWORD**</span></span> | <span data-ttu-id="7c91e-112">Establezca este valor en 1 para habilitar la adquisición silenciosa o establézcalo en 0 para deshabilitar la adquisición silenciosa.</span><span class="sxs-lookup"><span data-stu-id="7c91e-112">Set this value to 1 to enable silent acquisition, or set it to 0 to disable silent acquisition.</span></span> <span data-ttu-id="7c91e-113">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="7c91e-113">The default is 1.</span></span> |



 

<span data-ttu-id="7c91e-114">Para especificar un valor, el usuario puede iniciar Windows Media Player, abrir el cuadro de diálogo **Opciones** , hacer clic en la pestaña **privacidad** y, a continuación, activar o desactivar la casilla **descargar los derechos de uso automáticamente al reproducir o sincronizar un archivo** .</span><span class="sxs-lookup"><span data-stu-id="7c91e-114">To specify a value, the user can start Windows Media Player, open the **Options** dialog box, click the **Privacy** tab, and then select or clear the **Download usage rights automatically when I play or sync a file** check box.</span></span> <span data-ttu-id="7c91e-115">Al activar esta casilla, se establece SilentAcquisition en 1; al desactivar la casilla, se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="7c91e-115">Selecting this check box sets SilentAcquisition to 1; clearing the check box sets it to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c91e-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c91e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c91e-117">**Configuración del registro**</span><span class="sxs-lookup"><span data-stu-id="7c91e-117">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




