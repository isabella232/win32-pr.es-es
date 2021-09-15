---
description: Representación de la funcionalidad
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: Representación de la funcionalidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101614592224a1a5ac079b1f9c3dc89cea9afefe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572089"
---
# <a name="representing-functionality"></a>Representación de la funcionalidad

Existen objetos funcionales para identificar o agrupar lógicamente las funcionalidades de características de un dispositivo. Por ejemplo, una aplicación puede ver que un dispositivo admite SMS buscando el objeto funcional SMS. De forma similar, la aplicación puede ver que un dispositivo tiene funcionalidades de cámara buscando el objeto funcional Still Image Capture.

Esta representación flexible de objetos ayuda a facilitar la compatibilidad con dispositivos con funcionalidades de varias funciones. Los controladores simplemente pueden exponer cualquier objeto funcional que represente su dispositivo, que es más granular que el uso de clases de dispositivo tradicionales. La representación del objeto también ayuda a aislar las partes funcionales superpuestas; Por ejemplo, algunos teléfonos pueden tener dos cámaras o cuatro almacenamientos.

En el Windows operativo 7, los servicios amplían los objetos funcionales al proporcionar consultas completas de funcionalidades y una agrupación abstracta de contenido. Las aplicaciones pueden usar servicios para detectar las funcionalidades del dispositivo e interactuar con el contenido de forma más eficaz. Por ejemplo, una aplicación puede ver que un dispositivo admite las funcionalidades de sincronización de contactos buscando un objeto de servicio Contactos y puede encontrar todos los contactos como objetos secundarios del objeto de servicio, sin tener que buscar de forma recursiva en la jerarquía de almacenamiento.

Los servicios también permiten a las aplicaciones detectar e invocar comportamientos personalizados en un dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción a la aplicación**](application-overview.md)
</dt> </dl>

 

 



