---
title: Interfaces duales (COM)
description: Interfaces duales
ms.assetid: 6e4dc529-8a25-4ae5-b868-28cb17e0db52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6540b93f12cdef698f807bc6179e4e36c4ef1bf18c6b0c1abbed96480b3e3289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919291"
---
# <a name="dual-interfaces"></a>Interfaces duales

Ole Automation permite que un objeto exponga un conjunto de métodos de dos maneras: a través de la **interfaz IDispatch** y a través del enlace directo de OLE VTable. **IDispatch se** usa en la mayoría de las herramientas disponibles actualmente y ofrece compatibilidad para el enlace en tiempo de entrega a propiedades y métodos.

El enlace de VTable ofrece un rendimiento mucho mayor porque este método se llama directamente en lugar de a través **de IDispatch::Invoke**. **IDispatch ofrece compatibilidad** enlazada en tiempo de ejecución, donde el enlace directo de VTable ofrece una mejora significativa del rendimiento. ambas técnicas son valiosas e importantes en distintos escenarios. Al etiquetar una interfaz como dual en la biblioteca de tipos, se puede usar una interfaz de automatización OLE a través de \[ [](/windows/desktop/Midl/dual) \] **IDispatch** o se puede enlazar a directamente. Por lo tanto, los contenedores pueden elegir la técnica más adecuada. Se recomienda encarecidamente la compatibilidad con interfaces duales para controles y contenedores.

 

 