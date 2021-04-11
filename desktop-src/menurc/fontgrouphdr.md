---
title: Estructura FONTGROUPHDR
description: Contiene la información necesaria para que una aplicación tenga acceso a una fuente específica. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- Menús de la estructura FONTGROUPHDR y otros recursos
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d67d9ecfa451970422f21d05817f26170a9c8eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274540"
---
# <a name="fontgrouphdr-structure"></a>Estructura FONTGROUPHDR

Contiene la información necesaria para que una aplicación tenga acceso a una fuente específica. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.

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

Tipo: **Word**

</dd> <dd>

El número de fuentes individuales asociadas a este recurso.

</dd> <dt>

**DE**
</dt> <dd>

Tipo: **[ **dirente**](direntry.md)**

</dd> <dd>

Estructura que contiene un identificador ordinal único para cada fuente del recurso. El miembro **de** es un marcador de posición para la matriz de longitud variable de estructuras de [**direntary**](direntry.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura **FONTGROUPHDR** sigue los datos de las fuentes individuales en. Archivo res. El compilador de recursos agrega automáticamente la estructura **FONTGROUPHDR** , generalmente como la última entrada del archivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**ARRENDAMIENTO**](direntry.md)
</dt> <dt>

[**FONTDIRENTRY**](fontdirentry.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





