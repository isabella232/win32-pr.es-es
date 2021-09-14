---
description: La estructura CAPTUREFILTER contiene datos de filtro de captura.
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: Estructura CAPTUREFILTER (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILTER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 129575ba401aed0e78f52695a49139f4143c9c87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253917"
---
# <a name="capturefilter-structure"></a>Estructura CAPTUREFILTER

La **estructura CAPTUREFILTER** contiene datos de filtro de captura.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _CAPTUREFILTER {
  DWORD          FilterFlags;
  LPBYTE         lpSapTable;
  LPWORD         lpEtypeTable;
  WORD           nSaps;
  WORD           nEtypes;
  LPADDRESSTABLE AddressTable;
  EXPRESSION     FilterExpression;
  TRIGGER        Trigger;
  DWORD          nFrameBytesToCopy;
  RESERVED       Reserved;
} CAPTUREFILTER, *LPCAPTUREFILTER;
```



## <a name="members"></a>Members

<dl> <dt>

**FilterFlags**
</dt> <dd>

Marcas que describen el contenido del filtro de captura.



| Value                                                                                                                                                                                                                                                                                                   | Significado                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <dt>**CAPTUREFILTER \_ LAS MARCAS \_ INCLUYEN \_ TODAS las \_ 0x0001**</dt> <dt></dt> </dl>       | Incluye todas las SAP como fotogramas aceptables.<br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <dt>**CAPTUREFILTER \_ LAS MARCAS \_ INCLUYEN \_ TODOS LOS \_ ETYPES**</dt> <dt>0x0002</dt> </dl> | Incluya todos los Etypes como fotogramas aceptables.<br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <dt>**CAPTUREFILTER \_ MARCA SOLO \_ \_ LA CONFIGURACIÓN**</dt> <dt>0X0008</dt> </dl>                          | Sin modo P<br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <dt>**CAPTUREFILTER \_ FLAGS \_ KEEP \_ RAW**</dt> <dt>0x0020</dt> </dl>                                | Mantenga tramas MAC de anillo de token y SMT.<br/>      |



 

</dd> <dt>

**lpSapTable**
</dt> <dd>

Puntero a una matriz de valores de SAP. Este miembro indica los valores de SAP que son válidos para pasar al controlador. Si se establece CAPTUREFILTER FLAGS INCLUDE ALL SAPS, se convierte en una lista de excepciones (incluya todos \_ \_ los \_ \_ SAPS excepto estos).

</dd> <dt>

**lpEtypeTable**
</dt> <dd>

Puntero a una matriz de valores Etype. Esto indica los valores Etype que son válidos para pasar al controlador. Si se establece CAPTUREFILTER FLAGS INCLUDE ALL ETYPES, se convierte en una lista de excepciones (incluya todos \_ \_ los \_ \_ Etypes excepto estos).

</dd> <dt>

**nSaps**
</dt> <dd>

Número de SAP en la tabla de SAP.

</dd> <dt>

**nEtypes**
</dt> <dd>

Número de Etypes de la tabla Etype.

</dd> <dt>

**AddressTable**
</dt> <dd>

Nombre de la tabla de direcciones.

</dd> <dt>

**FilterExpression**
</dt> <dd>

Estructura EXPRESSION. Contiene la parte de coincidencia de patrón del filtro de captura.

</dd> <dt>

**Desencadenador**
</dt> <dd>

Reservado.

</dd> <dt>

**nFrameBytesToCopy**
</dt> <dd>

Si este miembro no es 0, especifica cuántos bytes se conservarán de cada fotograma recibido. Si es 0, mantenga todo el marco.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La combinación de marcas, valores y expresiones determina qué marcos pasará el controlador que usa estos datos de estructura. Para obtener más información sobre cómo implementar una **estructura CAPTUREFILTER,** vea [Filtros de captura](capture-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ADDRESSTABLE](addresstable.md)
</dt> <dt>

[ADDRESSPAIR](addresspair.md)
</dt> <dt>

[EXPRESIÓN](expression.md)
</dt> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




