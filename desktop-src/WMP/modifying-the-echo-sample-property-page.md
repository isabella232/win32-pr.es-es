---
title: Modificar la página de propiedades Echo Sample
description: Modificar la página de propiedades Echo Sample
ms.assetid: a7ebf7d7-1f70-421f-862f-bc60655bb242
keywords:
- Reproductor de Windows Media complementos, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo de eco
- complementos de procesamiento de señales digitales, páginas de propiedades de ejemplo de eco
- Complementos de DSP, páginas de propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, páginas de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f16c623f833d8d9c107c00e96fed92bab28e8b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967467"
---
# <a name="modifying-the-echo-sample-property-page"></a>Modificar la página de propiedades Echo Sample

La implementación predeterminada de la página de propiedades proporcionada por el ejemplo de complemento DSP del Asistente para complementos de Reproductor de Windows Media contiene un único control de cuadro de edición que recibe el factor de escala del usuario. Debe modificar la página de propiedades para recibir los dos valores de propiedad utilizados por el ejemplo echo.

Para obtener información general sobre las páginas de propiedades del complemento DE DSP, vea [Implementing an Audio DSP Plug-in](implementing-an-audio-dsp-plug-in.md).

Las secciones siguientes le guían por el proceso de modificación de la página de propiedades de ejemplo:

-   [Modificar el recurso del cuadro de diálogo Eco](modifying-the-echo-dialog-resource.md)
-   [Agregar y modificar los eventos](adding-and-modifying-the-events.md)
-   [Cómo conserva los datos el ejemplo de eco](how-the-echo-sample-persists-data.md)
-   [Implementación de CEchoPropPage::OnInitDialog](implementing-cechoproppage--oninitdialog.md)
-   [Implementación de CEchoPropPage::Apply](implementing-cechoproppage--apply.md)
-   [Implementación de CEcho::FinalConstruct](implementing-cecho--finalconstruct.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**El ejemplo de eco**](the-echo-sample.md)
</dt> </dl>

 

 




