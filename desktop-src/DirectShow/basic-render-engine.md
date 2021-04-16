---
description: Motor de representación básico
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Motor de representación básico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9b51240b43c58de99b7d6fe1f7ad61f754c7ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537816"
---
# <a name="basic-render-engine"></a>Motor de representación básico

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El objeto de motor de representación básico representa la salida sin comprimir de una escala de tiempo. Para crear este objeto, llame a **CoCreateInstance**. Para la salida comprimida, use el motor de representación inteligente. El identificador de clase es CLSID \_ RenderEngine.

El motor de representación básico expone las siguientes interfaces:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   IObjectWithSite
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar un proyecto](rendering-a-project.md)
</dt> <dt>

[Smart Render Engine](smart-render-engine.md)
</dt> </dl>

 

 



