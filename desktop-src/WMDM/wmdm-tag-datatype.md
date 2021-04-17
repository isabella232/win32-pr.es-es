---
title: Enumeración WMDM_TAG_DATATYPE
description: El \_ tipo de enumeración de tipo de datos de la etiqueta WMDM \_ define un tipo de datos.
ms.assetid: 9c300814-5610-4e46-b441-e7f2fc78a47b
keywords:
- Enumeración WMDM_TAG_DATATYPE Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_TAG_DATATYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad04f0d220809f6bd13d8ae29cc36d52ff6e599
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698694"
---
# <a name="wmdm_tag_datatype-enumeration"></a>\_Enumeración de tipos de tipo de texto de etiqueta WMDM \_

El tipo de enumeración de **\_ \_ tipo** de datos de la etiqueta WMDM define un tipo de datos.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagWMDM_TAG_DATATYPE { 
  WMDM_TYPE_DWORD,
  WMDM_TYPE_STRING,
  WMDM_TYPE_BINARY,
  WMDM_TYPE_BOOL,
  WMDM_TYPE_QWORD,
  WMDM_TYPE_WORD,
  WMDM_TYPE_GUID,
  WMDM_TYPE_DATE
} WMDM_TAG_DATATYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM \_ tipo \_ DWORD**
</dt> <dd>

Especifica un valor **DWORD** de 4 bytes.

</dd> <dt>

<span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**\_cadena de tipo WMDM \_**
</dt> <dd>

Especifica una cadena Unicode terminada en null (2 bytes por carácter).

</dd> <dt>

<span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**tipo de WMDM \_ \_ binario**
</dt> <dd>

Especifica una matriz de bytes.

</dd> <dt>

<span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**WMDM \_ tipo \_ bool**
</dt> <dd>

Especifica un valor booleano de 4 bytes.

</dd> <dt>

<span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**tipo de WMDM de WMDM \_ \_**
</dt> <dd>

Especifica un valor **QWord** de 8 bytes.

</dd> <dt>

<span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM \_ Escriba \_ Word**
</dt> <dd>

Especifica un valor de **palabra** de 2 bytes.

</dd> <dt>

<span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**\_GUID de tipo de WMDM \_**
</dt> <dd>

Especifica un GUID de 128 bits (16 bytes).

</dd> <dt>

<span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**\_fecha de tipo de WMDM \_**
</dt> <dd>

Especifica una fecha.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





