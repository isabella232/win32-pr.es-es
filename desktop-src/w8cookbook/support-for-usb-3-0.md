---
title: Compatibilidad con USB 3.0
description: Compatibilidad con USB 3.0
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2f6fa342efa5e7b4fd95287a2061482fa0cbb9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466265"
---
# <a name="support-for-usb-30"></a>Compatibilidad con USB 3.0

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8  
**Servidores:** Windows Server 2012  


## <a name="description"></a>Descripción

En Windows 8 y Windows Server 2012, hemos agregado compatibilidad con USB 3.0. Para ello, agregamos una nueva pila de software para encender el controlador de host USB 3.0, denominado controlador de host eXtensible (XHC). Hemos mantenido la paridad de la interfaz, el nivel de IRQL, el contexto del autor de la llamada, el estado de error, la frecuencia de reintento, entre otros. No debería haber ninguna diferencia al interactuar con un dispositivo conectado a través de USB 2.0 frente a USB 3.0.

Sin embargo, si va a escribir un controlador para un nuevo dispositivo USB 3.0, opte definitivamente por nuevas funcionalidades USB 3.0.

## <a name="manifestation"></a>Manifestación

Las transferencias de dispositivos son más rápidas y, en general, los dispositivos USB consumen menos energía desde un equipo. Existe el riesgo de que los dispositivos USB existentes no funcionen correctamente cuando se conecten a un puerto USB 3.0. Esto no debería ocurrir y no se espera, pero, dado que el software que impulsa USB 3.0 es nuevo, es un riesgo.

 

 




