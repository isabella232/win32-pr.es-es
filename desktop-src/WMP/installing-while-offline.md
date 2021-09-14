---
title: Instalación mientras está sin conexión
description: Instalación mientras está sin conexión
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Reproductor de Windows Media en línea, instalar mientras está sin conexión
- tiendas en línea, instalación sin conexión
- tiendas en línea de tipo 1, instalación sin conexión
- tiendas en línea de tipo 2, instalar mientras está sin conexión
- Reproductor de Windows Media en línea, instalación sin conexión
- tiendas en línea, instalación sin conexión
- tiendas en línea de tipo 1, instalación sin conexión
- tiendas en línea de tipo 2, instalación sin conexión
- instalar tiendas en línea sin conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad7048926f218ea7be74a2522eb32c58241a017
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249566"
---
# <a name="installing-while-offline"></a>Instalación mientras está sin conexión

Los usuarios pueden Reproductor de Windows Media mientras no están conectados a Internet. Cuando esto sucede, Reproductor de Windows Media programa de instalación busca el ServiceInfo.xml especificado por el parámetro de línea de comandos *ServiceInfo.* Si el **atributo Key** coincide con el parámetro de línea de comandos *DefaultService,* el programa de instalación aplica la información de los elementos siguientes a Reproductor de Windows Media:

-   FriendlyName. El nombre descriptivo de la tienda en línea se muestra en la Reproductor de Windows Media de usuario.
-   Color. Los colores especificados se aplican a la barra de tareas y a los botones.
-   ServiceTask1, ServiceTask2 y ServiceTask3. Se establecen los elementos secundarios ButtonText y ButtonTip. No se establece el atributo de dirección URL. La dirección URL se establece una vez que el usuario se conecta a Internet Reproductor de Windows Media recupera su lista de tiendas en línea de la manera normal.
-   Imagen. Se establecen los atributos MenuURL y ServiceLargeURL. Estas direcciones URL deben apuntar a las imágenes que instaló en el disco duro del usuario mediante el protocolo file:// usuario.

Cuando el usuario intenta ver la tienda en línea, Reproductor de Windows Media muestra un mensaje que informa al usuario de que se requiere una conexión a Internet.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Elemento Color**](color-element.md)
</dt> <dt>

[**Elemento FriendlyName**](friendlyname-element.md)
</dt> <dt>

[**Elemento Image**](image-element.md)
</dt> <dt>

[**Información común a los almacenes en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
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

[**Configuración de parámetros de línea de comandos para almacenes en línea**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




