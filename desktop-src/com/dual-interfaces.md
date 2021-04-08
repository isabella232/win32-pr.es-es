---
title: Interfaces duales (COM)
description: Interfaces duales
ms.assetid: 6e4dc529-8a25-4ae5-b868-28cb17e0db52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da95c77a307c40721b909eceb1e6d29bab23bc14
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078480"
---
# <a name="dual-interfaces"></a>Interfaces duales

OLE Automation permite que un objeto exponga un conjunto de métodos de dos maneras: a través de la interfaz **IDispatch** y a través del enlace vtable OLE directo. La mayoría de las herramientas disponibles en la actualidad usan **IDispatch** y ofrece compatibilidad para el enlace en tiempo de ejecución a propiedades y métodos.

El enlace VTable ofrece un rendimiento mucho mayor porque se llama directamente a este método en lugar de a través de **IDispatch:: Invoke**. **IDispatch** ofrece compatibilidad con enlace en tiempo de ejecución, donde el enlace vtable directo ofrece un aumento significativo del rendimiento. ambas técnicas son valiosas e importantes en diferentes escenarios. Al etiquetar una interfaz como \[ [**dual**](/windows/desktop/Midl/dual) \] en la biblioteca de tipos, se puede utilizar una interfaz de automatización OLE mediante **IDispatch**, o bien se puede enlazar directamente. Por lo tanto, los contenedores pueden elegir la técnica más adecuada. Se recomienda encarecidamente la compatibilidad con interfaces duales para controles y contenedores.

 

 