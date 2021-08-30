---
description: Contiene el atributo de información estándar. Este atributo está presente en cada registro de archivo base y debe ser residentes.
ms.assetid: 8e668309-2722-4115-923d-bf0aa78d24f1
title: STANDARD_INFORMATION estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STANDARD_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: d0ddba05eee5d822020cfbb2e4b30976bb3c7570e1613f457ee3fd373494e0da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984065"
---
# <a name="standard_information-structure"></a>Estructura \_ STANDARD INFORMATION

\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]

Contiene el atributo de información estándar. Este atributo está presente en cada registro de archivo base y debe ser residentes.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _STANDARD_INFORMATION {
  UCHAR Reserved[0x30];
  ULONG OwnerId;
  ULONG SecurityId;
} STANDARD_INFORMATION, *PSTANDARD_INFORMATION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**OwnerId**
</dt> <dd>

Identificador del propietario del archivo, del índice de seguridad.

</dd> <dt>

**SecurityId**
</dt> <dd>

Identificador de seguridad del archivo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.

Esta definición de estructura solo es válida para la versión principal 3 y la versión secundaria 0 o 1, como notifica [**FSCTL \_ GET NTFS VOLUME \_ \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tabla de archivos maestros](master-file-table.md)
</dt> </dl>

 

 
