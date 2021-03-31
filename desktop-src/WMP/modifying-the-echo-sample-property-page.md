---
title: Modificar la página de propiedades de ejemplo echo
description: Modificar la página de propiedades de ejemplo echo
ms.assetid: a7ebf7d7-1f70-421f-862f-bc60655bb242
keywords:
- Complementos de Windows Media Player, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo echo
- Complementos de procesamiento de señal digital, páginas de propiedades de ejemplo de eco
- Complementos DSP, páginas de propiedades de ejemplo echo
- Ejemplo de complemento de DSP de eco, páginas de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f16c623f833d8d9c107c00e96fed92bab28e8b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418578"
---
# <a name="modifying-the-echo-sample-property-page"></a>Modificar la página de propiedades de ejemplo echo

La implementación de la página de propiedades predeterminada que proporciona el ejemplo de complemento DSP del Asistente para complementos de Windows Media Player contiene un único control de cuadro de edición que recibe el factor de escala del usuario. Debe modificar la página de propiedades para recibir los dos valores de propiedad que usa el ejemplo echo.

Para obtener información general sobre las páginas de propiedades del complemento DSP, vea [implementar un complemento de DSP de audio](implementing-an-audio-dsp-plug-in.md).

Las secciones siguientes le guían por el proceso de modificación de la página de propiedades de ejemplo:

-   [Modificar el recurso de cuadro de diálogo echo](modifying-the-echo-dialog-resource.md)
-   [Agregar y modificar eventos](adding-and-modifying-the-events.md)
-   [Cómo el ejemplo echo conserva los datos](how-the-echo-sample-persists-data.md)
-   [Implementar CEchoPropPage:: OnInitDialog](implementing-cechoproppage--oninitdialog.md)
-   [Implementación de CEchoPropPage:: Apply](implementing-cechoproppage--apply.md)
-   [Implementación de CEcho:: FinalConstruct](implementing-cecho--finalconstruct.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**El ejemplo echo**](the-echo-sample.md)
</dt> </dl>

 

 




