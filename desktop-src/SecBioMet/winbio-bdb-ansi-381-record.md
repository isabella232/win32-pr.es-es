---
title: Estructura de WINBIO_BDB_ANSI_381_RECORD (Winbio \_ Types. h)
description: Contiene información sobre una sola huella digital o un ejemplo de Palm de un usuario final.
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- Plataforma de biometría de Windows API de WINBIO_BDB_ANSI_381_RECORD Structure
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421971"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a>\_Estructura de registro WINBIO BDB \_ ANSI \_ 381 \_

La estructura de **\_ registro WINBIO BDB \_ ANSI \_ 381 \_** contiene información sobre una sola huella digital o un ejemplo de Palm de un usuario final. Se incluye una colección de estas estructuras en cada estructura de [**\_ encabezado WINBIO BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-header.md) .

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



## <a name="members"></a>Miembros

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

Un valor de **\_ \_ subtipo biométrico WINBIO** que especifica el dedo o la palma utilizada para generar el ejemplo biométrico. Para obtener más información, vea la sección Comentarios.

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

El miembro *posición* especifica el área de la mano o la palma utilizada para crear el ejemplo biométrico. El Plataforma de biometría de Windows (WBF) actualmente solo admite la captura de huellas digitales y usa las siguientes constantes para representar la información de posición.

-   WINBIO \_ ANSI \_ 381 \_ pos \_ desconocido
-   \_Thumb WINBIO ANSI \_ 381 \_ pos \_ RH \_
-   \_Dedo de \_ \_ \_ \_ índice RH \_ de WINBIO ANSI 381 pos
-   \_Dedo central de WINBIO ANSI \_ 381 \_ pos \_ dcha \_ \_
-   \_Dedo de \_ \_ \_ \_ anillo RH \_ de WINBIO ANSI 381 pos
-   \_ \_ \_ \_ \_ Pequeño \_ dedo de WINBIO ANSI 381 pos
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Thumb
-   WINBIO \_ de \_ Índice de LH de pdv ANSI 381 \_ pos \_ \_ \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ central \_
-   WINBIO \_ el \_ \_ dedo de \_ anillo de LH ANSI 381 pos \_ \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Little \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ cuatro \_ dedos
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ cuatro \_ dedos
-   WINBIO \_ ANSI \_ 381 \_ pos \_ dos \_ Thumbs

> [!IMPORTANT]
>
> No intente validar el valor proporcionado para el valor de *posición* . El servicio biométrico de Windows validará el valor proporcionado antes de pasarlo a su implementación. Si el valor es **WINBIO \_ SubType \_ no \_ Information** o **WINBIO \_ SubType \_ any**, valide cuando sea necesario.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> </dl>

 

 





