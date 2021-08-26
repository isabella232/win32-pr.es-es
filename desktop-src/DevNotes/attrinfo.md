---
description: Contiene los datos de atributo de un archivo.
ms.assetid: f23f801c-826c-4269-bf96-0e01430484f4
title: Estructura ATTRINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 090f2ab58d8bf1eb4e379166086d31389b533712a3df23f987bba1331f990891
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103735"
---
# <a name="attrinfo-structure"></a>Estructura ATTRINFO

Contiene los datos de atributo de un archivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagATTRINFO {
  TAG   tAttrID;
  DWORD dwFlags;
  union {
    ULONGLONG ullAttr;
    DWORD     dwAttr;
    TCHAR     *lpAttr;
  };
} ATTRINFO, *PATTRINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**tAttrID**
</dt> <dd>

Tipo de atributo. Vea [Tipos DE ETIQUETA.](tag-types.md)

</dd> <dt>

**dwFlags**
</dt> <dd>

Marcas para este atributo.



| Value                                                                                                                                                                                                                                           | Significado                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <dt>**ATTRIBUTE \_ DISPONIBLE**</dt> <dt>0x00000001</dt> </dl> | El atributo está disponible.<br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <dt>**ATTRIBUTE \_ Error**</dt> <dt>0x00000002</dt> </dl>          | Error en la llamada porque el atributo no está disponible.<br/> |



 

</dd> <dt>

**ullAttr**
</dt> <dd>

Un **valor QWORD** (si el tipo de etiqueta es **TAG TYPE \_ \_ QWORD**).

</dd> <dt>

**dwAttr**
</dt> <dd>

Valor **DWORD** (si el tipo de etiqueta es **TAG TYPE \_ \_ DWORD).**

</dd> <dt>

**lpAttr**
</dt> <dd>

Puntero a una cadena (si el tipo de etiqueta es **TAG \_ TYPE \_ STRINGREF).**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




