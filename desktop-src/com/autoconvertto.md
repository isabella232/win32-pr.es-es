---
title: AutoConvertTo
description: Especifica la conversión automática de una clase determinada de objetos en una nueva clase de objetos .
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- AutoConvertTo registry key COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160f6591ed318ad7622e0bf3c0af5187f95d3be3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360877"
---
# <a name="autoconvertto"></a>AutoConvertTo

Especifica la conversión automática de una clase determinada de objetos en una nueva clase de objetos .

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ SZ reg** que especifica el identificador de clase del objeto al que se debe convertir el objeto o la clase de objetos especificados.

Esta clave se usa normalmente para convertir automáticamente los archivos creados por una versión anterior de una aplicación en una versión más reciente de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**OleDoAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[**OleGetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[**OleSetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




