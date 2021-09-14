---
title: Contención de sitio de marco simple
description: Contención de sitio de marco simple
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0106bc88d9f69f380590e808741e0b1a0bdc2f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160540"
---
# <a name="simple-frame-site-containment"></a>Contención de sitio de marco simple

Un control de contenedor es ActiveX control que es capaz de contener otros controles. Un cuadro de grupo que contiene una colección de botones de radio es un ejemplo de un control de contenedor. Los controles de contenedor deben establecer el bit de estado SIMPLEFRAME de OLEMISC y deben llamar a la implementación \_ [**ISimpleFrameSite de su**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) contenedor. Un ActiveX de control que admite controles de contenedor debe implementar **ISimpleFrameSite**.

CATID - {157083E0-2368-11cf-87B9-00AA006C8166} CATID \_ SimpleFrameControl

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías del componente](component-categories.md)
</dt> </dl>

 

 




