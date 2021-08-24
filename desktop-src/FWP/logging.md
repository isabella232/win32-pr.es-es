---
title: Registro (plataforma Windows filtrado de datos)
description: Windows La plataforma de filtrado (WFP) proporciona el registro de pérdidas de paquetes y errores de IKE/AuthIP.
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1500be04837126e6907b663e4496c58c05380d313a1465b9c8db05b5ea39d832
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068915"
---
# <a name="logging-windows-filtering-platform"></a>Registro (plataforma Windows filtrado de datos)

La plataforma Windows filtrado de paquetes (WFP) proporciona el registro de pérdidas de paquetes y errores de IKE/AuthIP.

Los eventos registrados se definen en el tipo enumerado [**FWPM \_ NET EVENT \_ \_ TYPE**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) y son los siguientes.

-   Errores del modo principal de IKE/AuthIP.
-   Errores de modo rápido de IKE/AuthIP.
-   Errores de modo extendido de AuthIP.
-   Paquetes descartados durante la clasificación.
-   Paquetes descartados por IPsec.

De forma predeterminada, el registro de WFP está habilitado para los paquetes entrantes de unidifusión y para todos los paquetes salientes (unidifusión, multidifusión y difusión). El registro se puede habilitar para el resto de los paquetes o deshabilitarse para todos los paquetes mediante la función de administración [**FwpmEngineSetOptions0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) La configuración de eventos persiste entre reinicios.

Los eventos registrados se almacenan en un registro circular, es decir, los eventos nuevos reemplazan a los antiguos cuando el registro alcanza su tamaño máximo y se pueden analizar mediante las funciones de administración de eventos proporcionadas por WFP. [](fwp-mgmt-functions.md) El registro de eventos tiene un tamaño máximo de 128 KB y puede contener entre 100 y 150 eventos.

En general, las funciones de enumeración [**y FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) toman una instantánea del registro en el momento en que se crea el identificador de enumeración. Las llamadas posteriores que usan el mismo identificador de enumeración devuelven el siguiente conjunto de elementos que sigue a los del último búfer de salida.

Cuando una aplicación deshabilita el registro de WFP (mediante una llamada [**a FwpmEngineSetOptions0),**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)todas las aplicaciones se ven afectadas. El registro de eventos no se limpia hasta que una aplicación vuelve a habilitar el registro WFP, pero no se puede consultar el registro de eventos antes de ese momento.

El registro de eventos WFP se vacía después de un reinicio.

 

 




