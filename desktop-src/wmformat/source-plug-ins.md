---
title: Complementos de origen
description: Complementos de origen
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- Windows SDK de formato multimedia, complementos de origen
- Formato de sistemas avanzados (ASF), complementos de origen
- ASF (formato de sistemas avanzados), complementos de origen
- complementos de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f16d0edc82423a43e50591fa07e14623adc23b94234a28985afca8a496822a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845809"
---
# <a name="source-plug-ins"></a>Complementos de origen

Un complemento de origen es una opción disponible para los desarrolladores que desean implementar su propio sistema de almacenamiento para Windows archivos ® multimedia. Un complemento de origen lo habilita mediante la implementación de una interfaz COM denominada **IStream**, que es una interfaz estándar para proporcionar datos.

El complemento de origen debe escribirse como un archivo DLL y su presencia se conoce para el SDK a través de una entrada del Registro. Puede haber cualquier número de complementos de origen implementados de esta manera. El complemento de origen debe exportar la [**función WMCreateStreamForURL.**](wmcreatestreamforurl.md)

Para registrar un complemento de origen, se debe agregar la siguiente entrada del Registro:

HKEY \_ LOCAL MACHINE Software Microsoft Windows media \_ \\ \\ \\ \\ WMSDK \\ sources

Name = "any unique name"

Valor = pathname del archivo DLL del complemento de origen

Una vez registrado el archivo DLL, la aplicación puede usar el método **IWMReader::Open** (con la dirección URL adecuada como parámetro) para acceder a los datos de flujo, que se pueden almacenar en archivos o contenedores de datos definidos por el usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> <dt>

[**WMCreateStreamForURL**](wmcreatestreamforurl.md)
</dt> </dl>

 

 




