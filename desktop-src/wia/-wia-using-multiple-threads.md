---
description: Cuando se usa una interfaz de adquisición de imágenes de Windows (WIA) en más de un subproceso dentro de un único proceso, una aplicación debe proporcionar la serialización de la interfaz.
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: Usar varios subprocesos en una aplicación WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb1dbfa552e72dc068aff63a0a316d9af680ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154382"
---
# <a name="using-multiple-threads-in-a-wia-application"></a>Usar varios subprocesos en una aplicación WIA

Cuando se usa una interfaz de adquisición de imágenes de Windows (WIA) en más de un subproceso dentro de un único proceso, una aplicación debe proporcionar la serialización de la interfaz. Si un subproceso crea un puntero de interfaz, no puede usar ese puntero en un subproceso diferente sin serialización.

Por ejemplo, si un subproceso de una aplicación obtiene un puntero a la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) , un subproceso independiente no puede usar ese puntero de interfaz sin serialización.

Una técnica común que se usa para realizar esta serialización es usar la tabla de interfaz global. La tabla de interfaz global es una tabla que se mantiene en todos los subprocesos dentro de un único proceso. Todos los subprocesos que se ejecutan dentro del proceso pueden recuperar interfaces registradas en la tabla de interfaz global. Esta técnica evita la necesidad de crear secuencias para pasar interfaces entre subprocesos.

Para obtener información sobre cómo usar la tabla de interfaz global, vea [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

Incluso si no piensa usar varios subprocesos en una aplicación WIA, debe suponer que todas las funciones de devolución de llamada de eventos de dispositivo o de transferencia de datos se ejecutan en subprocesos independientes.

 

 
