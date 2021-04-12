---
title: Establecer atributos de metadatos
description: Establecer atributos de metadatos
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- SDK de Windows Media Format, establecer atributos de metadatos
- Advanced Systems Format (ASF), establecer atributos de metadatos
- ASF (formato de sistemas avanzados), establecer atributos de metadatos
- metadatos, establecer atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfde27d7bc965076d1a4b5f9674c6d198ce61da5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420305"
---
# <a name="setting-metadata-attributes"></a>Establecer atributos de metadatos

Los atributos de metadatos se establecen mediante el método [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) .

Todos los atributos se asignan a un idioma de la lista de idiomas del archivo. Puede tener acceso a la lista de idiomas mediante la interfaz [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) . Para obtener un puntero a una interfaz **IWMLanguageList** , llame a **QueryInterface** en cualquier interfaz del objeto desde el que haya obtenido [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).

Puede agregar atributos con cualquier nombre que desee. Sin embargo, el uso de nombres de atributo que no son nombres estándar compatibles con el SDK de Windows Media Format puede dificultar la detección de los metadatos. La mayoría de las aplicaciones de reproducción multimedia comprobarán los valores estándar. Para obtener más información, vea [metadatos personalizados](custom-metadata.md).

No se puede usar el número de secuencia 0xFFFF para agregar un atributo globalmente. Debe asignar cada atributo a un número de secuencia específico o a la secuencia 0 para los atributos de nivel de archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




