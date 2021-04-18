---
title: Elección de un método de codificación
description: Elección de un método de codificación
ms.assetid: 095245a6-39eb-4228-86ac-ade94dde3695
keywords:
- perfiles, elegir métodos de codificación
- perfiles, métodos de codificación
- códecs, elegir métodos de codificación
- códecs, métodos de codificación
- perfiles, seleccionar métodos de codificación
- códecs, seleccionar métodos de codificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54c5bd099e5aaf8b3a735594c8b87a335fc2594
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695300"
---
# <a name="choosing-an-encoding-method"></a>Elección de un método de codificación

Algunos códecs, como el códec de Windows Media Video 9, admiten varios métodos de codificación. El método de codificación que elija para un flujo dependerá de cómo se entregue la secuencia. En la tabla siguiente se describe cuándo usar los distintos métodos de codificación.



| Método de codificación                | Descripción                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1: pasar la velocidad de bits constante (CBR) | La única opción para el streaming en vivo. Codifica en una velocidad de bits predecible y proporciona la calidad más baja de todos los métodos de codificación.                                                                    |
| 2-Pass CBR                     | Use para los archivos que se transmitirán por secuencias a través de una red a un lector de cliente, pero que no se difunden desde un origen en directo. Codifica en una velocidad de bits predecible, pero con mejor calidad que 1-Pass CBR. |
| 1: pasar la velocidad de bits variable (VBR) | Use cuando necesite especificar la calidad de la salida codificada. Ofrece la calidad más coherente de todos los métodos de codificación. Use solo para archivos locales o para su descarga.                        |
| VBR de dos pasos: sin restricciones     | Use cuando necesite especificar un ancho de banda, pero se aceptan las fluctuaciones en torno al ancho de banda especificado. Solo para archivos locales o para descarga.                                                    |
| VBR de 2 pasos: restringido       | Use en las mismas circunstancias que sin restricciones, pero cuando tenga que especificar una velocidad de bits máxima. Solo para archivos locales o para descarga.                                                |



 

En la tabla siguiente se enumeran los métodos de codificación que son compatibles con los códecs que se incluyen con el SDK de Windows Media Format.



| Códec                                  | CBR | 2-Pass CBR | VBR | VBR de 2 pasos |
|----------------------------------------|-----|------------|-----|------------|
| Windows Media Video 9                  | X   | X          | X   | X          |
| Windows Media Audio 9 y versiones posteriores        | X   | X          | X   | X          |
| Pantalla de Windows Media Video 9           | X   |            | X   |            |
| Windows Media Audio 9 Voice            | X   |            |     |            |
| Windows Media Audio Professional       | X   | X          | X   | X          |
| Windows Media Audio sin pérdida de           |     |            | X   |            |
| Imagen de Windows Media Video 9 y versiones posteriores  | X   |            | X   |            |
| Perfil avanzado de Windows Media Video 9 | X   | X          | X   | X          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Diseñar perfiles**](designing-profiles.md)
</dt> <dt>

[**Codificación de velocidad de bits constante (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Codificación de dos pasos**](two-pass-encoding.md)
</dt> <dt>

[**Codificación de velocidad de bits variable (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




