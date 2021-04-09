---
description: Identifica el nombre del proveedor de inicio de la SIM o el dispositivo especificados.
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
ms.openlocfilehash: 3d0af51e4873915838f2d55f683d07e9098aad3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809619"
---
# <a name="homeprovidername-mbnprofile-element"></a>Elemento HomeProviderName (MBNProfile)

El elemento **HomeProviderName (MBNProfile)** identifica el nombre del proveedor de inicio de la SIM o el dispositivo especificados.

Este elemento es opcional y lo establece el servicio de banda ancha móvil para uso interno. Una aplicación no debe establecer este campo al crear o actualizar un perfil.

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

El elemento **HomeProviderName** se define mediante el elemento [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
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

 

 




