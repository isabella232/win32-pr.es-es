---
title: Out-Only parámetros de puntero único o completo no aceptados
description: El compilador MIDL no acepta los punteros únicos o completos que son \ out\. Estas especificaciones hacen que el compilador MIDL genere un mensaje de error.
ms.assetid: 0477980e-d76e-452f-9ab1-71a8ed8642d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9511c21045892eb7a5b3230d8f0180578b489b06b5b5402fb0b11f6a3ff31a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927574"
---
# <a name="out-only-unique-or-full-pointer-parameters-not-accepted"></a>Out-Only parámetros de puntero único o completo no aceptados

El compilador MIDL no acepta los punteros únicos o completos que están fuera \[ [](/windows/desktop/Midl/out-idl) \] de -only. Estas especificaciones hacen que el compilador MIDL genere un mensaje de error.

El código auxiliar de servidor generado automáticamente tiene que asignar memoria para el referenciador de puntero para que la aplicación de servidor pueda almacenar datos en ese área de memoria. Según la definición de un **\[ parámetro out \]**-only, no se transmite información sobre el parámetro de cliente a servidor. En el caso de un puntero único, que puede tomar el valor NULL, el código auxiliar del servidor no tiene suficiente información para duplicar correctamente el puntero único en el espacio de direcciones del servidor, ni el código auxiliar tiene información sobre si el puntero debe apuntar a una dirección válida o si debe establecerse en NULL. Por lo tanto, no se permite esta combinación.

En lugar de out , único u out \[ , punteros [](/windows/desktop/Midl/unique) ptr, use en , out , unique o en \] , \[  [](/windows/desktop/Midl/ptr) \] \[    \] \[  **out**, **ptr** \] pointers, o use otro nivel de direccionamiento indirecto, como un puntero de referencia que apunta al puntero único o completo válido.

 

 