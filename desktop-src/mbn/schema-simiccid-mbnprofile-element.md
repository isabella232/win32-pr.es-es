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
ms.openlocfilehash: f566253ad3e86b4f7ee7317cf125d9e649034847
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252530"
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
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/> |
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

 

 




