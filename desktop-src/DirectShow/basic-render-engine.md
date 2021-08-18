---
description: Motor de representación básico
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Motor de representación básico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a3e04e1ad32c163db93794e075ff7933f041c3270ab8412cbd5b5a68b4a763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955583"
---
# <a name="basic-render-engine"></a>Motor de representación básico

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El objeto Basic Render Engine representa la salida sin comprimir de una escala de tiempo. Para crear este objeto, llame a **CoCreateInstance**. Para la salida comprimida, use el motor de representación inteligente. El identificador de clase es CLSID \_ RenderEngine.

El motor de representación básico expone las interfaces siguientes:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   IObjectWithSite
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de un Project](rendering-a-project.md)
</dt> <dt>

[Motor de representación inteligente](smart-render-engine.md)
</dt> </dl>

 

 



