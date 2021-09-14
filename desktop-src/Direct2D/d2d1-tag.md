---
title: D2D1_TAG (D2d1.h)
description: Valor de 64 bits definido por la aplicación que se usa para \ 160; marcar un conjunto de operaciones de representación.
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacd11aa016e64ed463f1809595c865ae7e1f124
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163477"
---
# <a name="d2d1_tag"></a>ETIQUETA D2D1 \_

Valor de 64 bits definido por la aplicación que se usa para marcar un conjunto de operaciones de representación.


```C++
typedef UINT64 D2D1_TAG;
```



## <a name="remarks"></a>Observaciones

Para establecer una etiqueta antes de una serie de operaciones de representación, use el [**método ID2D1RenderTarget::SetTags.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) Para recuperar la etiqueta actual, use el [**método ID2D1RenderTarget::GetTags.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y Actualización de plataforma para aplicaciones de escritorio Windows Vista \[ \| aplicaciones para UWP\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y Actualización de plataforma para aplicaciones de escritorio de Windows Server 2008 aplicaciones \[ \| para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>D2d1.h</dt> </dl>                                                        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 

