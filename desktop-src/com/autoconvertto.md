---
title: AutoConvertTo
description: Especifica la conversión automática de una clase determinada de objetos en una nueva clase de objetos .
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- AutoConvertTo registry key COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ea2b32445bb7107dcbfdc2aec8aee518fdd474674e76fdbd820265d06b6160
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097055"
---
# <a name="autoconvertto"></a>AutoConvertTo

Especifica la conversión automática de una clase determinada de objetos en una nueva clase de objetos .

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG SZ** que especifica el identificador de clase del objeto al que se debe convertir el objeto o la clase de objetos especificados.

Esta clave se usa normalmente para convertir automáticamente los archivos creados por una versión anterior de una aplicación a una versión más reciente de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**OleDoAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[**OleGetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[**OleSetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




