---
description: La estructura CAPTUREFILTER contiene datos de filtro de captura.
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: Estructura CAPTUREFILTER (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667742"
---
# <a name="capturefilter-structure"></a>Estructura CAPTUREFILTER

La estructura **CAPTUREFILTER** contiene datos de filtro de captura.

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



## <a name="members"></a>Miembros

<dl> <dt>

**FilterFlags**
</dt> <dd>

Marcas que describen el contenido del filtro de captura.



| Value                                                                                                                                                                                                                                                                                                   | Significado                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <dt>**CAPTUREFILTER \_ \_Las marcas incluyen \_ todos los \_**</dt> <dt>0x0001</dt> de SAP </dl>       | Incluye todos los SAP como fotogramas aceptables.<br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <dt>**CAPTUREFILTER \_ \_Las marcas incluyen \_ All \_ ETYPE**</dt> <dt>0x0002</dt> </dl> | Incluya todos los ETYPE como fotogramas aceptables.<br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <dt>**CAPTUREFILTER \_ MARCAS \_ \_ solo locales**</dt> de <dt>0x0008</dt> </dl>                          | Sin modo P<br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <dt>**CAPTUREFILTER \_ Las marcas \_ mantienen 0x0020 \_ sin procesar**</dt> <dt></dt> </dl>                                | Mantenga fotogramas de SMT y tokens de MAC en anillo.<br/>      |



 

</dd> <dt>

**lpSapTable**
</dt> <dd>

Puntero a una matriz de valores de SAP. Este miembro indica los valores de SAP que son válidos para pasar al controlador. Si \_ las marcas \_ de CAPTUREFILTER incluyen \_ \_ la configuración de todos los SAP, se convierte en una lista de excepciones (incluye todos los SAP excepto estos).

</dd> <dt>

**lpEtypeTable**
</dt> <dd>

Puntero a una matriz de valores ETYPE. Indica los valores ETYPE que son válidos para pasar al controlador. Si \_ las marcas \_ de CAPTUREFILTER incluyen \_ \_ la configuración de ETYPE, se convierte en una lista de excepciones (incluye todos los ETYPE excepto estos).

</dd> <dt>

**nSaps**
</dt> <dd>

Número de SAP en la tabla de SAP.

</dd> <dt>

**nEtypes**
</dt> <dd>

Número de ETYPE en la tabla ETYPE.

</dd> <dt>

**AddressTable**
</dt> <dd>

Nombre de la tabla de direcciones.

</dd> <dt>

**FilterExpression**
</dt> <dd>

Una estructura de expresión. Contiene la parte de la coincidencia de patrones del filtro de captura.

</dd> <dt>

**Desencadenador**
</dt> <dd>

Reservado.

</dd> <dt>

**nFrameBytesToCopy**
</dt> <dd>

Si este miembro no es 0, especifica el número de bytes que se deben mantener de cada fotograma recibido. Si es 0, mantenga todo el marco.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La combinación de marcas, valores y expresiones determina qué fotogramas pasará el controlador que utiliza estos datos de estructura. Para obtener más información sobre la implementación de una estructura **CAPTUREFILTER** , consulte [filtros de captura](capture-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ADDRESSTABLE](addresstable.md)
</dt> <dt>

[ADDRESSPAIR](addresspair.md)
</dt> <dt>

[Expresiones](expression.md)
</dt> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




