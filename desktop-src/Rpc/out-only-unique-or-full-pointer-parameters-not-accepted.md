---
title: Out-Only parámetros único o de puntero completo no aceptados
description: El compilador de MIDL no acepta los punteros únicos o completos. Tales especificaciones hacen que el compilador MIDL genere un mensaje de error.
ms.assetid: 0477980e-d76e-452f-9ab1-71a8ed8642d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b21baa370c1b68fb3c708a8fdb21115686646f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533363"
---
# <a name="out-only-unique-or-full-pointer-parameters-not-accepted"></a>Out-Only parámetros único o de puntero completo no aceptados

\[ [](/windows/desktop/Midl/out-idl) \] El compilador MIDL no acepta los punteros únicos o completos que son de solo lectura. Tales especificaciones hacen que el compilador MIDL genere un mensaje de error.

El código auxiliar de servidor generado automáticamente tiene que asignar memoria para el puntero de forma que la aplicación de servidor pueda almacenar datos en ese área de memoria. Según la definición de un parámetro de solo **\[ salida \]**, no se transmite información sobre el parámetro desde el cliente al servidor. En el caso de un puntero único, que puede tomar el valor null, el código auxiliar del servidor no tiene suficiente información para duplicar correctamente el puntero único en el espacio de direcciones del servidor, ni tampoco información sobre si el puntero debe apuntar a una dirección válida o si debe establecerse en NULL. Por lo tanto, esta combinación no está permitida.

En lugar de \[ **out**, [Unique](/windows/desktop/Midl/unique) \] o \[ **out**, punteros [ptr](/windows/desktop/Midl/ptr) \] , use \[ **in**, **out**, **Unique** \] o \[ **in**, **out** o **ptr** , \] o use otro nivel de direccionamiento indirecto, como un puntero de referencia que apunte al puntero completo o único válido.

 

 