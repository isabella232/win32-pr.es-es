---
title: Web Secuencias
description: Web Secuencias
ms.assetid: 78a2c703-a3f8-4afc-85d3-1c0a8f5a52b5
keywords:
- Windows SDK de formato multimedia, secuencias web
- Formato de sistemas avanzados (ASF), flujos web
- ASF (formato de sistemas avanzados), flujos web
- Windows SDK de formato multimedia, secuencias
- Formato de sistemas avanzados (ASF), secuencias
- ASF (formato de sistemas avanzados), secuencias
- Flujos web, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c85009eb2071584c01d7ffce0492cee4eb4652db8ad7710d0d909dd3ed21ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930465"
---
# <a name="web-streams"></a>Web Secuencias

Una secuencia web es como una secuencia de archivos en la que contiene archivos de datos. En una secuencia web, estos archivos suelen ser páginas HTML y gráficos asociados en formato GIF o JPEG.

Las secuencias web pueden ser especialmente útiles para los archivos ASF que se usan como presentaciones. Antes de admitir secuencias web, las presentaciones tendrían direcciones URL en secuencias de scripts dentro de un archivo para que una página web se cargara en un momento predeterminado. La dificultad era que la congestión de la red pudiera provocar retrasos y crear una experiencia de visualización deficiente.

Con las secuencias web, las partes constituyentes de las páginas web se pueden incluir en el archivo ASF como una secuencia. A medida que se reciben los archivos, se pueden almacenar en caché para que, cuando se entregue el comando para mostrar (o representar) una dirección URL, un explorador pueda acceder a ellos al instante. Esto permite una reproducción fluida y coherente. El comando render se entrega en la propia secuencia web, no como un comando de script en una secuencia independiente.

Se recomienda que las secuencias web creadas mediante el SDK de la serie Windows Media Format 9 o posterior tenga el número de versión 1. Este valor se especifica en la estructura [**WMT \_ WEBSTREAM \_ FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) del **miembro wVersion.** El propio SDK no hace nada para aplicar esta versión.

> [!Note]  
> Al conectarse a secuencias de difusión en vivo que tienen secuencias web, es posible que el usuario pueda recibir un comando de representación antes de que el archivo especificado esté realmente en la memoria caché local. A menos que la aplicación controle esta condición, el explorador mostrará un error "Página no encontrada".

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Errores arbitrarios Secuencias**](arbitrary-streams.md)
</dt> <dt>

[**Configuración de web Secuencias**](configuring-web-streams.md)
</dt> </dl>

 

 




