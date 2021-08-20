---
description: El terminal CVideoCaptureTerminal se deriva de CSingleFilterTerminal e implementa un terminal de captura de vídeo estático mediante un único DirectShow filtro.
ms.assetid: e66b1c8d-37c0-40c7-8ad6-b1e84294b02b
title: CVideoCaptureTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23751e879c73c8846dabc054d27034647813231f32cbe1127b9ee21e90c017ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946168"
---
# <a name="cvideocaptureterminal"></a>CVideoCaptureTerminal

El terminal **CVideoCaptureTerminal** se deriva de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminal de captura de vídeo estático mediante un único DirectShow filtro. No admite ciertas interfaces avanzadas de captura de vídeo que solo son aplicables a la captura de vídeo WDM. La mayoría de los MSP no tendrán que invalidar la implementación de este terminal.

Se define en MSPtmvc.h.

 

 



