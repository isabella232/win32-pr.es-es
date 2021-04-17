---
description: Especifica si un descodificador puede usar marcas de tiempo de descodificación (DTS) al establecer las marcas de tiempo.
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ad80b0b7b29677ed0bee2f86a2c12c56c08441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720764"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>\_Atributo MF MT \_ FSSourceTypeDecoded

Especifica que un tipo de medio se descodifica automáticamente.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**


## <a name="remarks"></a>Observaciones
Un tipo de medio se marca como atributo para indicar que no existe en el origen físico y está sintetizado por la canalización. Un valor de 1 (TRUE) indica que el tipo de medio es sintetizado. Un valor de 0 (FALSE) o el valor que no está presente indica que no lo está.

En la versión actual, este atributo se debe especificar utilizando el siguiente valor de GUID en lugar de la constante MD_MT_FSSourceTypeDecoded:

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




