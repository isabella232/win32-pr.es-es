---
description: Estructura utilizada por la función SfcGetFiles.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: PPROTECT_FILE_ENTRY estructura (sfcfiles. h)
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
ms.openlocfilehash: 98cda570a3677560d51800d58822d93a942847c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706395"
---
# <a name="pprotect_file_entry-structure"></a>PPROTECT \_ estructura de entrada de archivo \_

\[Esta estructura está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. Se ha quitado la compatibilidad con esta estructura en Windows Vista y Windows Server 2008. En su lugar, use las funciones admitidas que se enumeran en [las funciones de WRP](wfp-functions.md) .\]

Estructura utilizada por la función [**SfcGetFiles**](sfcgetfiles.md) .

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

Puntero a un valor de cadena que contiene el nombre de archivo del archivo de código fuente. Será **null** si no se cambia el nombre del archivo durante la instalación.

</dd> <dt>

**FileName**
</dt> <dd>

Puntero al valor de cadena que contiene el nombre de archivo de destino más la ruta de acceso completa al archivo.

</dd> <dt>

**InfName**
</dt> <dd>

Puntero al valor de cadena que contiene el nombre del archivo INF que proporciona información de diseño. Este parámetro puede ser **null** cuando se usa el diseño predeterminado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                 |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Sfcfiles. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SfcGetFiles**](sfcgetfiles.md)
</dt> </dl>

 

 




