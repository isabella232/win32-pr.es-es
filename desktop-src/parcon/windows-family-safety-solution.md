---
description: Solución de seguridad para la familia Windows
ms.assetid: b89cf0c7-bf9f-4bcb-b008-8b7c792f3300
title: Solución de seguridad para la familia Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2d8776893468df4f4877c7220436f505ab1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649256"
---
# <a name="windows-family-safety-solution"></a><span data-ttu-id="31d46-103">Solución de seguridad para la familia Windows</span><span class="sxs-lookup"><span data-stu-id="31d46-103">Windows Family Safety Solution</span></span>

<span data-ttu-id="31d46-104">Los requisitos clave definidos por Microsoft para una solución más completa son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="31d46-104">Key requirements defined by Microsoft for a more comprehensive solution are as follows.</span></span> <span data-ttu-id="31d46-105">Tenga en cuenta que la definición de en línea es una tecnología principalmente orientada a Internet, a diferencia de un cliente sin conexión que normalmente está limitado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="31d46-105">Note the definition for online is a primarily Internet-facing technology, unlike an offline client which is usually bounded at the computer.</span></span>

-   <span data-ttu-id="31d46-106">Proporcionan un área única y fácil de encontrar en la interfaz de usuario del sistema operativo donde se pueden detectar fácilmente todas las directivas de controles parentales, el control de la supervisión de la actividad y los datos de actividad de una identidad.</span><span class="sxs-lookup"><span data-stu-id="31d46-106">Provide a single, easy to find area in the operating system user interface where all parental controls policies, control of activity monitoring, and activity data for an identity may be readily discovered.</span></span>

-   <span data-ttu-id="31d46-107">Admitir la supervisión de la actividad suficiente del usuario controlado para que un padre o tutor tenga una confianza razonable de que se puedan detectar actividades de riesgo.</span><span class="sxs-lookup"><span data-stu-id="31d46-107">Support monitoring of sufficient activity of the controlled user so that a parent or guardian has reasonable confidence that risky activities may be discovered.</span></span> <span data-ttu-id="31d46-108">Además, registre la reconfiguración de las directivas del usuario controlado para que los cambios no deseados o no autorizados sean reconocibles.</span><span class="sxs-lookup"><span data-stu-id="31d46-108">Also, log reconfiguration of the controlled user's policies so that unintended or unauthorized changes are discoverable.</span></span>

-   <span data-ttu-id="31d46-109">Exponga las capacidades de supervisión de actividades a través de las interfaces estándar de registro de eventos de Windows Vista y proporcione una solución de visor integrada.</span><span class="sxs-lookup"><span data-stu-id="31d46-109">Expose activity monitoring capabilities through standard Windows Vista event logging interfaces, and provide an in-box viewer solution.</span></span> <span data-ttu-id="31d46-110">Defina los eventos de actividad estándar y proporcione extensibilidad a la generación de eventos personalizados por parte de los ISV.</span><span class="sxs-lookup"><span data-stu-id="31d46-110">Define standard activity events, and provide for extensibility to custom event generation by ISVs.</span></span>

-   <span data-ttu-id="31d46-111">Promueva que toda la supervisión y las restricciones de un usuario se activen solo en función de los padres o tutores.</span><span class="sxs-lookup"><span data-stu-id="31d46-111">Promote that all monitoring and restrictions for a user are turned on only on an opt-in basis by parents or guardians.</span></span> <span data-ttu-id="31d46-112">Siempre que sea posible, la funcionalidad de restricciones debe estar completamente inactiva para los usuarios no controlados con el fin de minimizar los riesgos de seguridad y compatibilidad de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="31d46-112">Wherever possible, restrictions functionality should be completely inactive for non-controlled users to minimize security and application compatibility risks.</span></span>

-   <span data-ttu-id="31d46-113">Microsoft procurará, siempre que sea posible, no realizar resoluciones de valor por edad u otros parámetros para el usuario controlado (es posible que otros fabricantes decidan hacerlo).</span><span class="sxs-lookup"><span data-stu-id="31d46-113">Microsoft shall strive, whenever possible, not to make value judgments by age or other parameters for the controlled user (third parties may choose to do so).</span></span> <span data-ttu-id="31d46-114">Dichas decisiones se dejan al padre o a la protección, que a menudo se ven afectadas por comunidades u organizaciones.</span><span class="sxs-lookup"><span data-stu-id="31d46-114">Such decisions are left up to the parent or guardian, often influenced by communities or organizations.</span></span>

-   <span data-ttu-id="31d46-115">Proporcionar implementaciones en el producto para la supervisión de actividades sin conexión y las restricciones en las que las ofertas o no están disponibles hoy en día, donde la funcionalidad de riesgo de seguridad asociada está disponible en el producto, o en los casos en los que una solución de Microsoft proporciona una funcionalidad compatible y sólida totalmente integrada con el diseño del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="31d46-115">Provide implementations in the product for offline activity monitoring and restrictions where few or no offerings are available today, where the associated safety-risk functionality is available in the product, or where a Microsoft solution provides capable and robust functionality fully integrated with the design of the operating system.</span></span>

-   <span data-ttu-id="31d46-116">Por lo general, promueva que las aplicaciones realicen sus propios registros y restricciones para obtener una mejor experiencia de contexto y de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="31d46-116">Generally, promote that applications perform their own logging and restrictions for best context and UI experience.</span></span>

    <span data-ttu-id="31d46-117">Excepción: proporcione una supervisión y restricciones completas de la actividad en línea en áreas seleccionadas en las que la ventaja de los consumidores y del sector supere los costos.</span><span class="sxs-lookup"><span data-stu-id="31d46-117">Exception: Provide comprehensive online activity monitoring and restrictions in selected areas where the benefit to consumers and industry outweigh the costs.</span></span>

-   <span data-ttu-id="31d46-118">Exponga la configuración de la interfaz de usuario de controles parentales y las definiciones de eventos de actividad mediante el uso de API públicas para que otros usuarios puedan consultar el estado, modificar la configuración y leer los registros de actividad si se ejecutan con suficientes privilegios de cuenta de Windows.</span><span class="sxs-lookup"><span data-stu-id="31d46-118">Expose parental controls user interface settings and activity event definitions by using public APIs so that third parties may query for state, modify settings, and read activity logs if they are running with sufficient Windows account privileges.</span></span>

<span data-ttu-id="31d46-119">Un objetivo general es promover la coexistencia de soluciones de controles parentales de terceros con la funcionalidad integrada y permitir agregar valor mediante la integración con, la extensión o el suministro de funcionalidades alternativas cuando sea adecuado.</span><span class="sxs-lookup"><span data-stu-id="31d46-119">An overarching goal is to promote third-party parental controls solutions' coexistence with the in-box functionality, and support adding value by integrating with, extending, or providing alternative capabilities where suitable.</span></span>

 

 



