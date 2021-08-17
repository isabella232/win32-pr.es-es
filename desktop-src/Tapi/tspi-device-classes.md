---
description: Obtenga información sobre las clases de dispositivo TSPI. Una clase de dispositivo es un grupo de dispositivos o controladores de dispositivos a través del cual las aplicaciones envían y reciben información o datos de llamadas.
ms.assetid: b29ea789-d017-4e35-b77a-c0d54ac54c66
title: Clases de dispositivo TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd6d2e79e021b6b73bc24ef0edb5b343fb8487ced3ca414084c7f2ad23a6c48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975445"
---
# <a name="tspi-device-classes"></a>Clases de dispositivo TSPI

Una *clase de dispositivo* es un grupo de dispositivos físicos o controladores de dispositivo relacionados a través de los cuales las aplicaciones envían y reciben la información o los datos que forma una llamada. Cada clase de  dispositivo tiene un nombre de clase de dispositivo que identifica de forma única la clase y proporciona información sobre la interfaz de programación y los comandos que se pueden usar para abrir y comunicarse con los dispositivos de la clase.

La interfaz de programación de aplicaciones de telefonía (TAPI) asocia dispositivos de una o varias clases de dispositivo a cada dispositivo de línea o teléfono. Para acceder a uno de estos dispositivos, recupere el identificador del dispositivo mediante la función [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid) [**o phoneGetID.**](/windows/win32/api/tapi/nf-tapi-phonegetid) Proporcione el nombre de clase de dispositivo y la función devuelve el nombre de puerto, el nombre del dispositivo, el identificador de dispositivo o el identificador de dispositivo específicos que necesita para abrir y acceder al dispositivo. El formato de la información devuelta depende de la clase de dispositivo y se describe en esta sección.

También se usan nombres de clase de dispositivo con las funciones [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) y [**phoneConfigDialog**](/windows/win32/api/tapi/nf-tapi-phoneconfigdialog) para permitir al usuario establecer opciones de configuración para el dispositivo determinado. con las [**funciones lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon) [**y phoneGetIcon**](/windows/win32/api/tapi/nf-tapi-phonegeticon) para recuperar un icono para representar el dispositivo dado; y con las [**funciones lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) y [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) para recuperar y establecer directamente las opciones de configuración para el dispositivo determinado.

A continuación se encuentran los nombres de clase de dispositivo predeterminados.



| Nombre de clase de dispositivo                                       | Descripción                                      |
|---------------------------------------------------------|--------------------------------------------------|
| [Comm](/previous-versions/windows/desktop/legacy/ms725177(v=vs.85))                                       | Puerto de comunicaciones                              |
| [comm/datamodem](/previous-versions/windows/desktop/legacy/ms725178(v=vs.85))                   | Módem a través de un puerto de comunicaciones              |
| [comm/datamodem/portname](/previous-versions/windows/desktop/legacy/ms725179(v=vs.85)) | Nombre del dispositivo al que está conectado un módem |
| [wave/in](/previous-versions/windows/desktop/legacy/ms725990(v=vs.85))                                 | Dispositivo de audio ondulado (solo entrada)                   |
| [wave/out](/previous-versions/windows/desktop/legacy/ms725992(v=vs.85))                               | Dispositivo de audio de onda (solo salida)                  |
| [wave/in/out](/previous-versions/windows/desktop/legacy/ms725991(v=vs.85))                         | Dispositivo de audio ondulado, dúplex completo                   |
| [midi/in](/previous-versions/windows/desktop/legacy/ms725244(v=vs.85))                                 | Secuenciador DE LÍNEA (solo entrada)                      |
| [midi/out](/previous-versions/windows/desktop/legacy/ms725245(v=vs.85))                               | Secuenciador DE LÍNEA (solo salida)                     |
| [tapi/line](/previous-versions/windows/desktop/legacy/ms725511(v=vs.85))                             | Dispositivo de línea                                      |
| [tapi/phone](/previous-versions/windows/desktop/legacy/ms725512(v=vs.85))                           | Teléfono dispositivo                                     |
| [Ndis](/previous-versions/windows/desktop/legacy/ms725247(v=vs.85))                                       | Dispositivo de red                                   |
| [tapi/terminal](/previous-versions/windows/desktop/legacy/ms725515(v=vs.85))                     | Dispositivo terminal                                  |



 

Estos nombres no distinguen mayúsculas de minúsculas, por lo que puede usar cualquier combinación de letras mayúsculas y minúsculas.

Las clases de dispositivo y los nombres de clase de dispositivo adicionales pueden estar disponibles en un sistema determinado. En general, si un dispositivo no pertenece a una de las clases de dispositivo predeterminadas, el fabricante normalmente define una nueva clase de dispositivo y asigna un nombre de clase de dispositivo único. Debe consultar la documentación del dispositivo para determinar qué clases de dispositivo adicionales están disponibles para él. Sin embargo, tenga en cuenta que, aunque la clase de dispositivo y el tipo de medio están relacionados, no son iguales. Un *tipo de medio* describe un formato de  información en una llamada y una clase de dispositivo define la interfaz de programación utilizada para administrar esa información. Por lo tanto, incluso si un fabricante define un nuevo tipo de medio, puede que no sea cierto que el fabricante también deba definir una nueva clase de dispositivo para admitir el modo.

El formato de los datos de configuración utilizados con las funciones [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) y [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) también depende de la clase de dispositivo. En general, se usa **lineGetDevConfig** para guardar una copia de los datos de configuración actuales del dispositivo y, después, usar **lineSetDevConfig con** los datos de configuración guardados para restaurar la configuración del dispositivo al estado anterior. Esta es una manera cómoda de cambiar temporalmente la configuración sin necesidad de que el usuario la restaure manualmente al estado anterior. Dado que el formato exacto de los datos de configuración del dispositivo puede ser diferente con cada proveedor de servicios, no use **lineSetDevConfig** y **lineGetDevConfig** para manipular directamente los datos de configuración del dispositivo. Algunos formatos solo se proporcionan para obtener información.

 

 
