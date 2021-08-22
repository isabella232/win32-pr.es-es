---
description: Identifica el nombre del proveedor principal para la SIM o el dispositivo especificados.
ms.assetid: 05d65091-5a1d-427a-8f51-1e1b9d189571
title: Elemento HomeProviderName (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HomeProviderName
api_type:
- Schema
ms.openlocfilehash: 1868be18dc7acf9d5146f987658feb006714fbcc3db35883007afd01c308609e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035833"
---
# <a name="homeprovidername-mbnprofile-element"></a>Elemento HomeProviderName (MBNProfile)

El **elemento HomeProviderName (MBNProfile)** identifica el nombre del proveedor home para la SIM o el dispositivo especificados.

Este elemento es opcional y lo establece el servicio banda ancha móvil para uso interno. Una aplicación no debe establecer este campo al crear o actualizar un perfil.

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

El elemento [**MBNProfile**](schema-mbnprofile-element.md) define el elemento **HomeProviderName.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 




