---
description: Motor de representación básico
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Motor de representación básico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9b51240b43c58de99b7d6fe1f7ad61f754c7ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161695"
---
# <a name="basic-render-engine"></a>Motor de representación básico

> [!Note]  
> \[En desuso. Esta API puede quitarse de futuras versiones de Windows.\]

 

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

 

 



