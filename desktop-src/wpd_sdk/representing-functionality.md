---
description: Representar la funcionalidad
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: Representar la funcionalidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101614592224a1a5ac079b1f9c3dc89cea9afefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911122"
---
# <a name="representing-functionality"></a>Representar la funcionalidad

Existen objetos funcionales para identificar o agrupar lógicamente las capacidades de características de un dispositivo. Por ejemplo, una aplicación puede ver que un dispositivo admite SMS buscando el objeto funcional de SMS. Del mismo modo, la aplicación puede ver que un dispositivo tiene capacidades de cámara buscando el objeto funcional de captura de imagen fija.

Esta representación de objeto flexible ayuda a facilitar la compatibilidad con dispositivos con funciones multifunción. Los controladores pueden exponer simplemente los objetos funcionales que representan su dispositivo, lo que es más granular que el uso de las clases de dispositivos tradicionales. La representación del objeto también ayuda a aislar las partes funcionales superpuestas. por ejemplo, algunos teléfonos pueden tener dos cámaras o cuatro almacenamientos.

En el sistema operativo Windows 7, los servicios amplían los objetos funcionales proporcionando consultas enriquecidas de capacidades y una agrupación abstracta de contenido. Las aplicaciones pueden usar los servicios para detectar funcionalidades del dispositivo e interactuar con el contenido de forma más eficaz. Por ejemplo, una aplicación puede ver que un dispositivo es compatible con las funcionalidades de sincronización de contactos buscando un objeto de servicio de contactos y puede buscar todos los contactos como objetos secundarios del objeto de servicio, sin tener que buscar de forma recursiva en la jerarquía de almacenamiento.

Los servicios también permiten a las aplicaciones detectar e invocar el comportamiento personalizado en un dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información general de la aplicación**](application-overview.md)
</dt> </dl>

 

 



