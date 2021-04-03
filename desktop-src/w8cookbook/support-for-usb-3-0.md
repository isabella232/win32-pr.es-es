---
title: Compatibilidad con USB 3,0
description: Compatibilidad con USB 3,0
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2f6fa342efa5e7b4fd95287a2061482fa0cbb9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "103794218"
---
# <a name="support-for-usb-30"></a>Compatibilidad con USB 3,0

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


## <a name="description"></a>Descripción

En Windows 8 y Windows Server 2012, se ha agregado compatibilidad con USB 3,0. Para ello, hemos agregado una nueva pila de software para potenciar el controlador de host USB 3,0, denominado controlador de host extensible (XHC). Mantuvimos la paridad de la interfaz, el nivel de IRQL, el contexto del autor de la llamada, el estado de error, la frecuencia de reintento, etc. No debe haber ninguna diferencia cuando interactúe con un dispositivo conectado a través de USB 2,0 frente a USB 3,0.

Sin embargo, si está escribiendo un controlador para un nuevo dispositivo USB 3,0, definitivamente opta por las nuevas capacidades de USB 3,0.

## <a name="manifestation"></a>Manifestación

Las transferencias de dispositivos son más rápidas y el consumo de energía de un equipo de dispositivos USB es menor. Existe el riesgo de que los dispositivos USB existentes no funcionen correctamente cuando se conectan a un puerto USB 3,0. Esto no debería ocurrir y no se espera, pero, dado que el software que alimenta USB 3,0 es nuevo, es un riesgo.

 

 




