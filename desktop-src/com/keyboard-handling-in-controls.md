---
title: Control de teclado en controles
description: Control de teclado en controles
ms.assetid: 33affb3f-5d52-4ada-9751-0775b31a375e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f32610732ddbf88c6a587d5bc0fd7de1188152d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359837"
---
# <a name="keyboard-handling-in-controls"></a>Control de teclado en controles

Se recomienda encarecidamente la compatibilidad con el control de teclado para la siguiente funcionalidad, aunque se reconoce que no es aplicable a todos los contenedores.

-   Compatibilidad con los bits de estado DE OLEMISC \_ ACTSLIKELABEL y OLEMISC \_ ACTSLIKEBUTTON.
-   Implementar la propiedad de ambiente DisplayAsDefault (si existe, puede devolver **FALSE).**
-   Implementar el control de pestañas, incluido el orden de tabulación.

Algunos contenedores usarán controles ActiveX en escenarios de documentos compuestos tradicionales. Por ejemplo, una hoja de cálculo puede permitir que un usuario inserte un control ActiveX en una hoja de cálculo. En tales escenarios, el contenedor realizaría el control de teclado de forma diferente, ya que la interfaz de teclado debe ser coherente con las expectativas del usuario de una hoja de cálculo. La documentación de estos productos debe informar a los usuarios de las diferencias en el control del control en estos distintos escenarios. Otros contenedores deben procurar respetar correctamente la funcionalidad anterior, incluido el control mnemotécnico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

 




