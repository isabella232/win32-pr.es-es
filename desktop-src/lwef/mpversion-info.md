---
title: MPVERSION_INFO estructura (MpClient.h)
description: Información de versión de los componentes del administrador de protección contra malware.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- MPVERSION_INFO estructura heredada de Windows environment
- PMPVERSION_INFO puntero de estructura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPVERSION_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50a89b03b8b310416f9b0b496c055f732f4e83859bb7eba50b7891abebc27d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608705"
---
# <a name="mpversion_info-structure"></a>Estructura DE \_ INFORMACIÓN DE MPVERSION

Información de versión de los componentes del administrador de protección contra malware.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPVERSION_INFO {
  MPCOMPONENT_VERSION Product;
  MPCOMPONENT_VERSION Service;
  MPCOMPONENT_VERSION FileSystemFilter;
  MPCOMPONENT_VERSION Engine;
  MPCOMPONENT_VERSION ASSignature;
  MPCOMPONENT_VERSION AVSignature;
  MPCOMPONENT_VERSION NISEngine;
  MPCOMPONENT_VERSION NISSignature;
  MPCOMPONENT_VERSION Reserved[4];
} MPVERSION_INFO, *PMPVERSION_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Producto**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versión del producto.

</dd> <dt>

**Servicio**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versión del componente de servicio.

</dd> <dt>

**FileSystemFilter**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versión del componente de filtro del sistema de archivos.

</dd> <dt>

**Engine**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versión del componente del motor.

</dd> <dt>

**ASSignature**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versión del componente de firma antispyware.

</dd> <dt>

**AVSignature**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versión del componente de firma antivirus.

</dd> <dt>

**NISEngine**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versión del motor de NIS.

</dd> <dt>

**NISSignature**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ VERSION**](mpcomponent-version.md)**

</dd> <dd>

Versión del componente de firma de firma de NIS.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **[**MPCOMPONENT \_ VERSIÓN**](mpcomponent-version.md) \[ 4\]**

</dd> <dd>

Campos reservados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**VERSIÓN DE \_ MPCOMPONENT**](mpcomponent-version.md)
</dt> </dl>

 

 





