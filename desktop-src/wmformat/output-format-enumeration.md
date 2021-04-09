---
title: Enumeración del formato de salida
description: Enumeración del formato de salida
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- SDK de Windows Media Format, enumeraciones de formato de salida
- Formato de sistemas avanzados (ASF), enumeraciones de formato de salida
- ASF (formato de sistemas avanzados), enumeraciones de formato de salida
- SDK de Windows Media Format, interfaz IWMReaderTypeNegotiation
- Advanced Systems Format (ASF), IWMReaderTypeNegotiation (interfaz)
- ASF (formato de sistemas avanzados), interfaz IWMReaderTypeNegotiation
- enumeraciones de formato de salida
- IWMReaderTypeNegotiation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49999c3da2afd05b0d2231d259d24a50356eb4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077270"
---
# <a name="output-format-enumeration"></a>Enumeración del formato de salida

Tanto el objeto lector como el objeto lector sincrónico se comunican con los códecs para enumerar los posibles formatos de salida de las secuencias comprimidas. Cuando lee un archivo que contiene contenido comprimido con uno o varios de los códecs de Windows Media, puede examinar los posibles formatos de salida para elegir el que mejor se adapte a sus necesidades. Para mayor comodidad, cada códec tiene un formato de salida predeterminado que se establece en el formato que se usa con más frecuencia. Para obtener más información sobre la enumeración de salida, vea [trabajar con salidas](working-with-outputs.md).

Puede realizar determinados cambios en un formato de salida en función del tipo de medio. En el caso de las secuencias de vídeo, por ejemplo, puede cambiar el tamaño del marco y la profundidad de color. Los objetos de lectura admiten una interfaz para probar los cambios que realice en el formato de salida, denominado [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de lectura de archivos**](file-reading-features.md)
</dt> </dl>

 

 




