---
description: 'Más información sobre: JET_UNICODEINDEX estructura'
title: JET_UNICODEINDEX estructura
TOCTitle: JET_UNICODEINDEX Structure
ms:assetid: d0b8ef74-850e-4e21-9f71-b56ec472aa0f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294097(v=EXCHG.10)
ms:contentKeyID: 32765712
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb2779c75d525e45e9140d8f70665a09fe202b21
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988118"
---
# <a name="jet_unicodeindex-structure"></a>JET_UNICODEINDEX estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_unicodeindex-structure"></a>JET_UNICODEINDEX estructura

La **JET_UNICODEINDEX** personaliza cómo se normalizan los datos Unicode cuando se crea un índice sobre una columna Unicode.

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a>Miembros

**lcid**

Identificador de configuración regional que se usará al normalizar los datos. Se puede usar cualquier configuración regional siempre que se haya instalado el paquete de idioma adecuado en la máquina. La única excepción es que la configuración regional de idioma neutro (LCID de cero) no es posible.

**dwMapFlags**

Estas marcas se pasan a [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) cuando los datos Unicode se normalizan en una clave, lo que permite que las marcas definidas por el usuario invalide el valor predeterminado.

**Windows 2000:** los dos únicos valores legales de **dwFlags** son:

  - ( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE )

<!-- end list -->

  - ( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH )

**dwMapFlags** tiene las restricciones siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>LCMAP_SORTKEY</p> | <p>Mandatory.</p> | 
| <p>LCMAP_BYTEREV</p> | <p>Opcional.</p> | 
| <p>NORM_IGNORECASE</p> | <p>Opcional.</p> | 
| <p>NORM_IGNORENONSPACE</p> | <p>Opcional.</p> | 
| <p>NORM_IGNORESYMBOLS</p> | <p>Opcional.</p> | 
| <p>NORM_IGNOREKANATYPE</p> | <p>Opcional.</p> | 
| <p>NORM_IGNOREWIDTH</p> | <p>Opcional.</p> | 
| <p>SORT_STRINGSORT</p> | <p>Opcional.</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)
