---
title: Modificador /msc_ver
description: El modificador /msc ver se usa para permitir que MIDL genere código que incluya optimizaciones para diferentes versiones de compiladores \_ de Microsoft C/C++.
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /msc_ver switch MIDL
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f010224e5339ef89e05d1d96630dbedc0cb453eb8dafb4dd5e9c6edb3c24cc00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811375"
---
# <a name="msc_ver-switch"></a>Modificador /msc \_ ver

El **modificador /msc \_ ver** se usa para permitir que MIDL genere código que incluya optimizaciones para diferentes versiones de compiladores de Microsoft C/C++.

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*número de \_ versión* 
</dt> <dd>

Especifica un número de versión entero del Microsoft Visual C++ que se usará para compilar los códigos auxiliares de cliente y servidor de la aplicación distribuida. El número de versión predeterminado es 1100, que corresponde a Visual C++ versión 5.0. El número de versión 1200 corresponde a Visual C++ versión 6.0, y así sucesivamente.

</dd> </dl>

## <a name="remarks"></a>Comentarios

En concreto, los valores de versión de 1100 o superiores hacen que el compilador de MIDL genere código mediante **\_ \_ la directiva declspec(uuid()).** También activa macros que usan las directivas **\_ \_ declspec(selectany)** y **\_ \_ declspec(novtable).**

 

 




