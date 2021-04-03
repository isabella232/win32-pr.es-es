---
description: Contiene el atributo de información estándar. Este atributo está presente en cada registro de archivo base y debe ser residente.
ms.assetid: 8e668309-2722-4115-923d-bf0aa78d24f1
title: Estructura de STANDARD_INFORMATION
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
ms.openlocfilehash: 4927553ac593475f8659932468227362ae19fe59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080085"
---
# <a name="standard_information-structure"></a>\_Estructura de información estándar

\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]

Contiene el atributo de información estándar. Este atributo está presente en cada registro de archivo base y debe ser residente.

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

El identificador de seguridad del archivo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.

Esta definición de estructura solo es válida para la versión 3 principal y la secundaria 0 o 1, tal y como lo ha indicado el [**FSCTL \_ obtener \_ \_ \_ datos del volumen NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tabla de archivos maestros](master-file-table.md)
</dt> </dl>

 

 
