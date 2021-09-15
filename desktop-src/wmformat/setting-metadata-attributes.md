---
title: Establecer atributos de metadatos
description: Establecer atributos de metadatos
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- Windows SDK de formato multimedia, establecimiento de atributos de metadatos
- Formato de sistemas avanzados (ASF), establecimiento de atributos de metadatos
- ASF (formato de sistemas avanzados), establecimiento de atributos de metadatos
- metadata,setting attributes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfde27d7bc965076d1a4b5f9674c6d198ce61da5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570201"
---
# <a name="setting-metadata-attributes"></a>Establecer atributos de metadatos

Los atributos de metadatos se establecen mediante [**el método IWMHeaderInfo3::AddAttribute.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute)

A todos los atributos se les asigna un idioma de la lista de idiomas del archivo. Puede acceder a la lista de idiomas mediante la [**interfaz IWMLanguageList.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) Para obtener un puntero a una **interfaz IWMLanguageList,** llame a **QueryInterface** en cualquier interfaz del objeto del que haya obtenido [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).

Puede agregar atributos con cualquier nombre que quiera. Sin embargo, el uso de nombres de atributo que no son nombres estándar admitidos por el SDK de formato multimedia de Windows puede dificultar la de descubrimiento de los metadatos para los usuarios. La mayoría de las aplicaciones de reproducción multimedia comprobarán si hay valores estándar. Para obtener más información, vea [Metadatos personalizados.](custom-metadata.md)

No puede usar el número de secuencia 0xFFFF agregar un atributo globalmente. Debe asignar cada atributo a un número de flujo específico o flujo 0 para los atributos de nivel de archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




