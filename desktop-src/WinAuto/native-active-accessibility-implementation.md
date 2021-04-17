---
title: Implementación de Active Accessibility nativa
description: Se dice que los elementos de la interfaz de usuario que implementan la interfaz IAccessible proporcionan una implementación nativa.
ms.assetid: 36a5c0cd-53f0-433e-8932-da7d1de177dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5f6e6b6152c2f5e5c41a6a2b7cd3f84a3fce373
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704663"
---
# <a name="native-active-accessibility-implementation"></a><span data-ttu-id="97d46-103">Implementación de Active Accessibility nativa</span><span class="sxs-lookup"><span data-stu-id="97d46-103">Native Active Accessibility Implementation</span></span>

<span data-ttu-id="97d46-104">Se dice que los elementos de la interfaz de usuario que implementan la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proporcionan una *implementación nativa*.</span><span class="sxs-lookup"><span data-stu-id="97d46-104">User interface elements that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface are said to provide a *native implementation*.</span></span> <span data-ttu-id="97d46-105">Aunque el costo de desarrollo para implementar **IAccessible** (o cualquier otra interfaz del modelo de objetos componentes (com)) puede ser alto, la ventaja es el control total sobre la información expuesta a los clientes.</span><span class="sxs-lookup"><span data-stu-id="97d46-105">Although the development cost for implementing **IAccessible** (or any other Component Object Model (COM) interface) can be high, the benefit is complete control over the information exposed to clients.</span></span>

<span data-ttu-id="97d46-106">Si la aplicación usa controles personalizados u otros controles que no pueden ser procesados por proxy por Oleacc.dll, deberá proporcionar una implementación nativa.</span><span class="sxs-lookup"><span data-stu-id="97d46-106">If your application uses custom controls or other controls that cannot be proxied by Oleacc.dll, you will need to provide a native implementation.</span></span>

 

 




