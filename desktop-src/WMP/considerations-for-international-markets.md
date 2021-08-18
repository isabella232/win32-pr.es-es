---
title: Consideraciones para mercados internacionales
description: Consideraciones para mercados internacionales
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Reproductor de Windows Media en línea, mercados internacionales
- tiendas en línea, mercados internacionales
- tiendas en línea de tipo 1, mercados internacionales
- tiendas en línea de tipo 2, mercados internacionales
- mercados internacionales
- Reproductor de Windows Media en línea,documento ServiceInfo
- online stores,ServiceInfo document
- tipo 1 tiendas en línea, documento ServiceInfo
- tipo 2 tiendas en línea, documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82e2db056f748e1257649716c57a2f1774ee0b1b149966dce3851a75d08c8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580515"
---
# <a name="considerations-for-international-markets"></a>Consideraciones para mercados internacionales

Si su empresa crea tiendas en línea para varios mercados, debe proporcionar a Microsoft la dirección URL de un documento ServiceInfo para cada mercado. Puede hacerlo de una de las dos maneras siguientes:

-   Cree un documento ServiceInfo independiente para cada mercado. En este caso, proporciona a Microsoft direcciones URL que apuntan a documentos ServiceInfo individuales para cada tienda en línea de cada mercado.
-   Cree un único documento ServiceInfo para todos los mercados. Al hacerlo, proporciona a Microsoft la misma dirección URL para cada mercado. El documento ServiceInfo, creado como una página ASP, puede detectar dinámicamente la ubicación del usuario en función de los parámetros de cadena de consulta.

Reproductor de Windows Media una cadena de consulta a la solicitud de dirección URL de ServiceInfo que proporciona información sobre la configuración regional y la ubicación del usuario. Si la tienda en línea usa esta información para determinar qué contenido se va a mostrar, debe anexar dinámicamente estos valores a sus propias direcciones URL en el documento ServiceInfo. Esta es la mejor manera de asegurarse de que las direcciones URL de la página web siempre contendrán los parámetros esperados.

Una vez que haya determinado la ubicación del usuario y las preferencias de idioma, es posible que desee conservar esta información para sesiones futuras. Puede hacerlo mediante cualquiera de las técnicas que usaría normalmente en una página web, como cookies, o mediante el uso de su objeto COM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación dinámica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Información común a las tiendas en línea de tipo 1 y tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento ServiceInfo**](serviceinfo-element.md)
</dt> </dl>

 

 




