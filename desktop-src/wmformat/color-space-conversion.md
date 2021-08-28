---
title: Conversión de espacio de color
description: Conversión de espacio de color
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- Windows SDK de formato multimedia, conversión de espacio de color
- Formato de sistemas avanzados (ASF), conversión de espacio de color
- ASF (formato de sistemas avanzados), conversión de espacio de color
- conversión de espacio de color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23b596b7ae8ed32e64cc3ebe8a23f1bc52dafb5304308104aba083675afe6370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447945"
---
# <a name="color-space-conversion"></a>Conversión de espacio de color

A menudo hay una diferencia entre la profundidad de color del formato de vídeo comprimido en el perfil y el formato de entrada. Cuando esto sucede, el vídeo de origen se debe convertir para ajustarse al espacio de color del destino. El escritor controla este proceso, comunicándose con un convertidor de espacio de color interno.

El lector también se comunica con el convertidor de espacio de color para conciliar cualquier diferencia entre el formato comprimido y el formato de salida.

Al igual que con todas las transformaciones realizadas en los datos, la conversión entre profundidades de color puede reducir la calidad de la salida. Cuando sea posible, debe usar formatos de entrada y salida con la misma profundidad de color que el formato comprimido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de escritura de archivos**](file-writing-features.md)
</dt> <dt>

[**Trabajar con entradas**](working-with-inputs.md)
</dt> <dt>

[**Trabajar con salidas**](working-with-outputs.md)
</dt> </dl>

 

 




