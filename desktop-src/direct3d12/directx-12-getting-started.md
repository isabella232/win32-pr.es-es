---
title: Descripción de Direct3D 12
description: Para escribir juegos y aplicaciones 3D para Windows 10 y Windows 10 Mobile, debe comprender los aspectos básicos de la tecnología Direct3D 12 y cómo prepararse para usarlos en sus juegos y aplicaciones.
ms.assetid: DED7A434-FCD4-4F41-8B2C-E5AE6E48430F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1353c8c66fd401e364b9db302463f164f757c9ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549181"
---
# <a name="understanding-direct3d-12"></a><span data-ttu-id="3b0b5-103">Descripción de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3b0b5-103">Understanding Direct3D 12</span></span>

<span data-ttu-id="3b0b5-104">Para escribir juegos y aplicaciones 3D para Windows 10 y Windows 10 Mobile, debe comprender los aspectos básicos de la tecnología Direct3D 12 y cómo prepararse para usarlos en sus juegos y aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="3b0b5-104">To write 3D games and apps for Windows 10 and Windows 10 Mobile, you must understand the basics of the Direct3D 12 technology, and how to prepare to use it in your games and apps.</span></span>

<span data-ttu-id="3b0b5-105">Use los temas de esta sección para configurar y obtener información sobre el entorno en el que programará sus aplicaciones y juegos con Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="3b0b5-105">Use the topics in this section to set up and learn about the environment in which you will program your apps and games with Direct3D 12.</span></span> <span data-ttu-id="3b0b5-106">Este contenido también le ayudará a trasladar sus aplicaciones y juegos de Direct3D 11 a Direct3D 12, de modo que pueda aprovechar las características y las eficiencias de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="3b0b5-106">This content will also help you to port your Direct3D 11 apps and games to Direct3D 12, so you can take advantage of Direct3D 12 features and efficiencies.</span></span>

<span data-ttu-id="3b0b5-107">Para programar con Direct3D 12, necesita estos componentes:</span><span class="sxs-lookup"><span data-stu-id="3b0b5-107">To program with Direct3D 12, you need these components:</span></span>

-   <span data-ttu-id="3b0b5-108">Una plataforma de hardware con una GPU compatible con Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3b0b5-108">A hardware platform with a Direct3D 12-compatible GPU</span></span>
-   <span data-ttu-id="3b0b5-109">[Mostrar los controladores](/previous-versions//ff569172(v=vs.85)) que admiten el modelo de controladores de pantalla de Windows (WDDM) 2,0</span><span class="sxs-lookup"><span data-stu-id="3b0b5-109">[Display drivers](/previous-versions//ff569172(v=vs.85)) that support the Windows Display Driver Model (WDDM) 2.0</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3b0b5-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="3b0b5-110">In this section</span></span>



| <span data-ttu-id="3b0b5-111">Tema</span><span class="sxs-lookup"><span data-stu-id="3b0b5-111">Topic</span></span>                                                                                                               | <span data-ttu-id="3b0b5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b0b5-112">Description</span></span>                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b0b5-113">Configuración del entorno de programación de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3b0b5-113">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)<br/>               | <span data-ttu-id="3b0b5-114">Describe la instalación, las herramientas y las bibliotecas admitidas que componen un entorno de desarrollo de Direct3D 12 productivo.</span><span class="sxs-lookup"><span data-stu-id="3b0b5-114">Describes the installation, tools and supported libraries that make up a productive Direct3D 12 development environment.</span></span> <br/>                              |
| [<span data-ttu-id="3b0b5-115">Crear un componente básico de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3b0b5-115">Creating a Basic Direct3D 12 Component</span></span>](creating-a-basic-direct3d-12-component.md)<br/>                     | <span data-ttu-id="3b0b5-116">En este tema se describe el flujo de llamadas para crear un componente básico de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="3b0b5-116">This topic describes the call flow to create a basic Direct3D 12 component.</span></span><br/>                                                                            |
| [<span data-ttu-id="3b0b5-117">Cambios importantes de Direct3D 11 a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3b0b5-117">Important Changes from Direct3D 11 to Direct3D 12</span></span>](important-changes-from-directx-11-to-directx-12.md)<br/> | <span data-ttu-id="3b0b5-118">Direct3D 12 representa una salida significativa del modelo de programación de Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="3b0b5-118">Direct3D 12 represents a significant departure from the Direct3D 11 programming model.</span></span> <span data-ttu-id="3b0b5-119">Direct3D 12 permite que las aplicaciones se acerquen más al hardware que nunca.</span><span class="sxs-lookup"><span data-stu-id="3b0b5-119">Direct3D 12 lets apps get closer to hardware than ever before.</span></span> <br/> |
| [<span data-ttu-id="3b0b5-120">Niveles de características de hardware</span><span class="sxs-lookup"><span data-stu-id="3b0b5-120">Hardware Feature Levels</span></span>](hardware-feature-levels.md)<br/>                                                   | <span data-ttu-id="3b0b5-121">Describe la funcionalidad de los \_ niveles de características de hardware 11 0 a 12 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="3b0b5-121">Describes the functionality of the 11\_0 through 12\_1 hardware feature levels.</span></span><br/>                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="3b0b5-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b0b5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b0b5-123">Guía de programación de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3b0b5-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

