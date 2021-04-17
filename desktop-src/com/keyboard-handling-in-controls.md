---
title: Control de teclado en controles
description: Control de teclado en controles
ms.assetid: 33affb3f-5d52-4ada-9751-0775b31a375e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f32610732ddbf88c6a587d5bc0fd7de1188152d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704797"
---
# <a name="keyboard-handling-in-controls"></a>Control de teclado en controles

Se recomienda encarecidamente la compatibilidad con la administración de teclado para la siguiente funcionalidad, aunque se reconoce que no es aplicable a todos los contenedores.

-   Compatibilidad con los \_ bits de estado OLEMISC ACTSLIKELABEL y OLEMISC \_ ACTSLIKEBUTTON.
-   Implementar la propiedad de ambiente DisplayAsDefault (si existe, puede devolver **false**).
-   Implementar el control de pestañas, incluido el orden de tabulación.

Algunos contenedores usarán controles ActiveX en escenarios de documentos compuestos tradicionales. Por ejemplo, una hoja de cálculo puede permitir que un usuario inserte un control ActiveX en una hoja de cálculo. En estos escenarios, el contenedor haría la administración del teclado de manera diferente, porque la interfaz de teclado debe ser coherente con las expectativas del usuario de una hoja de cálculo. La documentación de estos productos debe informar a los usuarios de las diferencias en el control de los controles en estos diferentes escenarios. Otros contenedores deben intentar respetar correctamente la funcionalidad anterior, incluido el control de teclas de tecla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

 




