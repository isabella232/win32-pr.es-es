---
title: Enumeración de formato de salida
description: Enumeración de formato de salida
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- Windows SDK de formato multimedia, enumeraciones de formato de salida
- Formato de sistemas avanzados (ASF), enumeraciones de formato de salida
- ASF (formato de sistemas avanzados), enumeraciones de formato de salida
- Windows SDK de formato multimedia, interfaz IWMReaderTypeNegotiation
- Advanced Systems Format (ASF),IWMReaderTypeNegotiation (interfaz)
- ASF (formato de sistemas avanzados), interfaz IWMReaderTypeNegotiation
- enumeraciones de formato de salida
- IWMReaderTypeNegotiation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49999c3da2afd05b0d2231d259d24a50356eb4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266967"
---
# <a name="output-format-enumeration"></a>Enumeración de formato de salida

Tanto el objeto de lector como el objeto de lector sincrónico se comunican con los códecs para enumerar los posibles formatos de salida para secuencias comprimidas. Al leer un archivo que contiene contenido comprimido con uno o varios de los códecs multimedia de Windows, puede examinar los posibles formatos de salida para elegir el que mejor se adapte a sus necesidades. Para mayor comodidad, cada códec tiene un formato de salida predeterminado que se establece en el formato más usado. Para obtener más información sobre la enumeración de salida, vea [Trabajar con salidas](working-with-outputs.md).

Puede realizar determinados cambios en un formato de salida en función del tipo de medio. En el caso de las secuencias de vídeo, por ejemplo, puede cambiar el tamaño del marco y la profundidad del color. Los objetos de lectura admiten una interfaz para probar los cambios realizados en el formato de salida, [**denominado IWMReaderTypeNegotiation.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de lectura de archivos**](file-reading-features.md)
</dt> </dl>

 

 




