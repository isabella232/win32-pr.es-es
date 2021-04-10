---
title: Trasladar funciones de comentarios
description: Con IRIS GL, el modo en que se trata la información se diferencia según el equipo que ejecuta IRIS GL.
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- Migración de la contabilidad de IRIS, comentarios
- portabilidad de IRIS GL, comentarios
- trasladar a OpenGL desde IRIS GL, comentarios
- Exportación de OpenGL desde IRIS GL, comentarios
- feedback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a04bcfe2c1d914a178ad7ad0dca95fb85d86bbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269168"
---
# <a name="porting-feedback-functions"></a><span data-ttu-id="34aec-108">Trasladar funciones de comentarios</span><span class="sxs-lookup"><span data-stu-id="34aec-108">Porting Feedback Functions</span></span>

<span data-ttu-id="34aec-109">Con IRIS GL, el modo en que se trata la información se diferencia según el equipo que ejecuta IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="34aec-109">With IRIS GL, the way that feedback is handled differs depending on the computer running IRIS GL.</span></span> <span data-ttu-id="34aec-110">OpenGL normaliza las funciones de comentarios para que pueda confiar en la información coherente entre varias plataformas de hardware.</span><span class="sxs-lookup"><span data-stu-id="34aec-110">OpenGL standardizes feedback functions so you can rely on consistent feedback among various hardware platforms.</span></span> <span data-ttu-id="34aec-111">En la tabla siguiente se enumeran las funciones de comentarios de la contabilidad de IRIS y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="34aec-111">The following table lists the IRIS GL feedback functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="34aec-112">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="34aec-112">IRIS GL function</span></span> | <span data-ttu-id="34aec-113">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="34aec-113">OpenGL function</span></span>                                                                                            | <span data-ttu-id="34aec-114">Significado</span><span class="sxs-lookup"><span data-stu-id="34aec-114">Meaning</span></span>                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="34aec-115">**los**</span><span class="sxs-lookup"><span data-stu-id="34aec-115">**feedback**</span></span>     | <span data-ttu-id="34aec-116">[**glRenderMode**](glrendermode.md) (comentarios de contabilidad \_ )</span><span class="sxs-lookup"><span data-stu-id="34aec-116">[**glRenderMode**](glrendermode.md) ( GL\_FEEDBACK )</span></span>                                                      | <span data-ttu-id="34aec-117">Cambia al modo de comentarios.</span><span class="sxs-lookup"><span data-stu-id="34aec-117">Switches to feedback mode.</span></span>                    |
| <span data-ttu-id="34aec-118">**endfeedback**</span><span class="sxs-lookup"><span data-stu-id="34aec-118">**endfeedback**</span></span>  | <span data-ttu-id="34aec-119">[**glRenderMode**](glrendermode.md) (representación en GL \_ )[**glFeedbackBuffer**](glfeedbackbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="34aec-119">[**glRenderMode**](glrendermode.md) ( GL\_RENDER )[**glFeedbackBuffer**](glfeedbackbuffer.md)</span></span><br/> | <span data-ttu-id="34aec-120">Cambia al modo de representación.</span><span class="sxs-lookup"><span data-stu-id="34aec-120">Switches to rendering mode.</span></span>                   |
| <span data-ttu-id="34aec-121">**acceso directo**</span><span class="sxs-lookup"><span data-stu-id="34aec-121">**passthrough**</span></span>  | [<span data-ttu-id="34aec-122">**glPassThrough**</span><span class="sxs-lookup"><span data-stu-id="34aec-122">**glPassThrough**</span></span>](glpassthrough.md)                                                                     | <span data-ttu-id="34aec-123">Coloca un marcador de token en el búfer de comentarios.</span><span class="sxs-lookup"><span data-stu-id="34aec-123">Places a token marker in the feedback buffer.</span></span> |



 

 

 





