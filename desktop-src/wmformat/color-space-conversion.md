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
ms.openlocfilehash: 2cbc284995cbc72aee148e12977dad9f4476b29c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359936"
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

 

 




