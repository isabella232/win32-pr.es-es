---
title: ClosedCaption.SAMILangCount
description: La propiedad SAMILangCount recupera el número de idiomas admitidos por el archivo SAMI actual.
ms.assetid: ad2e776a-b430-46ee-9705-18d279e8715e
keywords:
- ClosedCaption.SAMILangCount Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILangCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfcf9562639fe425915c9e0720cf7cf4cd75c5a56df66d8e6e2f31408145601
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118840314"
---
# <a name="closedcaptionsamilangcount"></a>ClosedCaption.SAMILangCount

La **propiedad SAMILangCount** recupera el número de idiomas admitidos por el archivo SAMI actual.

``` syntax
player.closedCaption.SAMILangCount
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Comentarios

Este método no se puede usar hasta que se abra un archivo multimedia digital *(Reproductor de*.**openState** es igual a 13).

**Reproductor de Windows Media 10 Mobile:** Esta propiedad siempre devuelve 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption (objeto)**](closedcaption-object.md)
</dt> <dt>

[**ClosedCaption.getSAMILangName**](closedcaption-getsamilangname.md)
</dt> <dt>

[**ClosedCaption.SAMILang**](closedcaption-samilang.md)
</dt> </dl>

 

 





