---
title: Claves de prueba y producción para una tienda en línea de tipo 1
description: Claves de prueba y producción para una tienda en línea de tipo 1
ms.assetid: 1a975c0b-16b8-4da7-8594-316ae34257d0
keywords:
- Reproductor de Windows Media en línea, claves de prueba
- tiendas en línea, claves de prueba
- tipo 1 tiendas en línea, claves de prueba
- Reproductor de Windows Media en línea, claves de producción
- tiendas en línea, claves de producción
- tipo 1 tiendas en línea, claves de producción
- Reproductor de Windows Media en línea,documento ServiceInfo
- online stores,ServiceInfo document
- tipo 1 tiendas en línea, documento ServiceInfo
- claves de prueba
- claves de producción
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e8ce8d049df78f186d336079f76eb00eb8bb10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580697"
---
# <a name="test-and-production-keys-for-a-type-1-online-store"></a>Claves de prueba y producción para una tienda en línea de tipo 1

Cuando empiece a desarrollar su tienda en línea, Microsoft le proporciona dos claves numéricas: una clave de prueba y una clave de producción. Al mismo tiempo, debe proporcionar a Microsoft dos direcciones URL: una que apunta al documento ServiceInfo de prueba y otra que apunta al documento ServiceInfo de producción.

Durante la fase de desarrollo y pruebas, la tienda en línea solo es visible en Reproductor de Windows Media si la clave de prueba o la clave de producción están en el registro del equipo del usuario. Si la clave de prueba está en el registro, Reproductor de Windows Media recupera el documento ServiceInfo de prueba, que apunta al complemento, las páginas web y las imágenes que pertenecen al almacén de pruebas. Si la clave de producción está en el registro, Reproductor de Windows Media recupera el documento ServiceInfo de producción, que apunta al complemento, las páginas web y las imágenes que pertenecen al almacén de producción.

Puede usar los almacenes de prueba y producción de cualquier manera que le sea útil. Sin embargo, normalmente la distinción es la siguiente:

-   El almacén de pruebas es el lugar donde realiza cambios diarios en el complemento, las páginas web, las imágenes y otros componentes del servicio.
-   El almacén de producción es el lugar donde mantiene una versión estable del servicio, que incluye el complemento, las páginas web, las imágenes y otros componentes.

Para que la tienda en línea se pueda publicar en Reproductor de Windows Media, Microsoft debe validar que el servicio funciona correctamente. Durante la fase de validación, Microsoft usa la clave de producción. Microsoft no usa la clave de prueba durante la fase de validación.

Cuando la tienda en línea de producción completa correctamente el proceso de validación, Microsoft publica la tienda, lo que significa que el almacén de producción aparece en Reproductor de Windows Media para todos los usuarios, no solo los que tienen la clave de producción en el Registro. Una vez publicada la tienda, las claves de prueba y producción ya no son necesarias.

> [!Note]  
> Es posible que los usuarios puedan adivinar la clave de prueba o producción de la tienda en línea y ver la tienda mientras se está desarrollando. Debe tener cuidado al exponer las características que desea mantener en secreto hasta la versión pública.

 

Para obtener información detallada sobre dónde colocar las claves de producción y de prueba en el registro del usuario, vea Claves y entradas del Registro para un almacén en línea de tipo [1.](registry-keys-and-entries-for-a-type-1-online-store.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




