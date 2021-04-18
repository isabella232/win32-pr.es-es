---
title: Complementos de origen
description: Complementos de origen
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- SDK de Windows Media Format, Complementos de origen
- Advanced Systems Format (ASF), Complementos de origen
- ASF (formato de sistemas avanzados), Complementos de origen
- Complementos de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4822b9110def4e1b758be40310f503fd56a251fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105720127"
---
# <a name="source-plug-ins"></a>Complementos de origen

Un complemento de origen es una opción disponible para los desarrolladores que desean implementar su propio sistema de almacenamiento para archivos de® de Windows Media. Un complemento de origen permite esto a través de la implementación de una interfaz COM denominada **IStream**, que es una interfaz estándar para proporcionar datos.

El complemento de origen debe escribirse como un archivo dll y su presencia se hace conocida en el SDK a través de una entrada del registro. Puede haber cualquier número de complementos de origen implementados de esta manera. El complemento de origen debe exportar la función [**WMCreateStreamForURL**](wmcreatestreamforurl.md) .

Para registrar un complemento de origen, se debe agregar la siguiente entrada del registro:

HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Media \\ WMSDK \\ sources

Name = "cualquier nombre único"

Valor = nombreruta del archivo dll de complemento de origen

Una vez registrado el archivo dll, la aplicación puede usar el método **IWMReader:: Open** (con la dirección URL adecuada como parámetro) para tener acceso a los datos de la secuencia, que se pueden almacenar en archivos o en contenedores de datos definidos por el usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> <dt>

[**WMCreateStreamForURL**](wmcreatestreamforurl.md)
</dt> </dl>

 

 




