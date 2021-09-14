---
description: Teléfono compatibilidad con dispositivos es complementaria en lugar de básica, por lo que no es necesario que los proveedores de servicios admitan dispositivos telefónicos.
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: Teléfono Dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f406442e43d8d4f31a89bfc0ccb1e59916d33e0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071089"
---
# <a name="phone-devices"></a>Teléfono Dispositivos

Teléfono compatibilidad con dispositivos es complementaria en lugar de básica, por lo que no es necesario que los proveedores de servicios admitan dispositivos telefónicos.

Al igual que una clase de dispositivo de línea es una abstracción de un dispositivo de línea física, la clase de dispositivo de teléfono representa una abstracción independiente del dispositivo de un conjunto de teléfonos. TAPI trata los dispositivos de línea y teléfono como dispositivos independientes entre sí. En otras palabras, puede usar un teléfono (dispositivo) sin usar una línea asociada y puede usar una línea (dispositivo) sin usar un teléfono.

Los proveedores de servicios que implementan completamente esta independencia pueden ofrecer usos para estos dispositivos no definidos por los protocolos de telefonía tradicionales. Por ejemplo, una persona puede usar el terminal del teléfono del escritorio como un dispositivo de audio de forma de onda para la grabación o reproducción de voz, quizás sin que el conmutador sepa que el teléfono está en uso. En este tipo de implementación, el izado del teléfono local no necesita enviar automáticamente una señal de offhook al conmutador.

Esta independencia también permite que una aplicación llame al teléfono local de una manera independiente de las llamadas entrantes. Las funcionalidades de los proveedores de servicios están limitadas por las funcionalidades del hardware y el software que se usan para interconectar el conmutador, el teléfono y el equipo.

TAPI incluye funciones para recuperar funcionalidades de dispositivo que permiten a los clientes determinar si se admite este modelo de uso.

En esta sección se describen los dispositivos telefónicos y se explica cómo usar las funciones de teléfono TAPI para acceder a estos dispositivos.

-   [Teléfono Dispositivo](phone-device-elements.md)
-   [Inicialización y apagado](initialization-and-shutdown.md)

 

 



