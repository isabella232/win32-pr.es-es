---
description: Una clase de dispositivo es un grupo de dispositivos físicos relacionados o controladores de dispositivos a través de los cuales las aplicaciones envían y reciben la información o los datos que componen una llamada.
ms.assetid: b29ea789-d017-4e35-b77a-c0d54ac54c66
title: Clases de dispositivos TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10392487657e8190052546605c54bed8cc0ccf4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361529"
---
# <a name="tspi-device-classes"></a>Clases de dispositivos TSPI

Una *clase de dispositivo* es un grupo de dispositivos físicos relacionados o controladores de dispositivos a través de los cuales las aplicaciones envían y reciben la información o los datos que componen una llamada. Cada clase de dispositivo tiene un *nombre de clase de dispositivo* que identifica de forma única la clase y proporciona información sobre la interfaz de programación y los comandos que se pueden usar para abrir y comunicarse con los dispositivos de la clase.

La interfaz de programación de aplicaciones de telefonía (TAPI) asocia dispositivos de una o varias clases de dispositivos a cada dispositivo de línea o teléfono. Puede acceder a uno de estos dispositivos recuperando el identificador de dispositivo para el dispositivo mediante la función [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid) o [**phoneGetID**](/windows/win32/api/tapi/nf-tapi-phonegetid) . Proporcione el nombre de la clase de dispositivo y la función devolverá el nombre de puerto específico, el nombre del dispositivo, el identificador del dispositivo o el identificador de dispositivo que necesita para abrir y acceder al dispositivo. El formato de la información devuelta depende de la clase de dispositivo y se describe en esta sección.

También puede usar nombres de clase de dispositivo con las funciones [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) y [**phoneConfigDialog**](/windows/win32/api/tapi/nf-tapi-phoneconfigdialog) para permitir al usuario establecer las opciones de configuración para el dispositivo especificado. con las funciones [**lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon) y [**phoneGetIcon**](/windows/win32/api/tapi/nf-tapi-phonegeticon) para recuperar un icono que represente el dispositivo determinado; y con las funciones [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) y [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) para recuperar y establecer directamente las opciones de configuración para el dispositivo especificado.

A continuación se muestran los nombres de clase de dispositivo predeterminados.



| Nombre de clase de dispositivo                                       | Descripción                                      |
|---------------------------------------------------------|--------------------------------------------------|
| [com](/previous-versions/windows/desktop/legacy/ms725177(v=vs.85))                                       | Puerto de comunicaciones                              |
| [COMM/telemodem](/previous-versions/windows/desktop/legacy/ms725178(v=vs.85))                   | Módem a través de un puerto de comunicaciones              |
| [COMM/telemodem/portname](/previous-versions/windows/desktop/legacy/ms725179(v=vs.85)) | Nombre del dispositivo al que está conectado un módem |
| [onda/en](/previous-versions/windows/desktop/legacy/ms725990(v=vs.85))                                 | Dispositivo Wave audio (solo entrada)                   |
| [onda/salida](/previous-versions/windows/desktop/legacy/ms725992(v=vs.85))                               | Dispositivo Wave audio (solo salida)                  |
| [Wave/in/out](/previous-versions/windows/desktop/legacy/ms725991(v=vs.85))                         | Dispositivo de audio de onda, dúplex completo                   |
| [MIDI/in](/previous-versions/windows/desktop/legacy/ms725244(v=vs.85))                                 | MIDI Sequencer (solo entrada)                      |
| [MIDI/salida](/previous-versions/windows/desktop/legacy/ms725245(v=vs.85))                               | MIDI Sequencer (solo salida)                     |
| [TAPI/línea](/previous-versions/windows/desktop/legacy/ms725511(v=vs.85))                             | Dispositivo de línea                                      |
| [TAPI/teléfono](/previous-versions/windows/desktop/legacy/ms725512(v=vs.85))                           | Dispositivo telefónico                                     |
| [NDIS](/previous-versions/windows/desktop/legacy/ms725247(v=vs.85))                                       | Dispositivo de red                                   |
| [TAPI/terminal](/previous-versions/windows/desktop/legacy/ms725515(v=vs.85))                     | Dispositivo terminal                                  |



 

Estos nombres no distinguen mayúsculas de minúsculas, por lo que puede usar cualquier combinación de mayúsculas y minúsculas.

Es posible que las clases de dispositivo y los nombres de clase de dispositivo adicionales estén disponibles en un sistema determinado. En general, si un dispositivo no pertenece a una de las clases de dispositivos predeterminadas, el fabricante normalmente define una nueva clase de dispositivo y asigna un nombre de clase de dispositivo único. Debe consultar la documentación del dispositivo para determinar qué clases de dispositivo adicionales están disponibles para él. Tenga en cuenta, sin embargo, que aunque la clase de dispositivo y el tipo de medio están relacionados, no son los mismos. Un *tipo de archivo multimedia* describe el formato de la información en una llamada y una *clase de dispositivo* define la interfaz de programación que se usa para administrar esa información. Por lo tanto, incluso si un fabricante define un nuevo tipo de medio, puede que no sea cierto que el fabricante también debe definir una nueva clase de dispositivo para admitir el modo.

El formato de los datos de configuración que se usan con las funciones [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) y [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) también depende de la clase de dispositivo. En general, se usa **lineGetDevConfig** para guardar una copia de los datos de configuración del dispositivo actual y, posteriormente, usar **lineSetDevConfig** con los datos de configuración guardados para restaurar la configuración del dispositivo al estado anterior. Esta es una manera cómoda de cambiar temporalmente la configuración sin necesidad de que el usuario la restaure manualmente al estado anterior. Dado que el formato exacto de los datos de configuración del dispositivo puede ser diferente con cada proveedor de servicios, no use **lineSetDevConfig** y **lineGetDevConfig** para manipular directamente los datos de configuración del dispositivo. Algunos formatos se proporcionan únicamente como información.

 

 
