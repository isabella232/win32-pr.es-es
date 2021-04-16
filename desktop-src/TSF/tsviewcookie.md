---
title: TsViewCookie (Textstor. h)
description: El tipo de datos TsViewCookie identifica una vista de contexto.
ms.assetid: e649b799-d0d6-4f2d-b9f1-28070eea9b16
keywords:
- TsViewCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb43f888f76410e83e89d037f39ea665ca548ec9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685913"
---
# <a name="tsviewcookie"></a>TsViewCookie

El tipo de datos **TsViewCookie** identifica una vista de contexto.


```C++
typedef DWORD TsViewCookie;
```



## <a name="remarks"></a>Observaciones

Una aplicación debe proporcionar un valor de **TsViewCookie** único para cada vista que cree.

El administrador de TSF obtiene este valor de la aplicación mediante una llamada a [ITextStoreACP:: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) o [ITextStoreAnchor:: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview). El administrador de TSF usa este valor para identificar la vista cuando se llama a varios métodos [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) o [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                       |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                             |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITextStoreACP**](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[**ITextStoreACP:: GetActiveView**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview)
</dt> <dt>

[**ITextStoreAnchor::GetActiveView**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)
</dt> </dl>

 

 





