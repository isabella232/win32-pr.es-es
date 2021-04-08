---
title: Claves de prueba y de producción para una tienda en línea de tipo 2
description: Claves de prueba y de producción para una tienda en línea de tipo 2
ms.assetid: 4fce47e2-d73d-4484-9bda-48257268ed96
keywords:
- Windows Media Player tiendas en línea, claves de prueba
- tiendas en línea, claves de prueba
- tipo 2 tiendas en línea, claves de prueba
- Windows Media Player tiendas en línea, claves de producción
- tiendas en línea, claves de producción
- tipo 2 tiendas en línea, claves de producción
- Windows Media Player tiendas en línea, documento de ServiceInfo
- tiendas en línea, documento de ServiceInfo
- tipo 2 tiendas en línea, documento de ServiceInfo
- claves de prueba
- claves de producción
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f009e1b0ca58a66820e193e3b66f8ca50ccadc43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994501"
---
# <a name="test-and-production-keys-for-a-type-2-online-store"></a>Claves de prueba y de producción para una tienda en línea de tipo 2

Al comenzar el desarrollo de la tienda en línea, Microsoft proporciona dos claves numéricas: una clave de prueba y una clave de producción. Al mismo tiempo, debe proporcionar a Microsoft dos direcciones URL: una que apunte al documento ServiceInfo de prueba y otra que apunte al documento ServiceInfo de producción.

Durante la fase de desarrollo y pruebas, la tienda en línea solo es visible en Windows Media Player si la clave de prueba o la clave de producción se encuentra en el registro del equipo del usuario. Si la clave de prueba está en el registro, Windows Media Player recupera el documento de la prueba ServiceInfo, que señala al complemento, las páginas web y las imágenes que pertenecen a su almacén de pruebas. Si la clave de producción está en el registro, Windows Media Player recupera el documento ServiceInfo de producción, que señala el complemento, las páginas web y las imágenes que pertenecen a la tienda de producción.

Puede usar sus almacenes de prueba y producción de la forma que le resulte útil. Sin embargo, normalmente, la distinción es la siguiente:

-   El almacén de pruebas es el lugar donde se realizan los cambios diarios en el complemento, las páginas web, las imágenes y otros componentes del servicio.
-   La tienda de producción es el lugar donde se mantiene una versión estable del servicio, que incluye el complemento, las páginas web, las imágenes y otros componentes.

Antes de que la tienda en línea pueda publicarse en Windows Media Player, Microsoft debe validar que el servicio funciona correctamente. Durante la fase de validación, Microsoft utiliza su clave de producción. Microsoft no usa la clave de prueba durante la fase de validación.

Cuando la tienda en línea de producción completa correctamente el proceso de validación, Microsoft publica la tienda, lo que significa que la tienda de producción aparece en Windows Media Player para todos los usuarios, no solo en las que tienen la clave de producción en el registro. Una vez publicada la tienda, ya no se necesitan las claves de prueba y de producción.

> [!Note]  
> Es posible que los usuarios puedan adivinar la clave de prueba o de producción de la tienda en línea y ver la tienda mientras se desarrolla. Debe tener cuidado al exponer las características que desea mantener como secreto hasta la versión pública.

 

Para obtener información detallada sobre dónde colocar las claves de producción y prueba en el registro del usuario, consulte [claves del registro y entradas para una tienda en línea de tipo 2](registry-keys-and-entries-for-a-type-2-online-store.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Ejemplos de la tienda en línea de tipo 2**](type-2-online-store-samples.md)
</dt> </dl>

 

 




