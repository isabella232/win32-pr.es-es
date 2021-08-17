---
title: Instalación mientras está sin conexión
description: Instalación mientras está sin conexión
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Reproductor de Windows Media en línea, instalar mientras está sin conexión
- tiendas en línea, instalar mientras está sin conexión
- tipo 1 tiendas en línea, instalar mientras está sin conexión
- tipo 2 tiendas en línea, instalar mientras está sin conexión
- Reproductor de Windows Media en línea, instalación sin conexión
- tiendas en línea, instalación sin conexión
- tipo 1 tiendas en línea, instalación sin conexión
- tiendas en línea de tipo 2, instalación sin conexión
- instalar tiendas en línea mientras está sin conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3051aca9634bc2c53950baa783bcf62fc6861c616facd9dc563d70d011c2459
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135508"
---
# <a name="installing-while-offline"></a>Instalación mientras está sin conexión

Los usuarios pueden instalar Reproductor de Windows Media mientras no están conectados a Internet. Cuando esto sucede, Reproductor de Windows Media programa de instalación busca el ServiceInfo.xml especificado por el parámetro de línea de comandos *ServiceInfo.* Si el **atributo Key** coincide con el parámetro de línea de comandos *DefaultService,* el programa de instalación aplica información de los siguientes elementos a Reproductor de Windows Media:

-   FriendlyName. El nombre descriptivo de la tienda en línea se muestra en la Reproductor de Windows Media usuario.
-   Color. Los colores especificados se aplican a la barra de tareas y a los botones.
-   ServiceTask1, ServiceTask2 y ServiceTask3. Se establecen los elementos secundarios ButtonText y ButtonTip. No se establece el atributo de dirección URL. La dirección URL se establece una vez que el usuario se conecta a Internet y Reproductor de Windows Media recupera su lista de tiendas en línea de la manera normal.
-   Imagen. Se establecen los atributos MenuURL y ServiceLargeURL. Estas direcciones URL deben apuntar a imágenes instaladas en el disco duro del usuario mediante el protocolo file:// usuario.

Cuando el usuario intenta ver la tienda en línea, Reproductor de Windows Media muestra un mensaje que informa al usuario de que se requiere una conexión a Internet.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Elemento Color**](color-element.md)
</dt> <dt>

[**Elemento FriendlyName**](friendlyname-element.md)
</dt> <dt>

[**Elemento Image**](image-element.md)
</dt> <dt>

[**Información común a las tiendas en línea de tipo 1 y tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento ServiceInfo**](serviceinfo-element.md)
</dt> <dt>

[**Elemento ServiceTask1**](servicetask1-element.md)
</dt> <dt>

[**Elemento ServiceTask2**](servicetask2-element.md)
</dt> <dt>

[**Elemento ServiceTask3**](servicetask3-element.md)
</dt> <dt>

[**Establecimiento de la tienda en línea inicial**](setting-the-initial-online-store.md)
</dt> <dt>

[**Configuración de parámetros de la línea de comandos para almacenes en línea**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




