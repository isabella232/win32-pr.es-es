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
ms.openlocfilehash: 01c061330db3e97989e0700452fd4a205488a9fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906964"
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

Tipo de atributo. Vea [tipos de etiqueta](tag-types.md).

</dd> <dt>

**dwFlags**
</dt> <dd>

Marcas para este atributo.



| Value                                                                                                                                                                                                                                           | Significado                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <dt>**Atributo \_ de DISPONIBLE**</dt> <dt>0x00000001</dt> </dl> | El atributo está disponible.<br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <dt>**Atributo \_ de ERROR**</dt> <dt>0x00000002</dt> </dl>          | Error en la llamada porque el atributo no está disponible.<br/> |



 

</dd> <dt>

**ullAttr**
</dt> <dd>

Un valor **QWord** (si el tipo de etiqueta es el **tipo de etiqueta \_ \_ QWord**).

</dd> <dt>

**dwAttr**
</dt> <dd>

Valor **DWORD** (si el tipo de etiqueta es **el \_ tipo \_ de etiqueta DWORD**).

</dd> <dt>

**lpAttr**
</dt> <dd>

Un puntero a una cadena (si el tipo de etiqueta es el **tipo de etiqueta \_ \_ STRINGREF**).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




