---
title: Estructura de WINBIO_REGISTERED_FORMAT (Winbio \_ Types. h)
description: Especifica un formato de datos registrado como par propietario/formato.
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- Plataforma de biometría de Windows API de WINBIO_REGISTERED_FORMAT Structure
- PWINBIO_REGISTERED_FORMAT de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_REGISTERED_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f45293fe95627c7dfad4c9c51eb7fa74ad1738c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534192"
---
# <a name="winbio_registered_format-structure"></a>WINBIO \_ \_ estructura de formato registrada

La estructura de **\_ \_ formato registrada WINBIO** especifica un formato de datos registrado como par de propietario/formato.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_REGISTERED_FORMAT {
  USHORT Owner;
  USHORT Type;
} WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Propietario**
</dt> <dd>

Un valor de propietario asignado de IBIA (Asociación del sector biométrico internacional).

</dd> <dt>

**Tipo**
</dt> <dd>

Formato asignado al propietario.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Dado que Windows actualmente solo admite lectores de huellas digitales, se deben usar los valores siguientes en la estructura de **\_ \_ formato registrada WINBIO** .



| Constante                                    | Significado                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| WINBIO \_ \_ propietario de \_ formato ANSI 381 \_<br/> | Comité Internacional para el Comité técnico M1 (biométrico de estándares de tecnología de la información) (INCITS).<br/> |
| WINBIO \_ \_ tipo de \_ formato ANSI 381 \_<br/>  | Formato de intercambio de datos basado en imágenes de Finger ANSI INCITS 381.<br/>                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> <dt>

[**WINBIO \_ \_ constantes de \_ formato ANSI 381**](winbio-ansi-381-format-constants.md)
</dt> <dt>

[**\_Encabezado WINBIO BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[**WINBIO \_ \_ encabezado Bir**](winbio-bir-header.md)
</dt> </dl>

 

 





