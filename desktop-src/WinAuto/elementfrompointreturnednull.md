---
title: ElementFromPointReturnedNull
description: ElementFromPointReturnedNull
ms.assetid: DBCA6705-BDFD-4024-A505-4539F72A9421
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde128b0865d24ea41270665a7b9592355a68d5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704806"
---
# <a name="elementfrompointreturnednull"></a>ElementFromPointReturnedNull

## <a name="text"></a>Texto

IUIAutomation. ElementFromPoint ( {0} , {1} ) devolvió null

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

La dirección del objeto [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) del elemento de la interfaz de usuario obtenida para las coordenadas dadas es NULL.

## <a name="possible-causes"></a>Causas posibles

-   Interacción del usuario durante la comprobación, por ejemplo, al mover el foco a un HWND no objetivo, se interfiere con el proceso de comprobación.
-   Implementación de automatización de la interfaz de usuario incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




