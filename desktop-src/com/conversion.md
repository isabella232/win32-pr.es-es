---
title: Conversión
description: Usado por el cuadro de diálogo Convertir para determinar los formatos que una aplicación puede leer y escribir.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- COM de clave del Registro de conversión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7f3a87594513c37a558d21fb7d001fc393763d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369579"
---
# <a name="conversion"></a>Conversión

Usado por el **cuadro de** diálogo Convertir para determinar los formatos que una aplicación puede leer y escribir.

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

El cuadro de diálogo Convertir usa **la** información de conversión para determinar qué formatos puede leer y escribir una aplicación. Un número indica un formato de archivo delimitado por comas si es uno de los formatos del Portapapeles definidos en Windows.h. Una cadena indica que el formato no está definido en Windows.h (privado). En este caso, el formato legible y grabable es CF \_ OUTLINE (privado).

El *valor rformat* especifica el formato de archivo que una aplicación puede leer (desde el que se convierte).

El *valor rwformat* especifica el formato de archivo que una aplicación puede leer y escribir (activar como).

 

 




