---
description: Las funciones de configuración del módem permiten configurar un módem antes de realizar una conexión.
ms.assetid: 67d8f3c4-0295-4028-8b12-1a5e26979df5
title: Configuración del módem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7abd6c5319011b8821487b6adf0351dc799e61f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164361"
---
# <a name="modem-configuration"></a>Configuración del módem

Las funciones de configuración del módem permiten configurar un módem antes de realizar una conexión. Una aplicación puede establecer opciones de módem y determinar las características de un módem sin usar comandos específicos de ningún dispositivo de módem. Estas son las características generales que una aplicación puede establecer antes de realizar una llamada:

-   Modo de operación principal (sincrónico, asincrónico y si el control de errores está habilitado).
-   Control de errores V.42 (definido por la recomendación de CCITT V.42), incluidos parámetros específicos. CCITT es el nombre del Comité Internacional de Telegrafía y Consulta telefónica.
-   V.42bis (definido por la recomendación de CCITT V.42bis) y compresión de datos MNP5.
-   Opciones de tiempo de espera, incluida la configuración de llamadas, la inactividad y la entrega de datos almacenados en búfer.

Antes de establecer la configuración de un módem, una aplicación debe determinar las funcionalidades del dispositivo de módem mediante la [**función GetCommProperties.**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties) Esta función rellena una [**estructura COMMPROP.**](/windows/desktop/api/WinBase/ns-winbase-commprop) Esta estructura contiene una parte general, que se aplica a todos los dispositivos de comunicaciones, y una parte específica de cada subtipo de proveedor. En el caso de los dispositivos de módem, la parte específica del proveedor de la **estructura COMMPROP** es una [**estructura MODEMDEVCAPS.**](/windows/desktop/api/Mcx/ns-mcx-modemdevcaps)

Una aplicación puede obtener y establecer la configuración actual de un módem mediante las funciones [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) y [**SetCommConfig,**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) que usan una [**estructura COMMCONFIG.**](/windows/desktop/api/Winbase/ns-winbase-commconfig) Esta estructura contiene una parte general, que se aplica a todos los dispositivos de comunicaciones, y una parte específica de cada subtipo de proveedor. En el caso de los dispositivos de módem, la parte específica del proveedor de la **estructura COMMCONFIG** es una [**estructura MODEMSETTINGS.**](/windows/desktop/api/Mcx/ns-mcx-modemsettings)

Después de configurar un módem, una aplicación puede usar la Interfaz de programación de aplicaciones de telefonía (TAPI) para establecer realmente una conexión.

Las funciones de configuración del módem no proporcionan para la administración y el mantenimiento a largo plazo de un módem. Los proveedores de servicios de módem deben proporcionar cuadros de diálogo de configuración de módem para este propósito.

 

 



