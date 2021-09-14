---
title: WINBIO_BDB_ANSI_381_RECORD estructura (Tipos de \_ Winbio.h)
description: Contiene información sobre una sola huella digital o una muestra de manos de un usuario final.
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- WINBIO_BDB_ANSI_381_RECORD estructura Windows API de marco biométrico
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_RECORD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30af31d88349dbe02066f231cdff21293aebe90
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160789"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a>Estructura DE REGISTROS \_ \_ ANSI \_ 381 \_ de WINBIO BDB

La **estructura WINBIO \_ BDB ANSI \_ \_ 381 \_ RECORD** contiene información sobre una sola huella digital o una muestra de la mano de un usuario final. Se incluye una colección de estas estructuras en cada [**estructura WINBIO \_ BDB \_ ANSI \_ 381 \_ HEADER.**](winbio-bdb-ansi-381-header.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_BDB_ANSI_381_RECORD {
  ULONG                    BlockLength;
  USHORT                   HorizontalLineLength;
  USHORT                   VerticalLineLength;
  WINBIO_BIOMETRIC_SUBTYPE Position;
  UCHAR                    CountOfViews;
  UCHAR                    ViewNumber;
  UCHAR                    ImageQuality;
  UCHAR                    ImpressionType;
  UCHAR                    Reserved;
} WINBIO_BDB_ANSI_381_RECORD;
```



## <a name="members"></a>Members

<dl> <dt>

**BlockLength**
</dt> <dd>

Contiene el número de bytes de esta estructura más el número de bytes de datos de imagen de ejemplo.

</dd> <dt>

**HorizontalLineLength**
</dt> <dd>

Especifica el número de píxeles en una línea horizontal del ejemplo.

</dd> <dt>

**VerticalLineLength**
</dt> <dd>

Especifica el número de píxeles en una línea vertical del ejemplo.

</dd> <dt>

**Position**
</dt> <dd>

Valor **DE \_ \_ SUBTYPE BIOMETRIC de WINBIO** que especifica el dedo o la mano usados para generar la muestra biométrica. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

**CountOfViews**
</dt> <dd>

Debe establecerse en uno (1);

</dd> <dt>

**ViewNumber**
</dt> <dd>

Debe establecerse en uno (1);

</dd> <dt>

**ImageQuality**
</dt> <dd>

Reservado. Debe ser 254 (0xFE).

</dd> <dt>

**ImpressionType**
</dt> <dd>

Reservado.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado. Debe establecerse en cero (0).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El *miembro* Position especifica el área de la mano o la mano que se usa para crear la muestra biométrica. El Windows Biometric Framework (WBF) actualmente solo admite la captura de huellas digitales y usa las siguientes constantes para representar información de posición.

-   WINBIO \_ ANSI \_ 381 \_ POS \_ UNKNOWN
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ THUMB
-   DEDO ÍNDICE RH DE WINBIO \_ ANSI \_ 381 \_ POS \_ \_ \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ MIDDLE \_ FINGER
-   DEDO ANILLO DE WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ INDEX \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ MIDDLE \_ FINGER
-   DEDO ANILLO DE LH DE WINBIO \_ ANSI \_ 381 \_ POS \_ \_ \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ FOUR \_ FINGERS
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ FOUR \_ FINGERS
-   WINBIO \_ ANSI \_ 381 \_ POS \_ TWO \_ THUMBS

> [!IMPORTANT]
>
> No intente validar el valor proporcionado para el *valor Position.* El Windows Biometrics Service validará el valor proporcionado antes de pasarlo a la implementación. Si el valor es **WINBIO \_ SUBTYPE \_ NO INFORMATION \_ o** **WINBIO \_ SUBTYPE \_ ANY**, valide cuando corresponda.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> </dl>

 

 





