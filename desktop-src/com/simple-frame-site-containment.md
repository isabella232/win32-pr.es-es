---
title: Contención de sitio de marco simple
description: Contención de sitio de marco simple
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0106bc88d9f69f380590e808741e0b1a0bdc2f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994081"
---
# <a name="simple-frame-site-containment"></a>Contención de sitio de marco simple

Un control contenedor es un control ActiveX que es capaz de contener otros controles. Un cuadro de grupo que contiene una colección de botones de radio es un ejemplo de un control contenedor. Los controles de contenedor deben establecer el \_ bit de estado OLEMISC SIMPLEFRAME y deben llamar a la implementación [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) de su contenedor. Un contenedor de controles ActiveX que admite controles de contenedor debe implementar **ISimpleFrameSite**.

CATId-{157083E0-2368-11cf-87B9-00AA006C8166} CATId \_ SimpleFrameControl

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías del componente](component-categories.md)
</dt> </dl>

 

 




