---
title: Conversión
description: Lo utiliza el cuadro de diálogo convertir para determinar los formatos que una aplicación puede leer y escribir.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- Clave del registro de conversión COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7f3a87594513c37a558d21fb7d001fc393763d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532457"
---
# <a name="conversion"></a>Conversión

Lo utiliza el cuadro de diálogo **convertir** para determinar los formatos que una aplicación puede leer y escribir.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Conversion
         Readable
            Main = rformat, ...
         ReadWritable
            Main = rwformat, ...
```

## <a name="remarks"></a>Observaciones

La información de conversión se usa en el cuadro de diálogo **convertir** para determinar qué formatos puede leer y escribir una aplicación. Un formato de archivo delimitado por comas se indica mediante un número si es uno de los formatos del portapapeles definido en Windows. h. Una cadena indica que el formato no es uno definido en Windows. h (privado). En este caso, el formato legible y grabable es CF \_ Outline (Private).

El valor *rformat* especifica el formato de archivo que una aplicación puede leer (convertir de).

El valor *rwformat* especifica el formato de archivo que una aplicación puede leer y escribir (activar como).

 

 




