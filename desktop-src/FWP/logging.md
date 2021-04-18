---
title: Registro (plataforma de filtrado de Windows)
description: La plataforma de filtrado de Windows (WFP) proporciona el registro de caídas de paquetes y errores de IKE/AuthIP.
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27868c76a643a8e1b7b478152c100a2026bfc20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105665903"
---
# <a name="logging-windows-filtering-platform"></a>Registro (plataforma de filtrado de Windows)

La plataforma de filtrado de Windows (WFP) proporciona el registro de caídas de paquetes y errores de IKE/AuthIP.

Los eventos registrados se definen en el tipo enumerado de [**\_ tipo de \_ evento \_ FWPM net**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) y son los siguientes.

-   Errores de modo principal de IKE/AuthIP.
-   Errores de modo rápido de IKE/AuthIP.
-   Errores de modo extendido de AuthIP.
-   Paquetes descartados durante la clasificación.
-   Paquetes descartados por IPsec.

De forma predeterminada, el registro de WFP está habilitado para los paquetes entrantes de unidifusión y para todos los paquetes salientes (unidifusión, multidifusión y difusión). El registro se puede habilitar para el resto de los paquetes o deshabilitarse para todos los paquetes a través de la función de administración [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) . La configuración de eventos se mantiene entre reinicios.

Los eventos registrados se almacenan en un registro circular, es decir, los nuevos eventos reemplazan a los antiguos cuando el registro alcanza su tamaño máximo y se pueden analizar con las funciones de [Administración de eventos](fwp-mgmt-functions.md) que proporciona WFP. El registro de eventos tiene un tamaño máximo de 128 KB y puede contener aproximadamente 100 a 150 eventos.

Las funciones de enumeración en general y [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) en concreto, toman una instantánea del registro en el momento en que se crea el identificador de la enumeración. Las llamadas subsiguientes que usan el mismo identificador de enumeración devuelven el siguiente conjunto de elementos que se encuentra en el último búfer de salida.

Cuando una aplicación deshabilita el registro de WFP (llamando a [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)), todas las aplicaciones se ven afectadas. El registro de eventos no se limpia hasta que una aplicación vuelve a habilitar el registro de WFP, pero no se puede consultar el registro de eventos antes de.

El registro de eventos de WFP se vacía después de un reinicio.

 

 




