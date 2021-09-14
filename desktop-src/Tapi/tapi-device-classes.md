---
description: Obtenga información sobre las clases de dispositivo TAPI. Una clase de dispositivo es un grupo de dispositivos o controladores de dispositivos a través de los cuales las aplicaciones envían y reciben información o datos de llamadas.
ms.assetid: 859979a8-0d16-4b7b-b183-d6e30f3e034d
title: Clases de dispositivo TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c16f5baf81bdc66d5110da2a1ac5127237738e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374759"
---
# <a name="tapi-device-classes"></a>Clases de dispositivo TAPI

Una clase de dispositivo es un grupo de dispositivos físicos o controladores de dispositivo relacionados a través de los cuales las aplicaciones envían y reciben la información o los datos que conste una llamada. Cada clase de  dispositivo tiene un nombre de clase de dispositivo que identifica de forma única la clase y proporciona información sobre la interfaz de programación y los comandos que se pueden usar para abrir y comunicarse con los dispositivos de la clase.

La Interfaz de programación de aplicaciones de telefonía (TAPI) asocia dispositivos de una o varias clases de dispositivo a cada dispositivo de línea o teléfono. Para acceder a uno de estos dispositivos, recupere el identificador del dispositivo mediante la [**función lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) [**o phoneGetID.**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) Proporcione el nombre de clase de dispositivo y la función devuelve el nombre de puerto, el nombre del dispositivo, el identificador de dispositivo o el identificador de dispositivo específicos que necesita para abrir el dispositivo y acceder a este. El formato de la información devuelta depende de la clase de dispositivo y se describe en temas posteriores de esta sección.

También se usan nombres de clase de dispositivo con las funciones [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) y [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) para permitir al usuario establecer opciones de configuración para el dispositivo determinado, con las funciones [**lineGetIcon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon) y [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon) para recuperar un icono para representar el dispositivo dado, y con las funciones [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) y [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) para recuperar y establecer directamente las opciones de configuración para el dispositivo determinado.

En la lista siguiente se muestran los nombres de clase de dispositivo.



| Nombre de clase de dispositivo                                      | Descripción                                       |
|--------------------------------------------------------|---------------------------------------------------|
| [Comm](comm.md)                                       | Puerto de comunicaciones.                              |
| [comm/datamodem](comm-datamodem.md)                   | Módem a través de un puerto de comunicaciones.              |
| [comm/datamodem/portname](comm-datamodem-portname.md) | Nombre del dispositivo al que está conectado un módem. |
| [wave/in](wave-in.md)                                 | Dispositivo de audio de onda (solo entrada).                   |
| [wave/out](wave-out.md)                               | Dispositivo de audio de onda (solo salida).                  |
| [wave/in/out](wave-in-out.md)                         | Dispositivo de audio de onda, dúplex completo.                   |
| [midi/in](midi-in.md)                                 | Secuenciador MIDI (solo entrada).                      |
| [midi/out](midi-out.md)                               | Secuenciador MIDI (solo salida).                     |
| [tapi/line](tapi-line.md)                             | Dispositivo de línea.                                      |
| [tapi/phone](tapi-phone.md)                           | Teléfono dispositivo.                                     |
| [Ndis](ndis.md)                                       | Dispositivo de red.                                   |
| [tapi/terminal](tapi-terminal.md)                     | Dispositivo terminal.                                  |



 

> [!Note]  
> Estos nombres no distinguen mayúsculas de minúsculas; puede usar cualquier combinación de letras mayúsculas y minúsculas.

 

Las clases de dispositivo adicionales y los nombres de clase de dispositivo pueden estar disponibles en un sistema determinado. En general, si un dispositivo no pertenece a una de las clases de dispositivo predeterminadas, el fabricante normalmente define una nueva clase de dispositivo y asigna un nombre de clase de dispositivo único. Consulte la documentación del dispositivo para determinar qué clases de dispositivos adicionales están disponibles para él. Tenga en cuenta, sin embargo, que aunque la clase de dispositivo y el tipo de medio están relacionados, no son iguales. Un tipo de medio describe el formato de información de llamada y una clase de dispositivo define la interfaz de programación utilizada para administrar esa información. Por lo tanto, incluso si un fabricante define un nuevo tipo de medio, no es necesariamente cierto que el fabricante también necesite definir una nueva clase de dispositivo para admitir el modo.

El formato de los datos de configuración usados con las funciones [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) y [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) también depende de la clase de dispositivo. En general, se usa **lineGetDevConfig para** guardar una copia de los datos de configuración actuales del dispositivo y, posteriormente, usar **lineSetDevConfig con** los datos de configuración guardados para restaurar la configuración del dispositivo al estado anterior. Esta es una manera cómoda de cambiar temporalmente la configuración sin necesidad de que el usuario la restaure manualmente al estado anterior. Dado que el formato exacto de los datos de configuración del dispositivo puede ser diferente con cada proveedor de servicios, no debe usar **lineSetDevConfig** y **lineGetDevConfig** para manipular directamente los datos de configuración del dispositivo. Algunos formatos solo se proporcionan para obtener información.

 

 



