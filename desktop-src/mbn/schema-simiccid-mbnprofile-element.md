---
description: Identifica el número de identificación de SIM para dispositivos GSM.
ms.assetid: 980afba4-fc31-4da0-ba01-6eb8e3db0ac8
title: Elemento SimIccID (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SimIccID
api_type:
- Schema
ms.openlocfilehash: 8a6e4a20d93396337e2af0f0533486618dc707760f1ccd5c4f20f399cbdbf203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777865"
---
# <a name="simiccid-mbnprofile-element"></a>Elemento SimIccID (MBNProfile)

El **elemento SimIccID (MBNProfile)** identifica el número de identificación de SIM para dispositivos GSM.

Este elemento es opcional y lo establece el servicio banda ancha móvil para uso interno. Una aplicación no debe establecer este campo al crear o actualizar un perfil.

``` syntax
<xs:element name="SimIccID"
    type="simIccIDType"
 />
```

El **elemento SimIccID** se define mediante el [**elemento MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




