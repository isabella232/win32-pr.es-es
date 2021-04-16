---
description: Smart Render Engine
ms.assetid: 279be879-9728-4fa1-bdf7-6b48485fc75f
title: Smart Render Engine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa727397f21aeba754cfe41f2dc4f9c1da1c91b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686366"
---
# <a name="smart-render-engine"></a>Smart Render Engine

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El objeto Smart Render Engine representa la salida comprimida de una escala de tiempo. Para crear este objeto, llame a **CoCreateInstance**. En el caso de la salida sin comprimir, use el motor de representación básico. El identificador de clase es CLSID \_ SmartRenderEngine.

El motor de representación inteligente expone las siguientes interfaces:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   **IObjectWithSite**
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)
-   [**ISmartRenderEngine**](ismartrenderengine.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar un proyecto](rendering-a-project.md)
</dt> <dt>

[Motor de representación básico](basic-render-engine.md)
</dt> </dl>

 

 



