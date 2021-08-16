---
description: Cuando se usa Windows de adquisición de imágenes (WIA) en más de un subproceso dentro de un único proceso, una aplicación debe proporcionar la configuración de la base de datos para esa interfaz.
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: Uso de varios subprocesos en una aplicación WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707adbfe6cd24152209e318bed73a0b6d7fee54b6cfa1e8fbcfecac67e272082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208011"
---
# <a name="using-multiple-threads-in-a-wia-application"></a>Uso de varios subprocesos en una aplicación WIA

Cuando se usa Windows de adquisición de imágenes (WIA) en más de un subproceso dentro de un único proceso, una aplicación debe proporcionar la configuración de la base de datos para esa interfaz. Si un subproceso crea un puntero de interfaz, no puede usar ese puntero en un subproceso diferente sin la creación de la referencia.

Por ejemplo, si un subproceso de una aplicación obtiene un puntero a la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2,**](-wia-iwiaitem2.md) un subproceso independiente no puede usar ese puntero de interfaz sin la marshalling.

Una técnica común que se usa para realizar esta marshalling es usar la tabla de interfaz global. La tabla de interfaz global es una tabla que se mantiene en todos los subprocesos dentro de un único proceso. Todos los subprocesos que se ejecutan dentro del proceso pueden recuperar interfaces registradas en la tabla de interfaz global. Esta técnica evita la necesidad de crear secuencias para pasar interfaces entre subprocesos.

Para obtener información sobre cómo usar la tabla de interfaz global, vea [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

Incluso si no piensa usar varios subprocesos en una aplicación WIA, debe suponer que todas las funciones de devolución de llamada de eventos de dispositivo o transferencia de datos se ejecutan en subprocesos independientes.

 

 
