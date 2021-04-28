---
description: 'MF_MT_FSSourceTypeDecoded atributo : especifica si un descodificador puede usar marcas de tiempo de descodificación (DTS) al establecer marcas de tiempo.'
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3799c11e3b921427ff4a3b05aa3d7f47e297ba14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093093"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>Atributo \_ MF MT \_ FSSourceTypeDecoded

Especifica que un tipo de medio se descodifica automáticamente.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**


## <a name="remarks"></a>Comentarios
Un tipo de medio se marca como un atributo para indicar que esto no existe en el origen físico y se sintetiza mediante la canalización. Un valor de 1 (TRUE) indica que el tipo de medio está sintetizado. Un valor de 0 (FALSE) o el valor que no está presente indica que no lo está.

En la versión actual, este atributo debe especificarse con el siguiente valor GUID en lugar de la MD_MT_FSSourceTypeDecoded constante:

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8 aplicaciones \[ de escritorio \| para aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Aplicaciones de escritorio de Windows Server 2012 \[ \| aplicaciones para UWP\]<br/>                        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




