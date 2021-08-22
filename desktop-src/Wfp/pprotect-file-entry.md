---
description: Estructura utilizada por la función SfcGetFiles.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: PPROTECT_FILE_ENTRY estructura (Sfcfiles.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PPROTECT_FILE_ENTRY
api_type:
- HeaderDef
api_location:
- Sfcfiles.h
ms.openlocfilehash: c9070290170febf08e532b071812600fb0ef8755302a4bd1603858659196d0c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053203"
---
# <a name="pprotect_file_entry-structure"></a>Estructura PPROTECT \_ FILE \_ ENTRY

\[Esta estructura está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. La compatibilidad con esta estructura se quitó en Windows Vista y Windows Server 2008. En su lugar, use las funciones admitidas [enumeradas en Funciones de WRP.](wfp-functions.md)\]

Estructura utilizada por la [**función SfcGetFiles.**](sfcgetfiles.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PPROTECT_FILE_ENTRY {
  PWSTR SourceFileName;
  PWSTR FileName;
  PWSTR InfName;
} PPROTECT_FILE_ENTRY, *PPPROTECT_FILE_ENTRY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**SourceFileName**
</dt> <dd>

Puntero a un valor de cadena que contiene el nombre de archivo del archivo de origen. Será NULL **si no se** cambia el nombre del archivo durante la instalación.

</dd> <dt>

**FileName**
</dt> <dd>

Puntero al valor de cadena que contiene el nombre de archivo de destino más la ruta de acceso completa al archivo.

</dd> <dt>

**InfName**
</dt> <dd>

Puntero al valor de cadena que contiene el nombre de archivo del archivo INF que proporciona información de diseño. Este parámetro puede ser **NULL** cuando se usa el diseño predeterminado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                 |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                        |
| Header<br/>                   | <dl> <dt>Sfcfiles.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SfcGetFiles**](sfcgetfiles.md)
</dt> </dl>

 

 




