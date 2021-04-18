---
title: Consideraciones para los mercados internacionales
description: Consideraciones para los mercados internacionales
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Windows Media Player tiendas en línea, mercados internacionales
- tiendas en línea, mercados internacionales
- tipo 1 tiendas en línea, mercados internacionales
- tipo 2 tiendas en línea, mercados internacionales
- mercados internacionales
- Windows Media Player tiendas en línea, documento de ServiceInfo
- tiendas en línea, documento de ServiceInfo
- tipo 1 tiendas en línea, documento de ServiceInfo
- tipo 2 tiendas en línea, documento de ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1822e4f647c9967d50d40fa19331cd58565cf2eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695368"
---
# <a name="considerations-for-international-markets"></a>Consideraciones para los mercados internacionales

Si su empresa crea tiendas en línea para varios mercados, debe proporcionar a Microsoft la dirección URL de un documento de ServiceInfo para cada mercado. Puede hacer esto de dos maneras:

-   Cree un documento ServiceInfo independiente para cada mercado. En este caso, proporciona a Microsoft las direcciones URL que apuntan a documentos de ServiceInfo individuales para cada tienda en línea en cada mercado.
-   Cree un único documento ServiceInfo para todos los mercados. Al hacerlo, proporciona a Microsoft la misma dirección URL para cada mercado. El documento ServiceInfo, creado como una página ASP, puede detectar dinámicamente la ubicación del usuario en función de los parámetros de la cadena de consulta.

Windows Media Player anexa una cadena de consulta a la solicitud URL de ServiceInfo que proporciona información sobre la configuración regional y de ubicación del usuario. Si la tienda en línea usa esta información para determinar el contenido que se va a mostrar, debe anexar dinámicamente estos valores a sus propias direcciones URL en el documento de ServiceInfo. Esta es la mejor manera de asegurarse de que las direcciones URL de la página web siempre contendrán los parámetros esperados.

Una vez que haya determinado la ubicación del usuario y la preferencia de idioma, es posible que desee conservar esta información para futuras sesiones. Para ello, puede usar cualquiera de las técnicas que usaría normalmente en una página web, como cookies, o mediante el objeto COM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación dinámica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**ServiceInfo, elemento**](serviceinfo-element.md)
</dt> </dl>

 

 




