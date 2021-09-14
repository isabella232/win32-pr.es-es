---
title: Interfaces duales (COM)
description: Interfaces duales
ms.assetid: 6e4dc529-8a25-4ae5-b868-28cb17e0db52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da95c77a307c40721b909eceb1e6d29bab23bc14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242894"
---
# <a name="dual-interfaces"></a>Interfaces duales

Ole Automation permite que un objeto exponga un conjunto de métodos de dos maneras: a través de la **interfaz IDispatch** y mediante el enlace directo de OLE VTable. **IDispatch se usa** en la mayoría de las herramientas disponibles actualmente y ofrece compatibilidad para el enlace en tiempo de tarde a propiedades y métodos.

El enlace de VTable ofrece un rendimiento mucho mayor porque se llama a este método directamente en lugar de a través **de IDispatch::Invoke**. **IDispatch ofrece compatibilidad** enlazada en tiempo de ejecución, donde el enlace directo de VTable ofrece una mejora significativa del rendimiento. ambas técnicas son valiosas e importantes en distintos escenarios. Al etiquetar una interfaz como dual en la biblioteca de tipos, se puede usar una interfaz de automatización OLE a través de \[ [](/windows/desktop/Midl/dual) \] **IDispatch** o se puede enlazar a directamente. Por lo tanto, los contenedores pueden elegir la técnica más adecuada. Se recomienda encarecidamente la compatibilidad con interfaces duales para controles y contenedores.

 

 