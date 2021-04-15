---
description: Una clase de dispositivo es un grupo de dispositivos físicos relacionados o controladores de dispositivos a través de los cuales las aplicaciones envían y reciben la información o los datos que componen una llamada.
ms.assetid: 859979a8-0d16-4b7b-b183-d6e30f3e034d
title: Clases de dispositivos TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357d68e07359468e7a3ba3a1e73c3e0888076e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689542"
---
# <a name="tapi-device-classes"></a>Clases de dispositivos TAPI

Una clase de dispositivo es un grupo de dispositivos físicos relacionados o controladores de dispositivos a través de los cuales las aplicaciones envían y reciben la información o los datos que componen una llamada. Cada clase de dispositivo tiene un *nombre de clase de dispositivo* que identifica de forma única la clase y proporciona información sobre la interfaz de programación y los comandos que se pueden usar para abrir y comunicarse con los dispositivos de la clase.

La interfaz de programación de aplicaciones de telefonía (TAPI) asocia dispositivos de una o varias clases de dispositivos a cada dispositivo de línea o teléfono. Puede acceder a uno de estos dispositivos recuperando el identificador de dispositivo para el dispositivo mediante la función [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) o [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) . Proporcione el nombre de la clase de dispositivo y la función devolverá el nombre de puerto específico, el nombre del dispositivo, el identificador del dispositivo o el identificador de dispositivo que necesita para abrir y acceder al dispositivo. El formato de la información devuelta depende de la clase de dispositivo y se describe en los temas siguientes de esta sección.

También puede usar nombres de clase de dispositivo con las funciones [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) y [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) para permitir al usuario establecer las opciones de configuración para el dispositivo dado, con las funciones [**lineGetIcon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon) y [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon) para recuperar un icono para representar el dispositivo determinado y con las funciones [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) y [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) para recuperar y establecer directamente las opciones de configuración para el dispositivo especificado.

La lista siguiente muestra los nombres de clase de dispositivo.



| Nombre de clase de dispositivo                                      | Descripción                                       |
|--------------------------------------------------------|---------------------------------------------------|
| [com](comm.md)                                       | Puerto de comunicaciones.                              |
| [COMM/telemodem](comm-datamodem.md)                   | Módem a través de un puerto de comunicaciones.              |
| [COMM/telemodem/portname](comm-datamodem-portname.md) | Nombre del dispositivo al que está conectado un módem. |
| [onda/en](wave-in.md)                                 | Dispositivo de audio de onda (solo entrada).                   |
| [onda/salida](wave-out.md)                               | Dispositivo de audio de onda (solo salida).                  |
| [Wave/in/out](wave-in-out.md)                         | Dispositivo de audio de onda, dúplex completo.                   |
| [MIDI/in](midi-in.md)                                 | MIDI Sequencer (solo entrada).                      |
| [MIDI/salida](midi-out.md)                               | MIDI Sequencer (solo salida).                     |
| [TAPI/línea](tapi-line.md)                             | Dispositivo de línea.                                      |
| [TAPI/teléfono](tapi-phone.md)                           | Dispositivo telefónico.                                     |
| [NDIS](ndis.md)                                       | Dispositivo de red.                                   |
| [TAPI/terminal](tapi-terminal.md)                     | Dispositivo terminal.                                  |



 

> [!Note]  
> Estos nombres no distinguen mayúsculas de minúsculas; puede usar cualquier combinación de mayúsculas y minúsculas.

 

Es posible que las clases de dispositivo y los nombres de clase de dispositivo adicionales estén disponibles en un sistema determinado. En general, si un dispositivo no pertenece a una de las clases de dispositivos predeterminadas, el fabricante normalmente define una nueva clase de dispositivo y asigna un nombre de clase de dispositivo único. Consulte la documentación del dispositivo para determinar qué clases de dispositivo adicionales están disponibles para él. Tenga en cuenta, sin embargo, que aunque la clase de dispositivo y el tipo de medio están relacionados, no son los mismos. Un tipo de medio describe el formato de la información de llamada y una clase de dispositivo define la interfaz de programación que se usa para administrar esa información. Por lo tanto, incluso si un fabricante define un nuevo tipo de medio, no es necesariamente que el fabricante también tenga que definir una nueva clase de dispositivo para admitir el modo.

El formato de los datos de configuración que se usan con las funciones [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) y [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) también depende de la clase de dispositivo. En general, se usa **lineGetDevConfig** para guardar una copia de los datos de configuración del dispositivo actual y, posteriormente, usar **lineSetDevConfig** con los datos de configuración guardados para restaurar la configuración del dispositivo al estado anterior. Esta es una manera cómoda de cambiar temporalmente la configuración sin necesidad de que el usuario la restaure manualmente al estado anterior. Dado que el formato exacto de los datos de configuración del dispositivo puede ser diferente con cada proveedor de servicios, no debe usar **lineSetDevConfig** y **lineGetDevConfig** para manipular directamente los datos de configuración del dispositivo. Algunos formatos solo se proporcionan para obtener información.

 

 



