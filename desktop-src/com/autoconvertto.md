---
title: Conversión a
description: Especifica la conversión automática de una clase determinada de objetos en una nueva clase de objetos.
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- Convertir en COM clave del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160f6591ed318ad7622e0bf3c0af5187f95d3be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103902994"
---
# <a name="autoconvertto"></a>Conversión a

Especifica la conversión automática de una clase determinada de objetos en una nueva clase de objetos.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **reg \_ SZ** que especifica el identificador de clase del objeto al que se debe convertir el objeto o la clase de objetos especificados.

Esta clave se usa normalmente para convertir automáticamente los archivos creados por una versión anterior de una aplicación a una versión más reciente de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**OleDoAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[**OleGetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[**OleSetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




