---
title: WMDM_TAG_DATATYPE enumeración
description: El tipo de \_ enumeración DATATYPE DE WMDM TAG \_ define un tipo de datos.
ms.assetid: 9c300814-5610-4e46-b441-e7f2fc78a47b
keywords:
- WMDM_TAG_DATATYPE enumeración windows Media Administrador de dispositivos
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
ms.openlocfilehash: bd725e6d8a0e1baef8a6dfc98cb5d3056f5d67b2d7babd07c919692d96248881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862675"
---
# <a name="wmdm_tag_datatype-enumeration"></a>Enumeración \_ DATATYPE de WMDM TAG \_

El **tipo de \_ enumeración \_ DATATYPE DE WMDM TAG** define un tipo de datos.

## <a name="syntax"></a>Syntax


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

<span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**DWORD \_ DE TIPO \_ WMDM**
</dt> <dd>

Especifica un valor **DWORD** de 4 bytes.

</dd> <dt>

<span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**CADENA DE TIPO WMDM \_ \_**
</dt> <dd>

Especifica una cadena Unicode terminada en NULL (2 bytes por carácter).

</dd> <dt>

<span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**WMDM \_ TYPE \_ BINARY**
</dt> <dd>

Especifica una matriz de bytes.

</dd> <dt>

<span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**WMDM \_ TYPE \_ BOOL**
</dt> <dd>

Especifica un valor booleano de 4 bytes.

</dd> <dt>

<span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**TIPO DE WMDM \_ \_ QWORD**
</dt> <dd>

Especifica un valor **QWORD** de 8 bytes.

</dd> <dt>

<span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**PALABRA DE TIPO WMDM \_ \_**
</dt> <dd>

Especifica un valor WORD de 2 **bytes.**

</dd> <dt>

<span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**GUID DE \_ TIPO \_ WMDM**
</dt> <dd>

Especifica un GUID de 128 bits (16 bytes).

</dd> <dt>

<span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**FECHA DE TIPO \_ WMDM \_**
</dt> <dd>

Especifica una fecha.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





