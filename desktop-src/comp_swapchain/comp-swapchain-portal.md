---
title: Cadena de intercambio de composición
description: Esta API es la versión pública inicial de la API de intercambio de composición.
keywords:
- Cadena de intercambio de composición
- API de intercambio de composición
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: a8c03448333a9bb1b2c6b2b3b1c64b51be9dbada
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128524018"
---
# <a name="composition-swapchain"></a>Cadena de intercambio de composición

> [!NOTE]
> **Parte de la información hace referencia al producto de versión preliminar, el cual puede sufrir importantes modificaciones antes de que se publique la versión comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.**

## <a name="overview"></a>Información general

Esta API es la versión pública inicial de la API de intercambio de composición. Permite a las aplicaciones que usan las API de Composition (como [**Windows.UI.Composition**](/uwp/api/windows.ui.composition) y [**DirectComposition)**](/windows/win32/directcomp/directcomposition-portal)hospedar contenido que se puede representar y presentar de forma independiente. En muchos sentidos, este tipo de contenido presentado es conceptualmente similar a una cadena de intercambio DXGI. Ambos ofrecen la capacidad de representar en un búfer y, a continuación, presentar ese búfer en la pantalla. Sin embargo, la API de intercambio de composición ofrece la posibilidad de que los presentes se desenván de un momento específico para aparecer (la hora *PresentAt),* mientras que DXGI no, y la API de intercambio de composición ofrece más libertad que DXGI en torno a la ordenación de búferes disponibles para presentarse.

El objetivo de la versión inicial de esta API es habilitar marcos multimedia, como [Windows Media Foundation](/windows/win32/medfound/microsoft-media-foundation-sdk), para usar eficazmente la presentación con tiempo.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Guía de programación de cadenas de intercambio de composición](comp-swapchain.md) | Esta API es un nuevo sucesor de la cadena de intercambio DXGI, que permite que las aplicaciones representen y presenten contenido en la pantalla. |
| [Ejemplos de código de cadena de intercambio de composición](comp-swapchain-examples.md) | Colección de ejemplos de código que muestran varios escenarios de cadena de intercambio de composición. |
| [Glosario de composición](comp-swapchain-glossary.md) | Glosario de términos de cadena de intercambio de composición. |
