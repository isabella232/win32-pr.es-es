---
description: 'MF_MT_FSSourceTypeDecoded atributo : especifica si un descodificador puede usar marcas de tiempo de descodificación (DTS) al establecer marcas de tiempo.'
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae25fce343d0c24f7b0a79e2623e7c3e2d0f9272b2f95a825860860ff6f88c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113765"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>Atributo \_ \_ FSSourceTypeDecoded de MF MT

Especifica que un tipo de medio se descodifica automáticamente.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**


## <a name="remarks"></a>Comentarios
Un tipo de medio se marca como un atributo para indicar que esto no existe en el origen físico y se sintetiza mediante la canalización. Un valor de 1 (TRUE) indica que se sintetiza el tipo de medio. Un valor de 0 (FALSE) o el valor que no está presente indica que no lo está.

En la versión actual, este atributo debe especificarse con el siguiente valor GUID en lugar de la MD_MT_FSSourceTypeDecoded constante:

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




