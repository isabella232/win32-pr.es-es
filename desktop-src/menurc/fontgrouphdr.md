---
title: FontGROUPHDR (estructura)
description: Contiene la información necesaria para que una aplicación acceda a una fuente específica. La definición de estructura que se proporciona aquí es solo para una explicación; no está presente en ningún archivo de encabezado estándar.
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- Menús de estructura FONTGROUPHDR y otros recursos
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51b307b7f5798a57e344096fe46227edf97babbf3547c4c851d71fd8ecdc28da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734483"
---
# <a name="fontgrouphdr-structure"></a>FontGROUPHDR (estructura)

Contiene la información necesaria para que una aplicación acceda a una fuente específica. La definición de estructura que se proporciona aquí es solo para una explicación; no está presente en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD     NumberOfFonts;
  DIRENTRY DE;
} FONTGROUPHDR;
```



## <a name="members"></a>Miembros

<dl> <dt>

**NumberOfFonts**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Número de fuentes individuales asociadas a este recurso.

</dd> <dt>

**DE**
</dt> <dd>

Tipo: **[ **DIRENTRY**](direntry.md)**

</dd> <dd>

Estructura que contiene un identificador ordinal único para cada fuente del recurso. El **miembro DE** es un marcador de posición para la matriz de longitud variable de estructuras [**DIRENTRY.**](direntry.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura FONTGROUPHDR** sigue los datos de las fuentes individuales de . Archivo Res. El compilador de recursos agrega automáticamente la **estructura FONTGROUPHDR,** generalmente como la última entrada del archivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DIRENTRY**](direntry.md)
</dt> <dt>

[**FONTDIRENTRY**](fontdirentry.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





