---
title: Instalación sin conexión
description: Instalación sin conexión
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Windows Media Player tiendas en línea, instalación sin conexión
- tiendas en línea, instalar sin conexión
- tipo 1 almacenes en línea, instalación sin conexión
- tipo 2 tiendas en línea, instalación sin conexión
- Windows Media Player tiendas en línea, instalaciones sin conexión
- tiendas en línea, instalaciones sin conexión
- tipo 1 tiendas en línea, instalaciones sin conexión
- tipo 2 tiendas en línea, instalaciones sin conexión
- instalación de tiendas en línea sin conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad7048926f218ea7be74a2522eb32c58241a017
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903584"
---
# <a name="installing-while-offline"></a>Instalación sin conexión

Los usuarios pueden instalar Windows Media Player mientras no están conectados a Internet. Cuando esto sucede, el programa de instalación de Windows Media Player localiza el ServiceInfo.xml documento especificado por el parámetro de línea de comandos *ServiceInfo* . Si el atributo **clave** coincide con el parámetro de línea de comandos *DefaultService* , el programa de instalación aplica la información de los siguientes elementos a Windows Media Player:

-   FriendlyName. El nombre descriptivo de la tienda en línea se muestra en la interfaz de usuario de Windows Media Player.
-   Color. Los colores especificados se aplican a la barra de tareas y los botones.
-   ServiceTask1, ServiceTask2 y ServiceTask3. Se establecen los elementos secundarios ButtonText y ButtonTip. No se ha establecido el atributo URL. La dirección URL se establece una vez que el usuario se conecta a Internet y Windows Media Player recupera su lista de tiendas en línea de manera normal.
-   Imagen. Se establecen los atributos MenuURL y ServiceLargeURL. Estas direcciones URL deben apuntar a las imágenes instaladas en el disco duro del usuario mediante el protocolo file://.

Cuando el usuario intenta ver la tienda en línea, Windows Media Player muestra un mensaje que informa al usuario de que se requiere una conexión a Internet.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Elemento color**](color-element.md)
</dt> <dt>

[**Elemento FriendlyName**](friendlyname-element.md)
</dt> <dt>

[**Elemento Image**](image-element.md)
</dt> <dt>

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**ServiceInfo, elemento**](serviceinfo-element.md)
</dt> <dt>

[**Elemento ServiceTask1**](servicetask1-element.md)
</dt> <dt>

[**Elemento ServiceTask2**](servicetask2-element.md)
</dt> <dt>

[**Elemento ServiceTask3**](servicetask3-element.md)
</dt> <dt>

[**Establecimiento de la tienda en línea inicial**](setting-the-initial-online-store.md)
</dt> <dt>

[**Parámetros de la línea de comandos del programa de instalación para tiendas en línea**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




