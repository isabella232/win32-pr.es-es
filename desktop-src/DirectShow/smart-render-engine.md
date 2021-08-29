---
description: Motor de representación inteligente
ms.assetid: 279be879-9728-4fa1-bdf7-6b48485fc75f
title: Motor de representación inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3472d096d1c3918a9bf1a45ae788a535fd65bfe4e4084c6b044516db01440d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072559"
---
# <a name="smart-render-engine"></a>Motor de representación inteligente

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El objeto Smart Render Engine representa la salida comprimida de una escala de tiempo. Para crear este objeto, llame a **CoCreateInstance**. Para la salida sin comprimir, use el motor de representación básico. El identificador de clase es CLSID \_ SmartRenderEngine.

El motor de representación inteligente expone las interfaces siguientes:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   **IObjectWithSite**
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)
-   [**ISmartRenderEngine**](ismartrenderengine.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de un Project](rendering-a-project.md)
</dt> <dt>

[Motor de representación básico](basic-render-engine.md)
</dt> </dl>

 

 



