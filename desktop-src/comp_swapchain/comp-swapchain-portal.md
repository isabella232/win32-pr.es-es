---
title: Cadena de intercambio de composición
description: Esta API es la versión pública inicial de composition swapchain API
keywords:
- Cadena de intercambio de composición
- API de cadena de intercambio de composición
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 33e4fe0f57126fc90c38c099ff7d696ce13dc570
ms.sourcegitcommit: b1f058e2360e54c07cb988a3204ec33f47889122
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/05/2021
ms.locfileid: "129454571"
---
# <a name="composition-swapchain"></a>Cadena de intercambio de composición

## <a name="overview"></a>Información general

Esta API es la versión pública inicial de la API de intercambio de composición. Permite a las aplicaciones que usan las API de Composición (como [**Windows.UI.Composition**](/uwp/api/windows.ui.composition) y [**DirectComposition)**](/windows/win32/directcomp/directcomposition-portal)hospedar contenido que se puede representar y presentar de forma independiente. En muchos sentidos, este tipo de contenido presentado es conceptualmente similar a una cadena de intercambio DXGI. Ambos ofrecen la capacidad de representar en un búfer y, a continuación, presentar ese búfer en la pantalla. Sin embargo, la API de cadena de intercambio de composición ofrece la posibilidad de que los presentes se desenríen a una hora específica para que aparezca (la hora *PresentAt),* mientras que DXGI no, y la API de cadena de intercambio de composición ofrece más libertad que DXGI en cuanto al orden de los búferes disponibles para presentarse.

El objetivo de la versión inicial de esta API es habilitar marcos multimedia, como [Windows Media Foundation](/windows/win32/medfound/microsoft-media-foundation-sdk), para usar eficazmente la presentación con tiempo.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Guía de programación de cadenas de intercambio de composición](comp-swapchain.md) | Esta API es una sucesora de la cadena de intercambio DXGI, que permite a las aplicaciones representar y presentar contenido en la pantalla. |
| [Ejemplos de código de cadena de intercambio de composición](comp-swapchain-examples.md) | Colección de ejemplos de código que muestran varios escenarios de cadena de intercambio de composición. |
| [Glosario de composición](comp-swapchain-glossary.md) | Glosario de términos de cadena de intercambio de composición. |
