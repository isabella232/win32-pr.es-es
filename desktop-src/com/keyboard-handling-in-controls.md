---
title: Control de teclado en controles
description: Control de teclado en controles
ms.assetid: 33affb3f-5d52-4ada-9751-0775b31a375e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f32610732ddbf88c6a587d5bc0fd7de1188152d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704797"
---
# <a name="keyboard-handling-in-controls"></a><span data-ttu-id="a3f8d-103">Control de teclado en controles</span><span class="sxs-lookup"><span data-stu-id="a3f8d-103">Keyboard Handling in Controls</span></span>

<span data-ttu-id="a3f8d-104">Se recomienda encarecidamente la compatibilidad con la administración de teclado para la siguiente funcionalidad, aunque se reconoce que no es aplicable a todos los contenedores.</span><span class="sxs-lookup"><span data-stu-id="a3f8d-104">Keyboard handling support for the following functionality is strongly recommended, although it is recognized that it is not applicable to all containers.</span></span>

-   <span data-ttu-id="a3f8d-105">Compatibilidad con los \_ bits de estado OLEMISC ACTSLIKELABEL y OLEMISC \_ ACTSLIKEBUTTON.</span><span class="sxs-lookup"><span data-stu-id="a3f8d-105">Support for OLEMISC\_ACTSLIKELABEL and OLEMISC\_ACTSLIKEBUTTON status bits.</span></span>
-   <span data-ttu-id="a3f8d-106">Implementar la propiedad de ambiente DisplayAsDefault (si existe, puede devolver **false**).</span><span class="sxs-lookup"><span data-stu-id="a3f8d-106">Implementing the DisplayAsDefault ambient property (if it exists, it can return **FALSE**).</span></span>
-   <span data-ttu-id="a3f8d-107">Implementar el control de pestañas, incluido el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="a3f8d-107">Implementing tab handling, including tab order.</span></span>

<span data-ttu-id="a3f8d-108">Algunos contenedores usarán controles ActiveX en escenarios de documentos compuestos tradicionales.</span><span class="sxs-lookup"><span data-stu-id="a3f8d-108">Some containers will use ActiveX controls in traditional compound document scenarios.</span></span> <span data-ttu-id="a3f8d-109">Por ejemplo, una hoja de cálculo puede permitir que un usuario inserte un control ActiveX en una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="a3f8d-109">For example, a spreadsheet may allow a user to embed an ActiveX control into a worksheet.</span></span> <span data-ttu-id="a3f8d-110">En estos escenarios, el contenedor haría la administración del teclado de manera diferente, porque la interfaz de teclado debe ser coherente con las expectativas del usuario de una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="a3f8d-110">In such scenarios, the container would do keyboard handling differently, because the keyboard interface should remain consistent with the user's expectations of a spreadsheet.</span></span> <span data-ttu-id="a3f8d-111">La documentación de estos productos debe informar a los usuarios de las diferencias en el control de los controles en estos diferentes escenarios.</span><span class="sxs-lookup"><span data-stu-id="a3f8d-111">Documentation for such products should inform users of differences in control handling in these different scenarios.</span></span> <span data-ttu-id="a3f8d-112">Otros contenedores deben intentar respetar correctamente la funcionalidad anterior, incluido el control de teclas de tecla.</span><span class="sxs-lookup"><span data-stu-id="a3f8d-112">Other containers should endeavor to honor the above functionality correctly, including Mnemonic handling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3f8d-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3f8d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3f8d-114">Contenedores</span><span class="sxs-lookup"><span data-stu-id="a3f8d-114">Containers</span></span>](containers.md)
</dt> </dl>

 

 




