---
title: MPVERSION_INFO estructura (MpClient. h)
description: Información de versión de los componentes del administrador de protección contra malware de.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- MPVERSION_INFO estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPVERSION_INFO características de entorno heredado de Windows
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
ms.openlocfilehash: f30153c427b880600a3d8aeb3c411a8679cd64b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359807"
---
# <a name="mpversion_info-structure"></a>Estructura de información de MPVERSION \_

Información de versión de los componentes del administrador de protección contra malware de.

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

Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versión del producto.

</dd> <dt>

**Servicio**
</dt> <dd>

Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versión del componente de servicio.

</dd> <dt>

**FileSystemFilter**
</dt> <dd>

Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versión del componente de filtro del sistema de archivos.

</dd> <dt>

**Engine**
</dt> <dd>

Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versión del componente del motor.

</dd> <dt>

**Assignature**
</dt> <dd>

Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versión del componente de firma de AntiSpyware.

</dd> <dt>

**AVSignature**
</dt> <dd>

Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versión del componente de firma antivirus.

</dd> <dt>

**NISEngine**
</dt> <dd>

Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versión del motor NIS.

</dd> <dt>

**NISSignature**
</dt> <dd>

Tipo: **[ **\_ versión de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versión del componente de firma de firma NIS.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **[**MPCOMPONENT \_ versión**](mpcomponent-version.md) \[ 4\]**

</dd> <dd>

Campos reservados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**versión de MPCOMPONENT \_**](mpcomponent-version.md)
</dt> </dl>

 

 





