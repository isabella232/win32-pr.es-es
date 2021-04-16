---
description: Algunos tipos definidos por TSPI son controladores opacos.
ms.assetid: e52ed691-0479-48da-9e06-c6a0d7a20e10
title: Manipuladores opacos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df2e0b0f608b9cefc8f0f4f538bffd452a8aab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542822"
---
# <a name="opaque-handles"></a>Manipuladores opacos

Algunos tipos definidos por TSPI son controladores opacos. Se usan en TSPI como referencias públicas a las estructuras de datos privadas. Esto permite la comprobación de tipos de los parámetros proporcionados a los procedimientos de interfaz y, al mismo tiempo, proporciona una medida de protección de tipos. Solo el propietario de la estructura de datos privada sabe cómo interpretar el tipo opaco como una referencia a su representación de la estructura de datos. Como ejemplo de cómo se usan los identificadores opacos, considere la posibilidad de usar un dispositivo de teléfono. Tanto TAPI como el proveedor de servicios suelen mantener las estructuras de datos que representan sus vistas correspondientes del dispositivo.

En las estructuras de datos de teléfono típicas mantenidas por TAPI y un proveedor de servicios, cada contiene un identificador opaco para la otra estructura de datos. Se intercambiaron en un paso de inicialización temprana. Cuando TAPI llama a una función TSPI, pasa el identificador opaco para hacer referencia al dispositivo. El proveedor de servicios sabe cómo resolver esto como una referencia (flecha) a su estructura de datos. Se produce un proceso similar cuando el proveedor de servicios llama a una función de devolución de llamada en TAPI.

 

 



