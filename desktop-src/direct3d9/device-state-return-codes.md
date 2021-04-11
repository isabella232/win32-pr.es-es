---
description: Una lista de algunos de los códigos de retorno posibles para métodos y funciones.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4146a65e9092dcd3fed261c127e84fe8552128a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274688"
---
# <a name="s_present"></a><span data-ttu-id="4155e-103">S \_ presentes</span><span class="sxs-lookup"><span data-stu-id="4155e-103">S\_PRESENT</span></span>

<span data-ttu-id="4155e-104">Una lista de algunos de los códigos de retorno posibles para métodos y funciones.</span><span class="sxs-lookup"><span data-stu-id="4155e-104">A list of some of the possible return codes for methods and functions.</span></span>



|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4155e-105">\#define</span><span class="sxs-lookup"><span data-stu-id="4155e-105">\#define</span></span>                  | <span data-ttu-id="4155e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="4155e-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="4155e-107">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="4155e-107">S\_OK</span></span>                     | <span data-ttu-id="4155e-108">El dispositivo se está ejecutando con normalidad y se puede usar para la representación.</span><span class="sxs-lookup"><span data-stu-id="4155e-108">The device is running normally and can be used for rendering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="4155e-109">S \_ presente \_ ocluidos</span><span class="sxs-lookup"><span data-stu-id="4155e-109">S\_PRESENT\_OCCLUDED</span></span>      | <span data-ttu-id="4155e-110">El área de presentación es ocluidos.</span><span class="sxs-lookup"><span data-stu-id="4155e-110">The presentation area is occluded.</span></span> <span data-ttu-id="4155e-111">La oclusión significa que la ventana de presentación está minimizada u otro dispositivo entró en el modo de pantalla completa en el mismo monitor que la ventana de presentación y la ventana de presentación está completamente en ese monitor.</span><span class="sxs-lookup"><span data-stu-id="4155e-111">Occlusion means that the presentation window is minimized or another device entered the fullscreen mode on the same monitor as the presentation window and the presentation window is completely on that monitor.</span></span> <span data-ttu-id="4155e-112">La oclusión no se producirá si el área de cliente está incluida en otra ventana.</span><span class="sxs-lookup"><span data-stu-id="4155e-112">Occlusion will not occur if the client area is covered by another Window.</span></span><br/> <span data-ttu-id="4155e-113">Las aplicaciones ocluidos pueden continuar la representación y todas las llamadas se realizarán correctamente, pero la ventana de presentación ocluidos no se actualizará.</span><span class="sxs-lookup"><span data-stu-id="4155e-113">Occluded applications can continue rendering and all calls will succeed, but the occluded presentation window will not be updated.</span></span> <span data-ttu-id="4155e-114">Preferiblemente, la aplicación debe dejar de representar la representación en la ventana de presentación mediante el dispositivo y mantener la llamada a [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) hasta que se cambie el modo de presentación de s \_ o el \_ \_ modo present \_ .</span><span class="sxs-lookup"><span data-stu-id="4155e-114">Preferably the application should stop rendering to the presentation window using the device and keep calling [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) until S\_OK or S\_PRESENT\_MODE\_CHANGED returns.</span></span><br/> |
| <span data-ttu-id="4155e-115">\_modo present \_ \_ cambiado</span><span class="sxs-lookup"><span data-stu-id="4155e-115">S\_PRESENT\_MODE\_CHANGED</span></span> | <span data-ttu-id="4155e-116">Se ha cambiado el modo de presentación del escritorio.</span><span class="sxs-lookup"><span data-stu-id="4155e-116">The desktop display mode has been changed.</span></span> <span data-ttu-id="4155e-117">La aplicación puede continuar con la representación, pero puede haber conversión o ajuste de color.</span><span class="sxs-lookup"><span data-stu-id="4155e-117">The application can continue rendering, but there might be color conversion/stretching.</span></span> <span data-ttu-id="4155e-118">Elija un formato de búfer de reserva similar al modo de presentación actual y llame a restablecer para volver a crear las cadenas de intercambio.</span><span class="sxs-lookup"><span data-stu-id="4155e-118">Pick a back buffer format similar to the current display mode, and call Reset to recreate the swap chains.</span></span> <span data-ttu-id="4155e-119">El dispositivo dejará este estado después de que se llame a RESET.</span><span class="sxs-lookup"><span data-stu-id="4155e-119">The device will leave this state after a Reset is called.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="4155e-120">Otros códigos de error se encuentran en [D3DERR](d3derr.md).</span><span class="sxs-lookup"><span data-stu-id="4155e-120">Other error codes are contained in [D3DERR](d3derr.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4155e-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4155e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4155e-122">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="4155e-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




