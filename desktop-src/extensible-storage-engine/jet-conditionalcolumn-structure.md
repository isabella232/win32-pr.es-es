---
description: 'Más información sobre: JET_CONDITIONALCOLUMN estructura'
title: JET_CONDITIONALCOLUMN estructura
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
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
ms.openlocfilehash: d7ca03c8c340c9c0b81ec46d0809f50a19e4d2f2
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122981968"
---
# <a name="jet_conditionalcolumn-structure"></a>JET_CONDITIONALCOLUMN estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_conditionalcolumn-structure"></a>JET_CONDITIONALCOLUMN estructura

La **JET_CONDITIONALCOLUMN** estructura define cómo se realiza la indexación condicional para un índice determinado. Un índice condicional contiene una entrada de índice solo para las filas que coinciden con la condición especificada. Sin embargo, la columna condicional no forma parte de la clave del índice, solo controla la presencia de la entrada de índice.

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a>Miembros

**cbStruct**

Este campo debe inicializarse en sizeof( JET_CONDITIONALCOLUMN ), en bytes.

**szColumnName**

Nombre de la columna que contiene los datos en los que el motor de base de datos indexa condicionalmente la fila.

**grbit** Grupo de bits que proporciona las opciones para el índice condicional. Pasar cero o valores or **lógicos- OR** ed no es válido para **JET_CONDITIONALCOLUMN**. El campo de bits debe ser exactamente uno de los siguientes:


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitIndexColumnMustBeNull</p> | <p>La columna especificada por el <em>parámetro szColumnName</em> debe ser NULL para que una entrada de índice de una fila determinada aparezca en este índice.</p> | 
| <p>JET_bitIndexColumnMustBeNonNull</p> | <p>La columna especificada por el parámetro <em>szColumnName</em> debe ser no NULL para una entrada de índice con el fin de que una fila determinada aparezca en este índice.</p> | 



### <a name="remarks"></a>Observaciones

Un índice condicional contiene una entrada de índice solo para las filas que coinciden con la condición especificada. Por ejemplo, una columna podría denominarse "Marked" y, cuando se marca una fila, la columna se establece en un valor distinto de NULL. Un JET_bitIndexColumnMustBeNonNull condicional en esta columna mostrará todas las filas marcadas y un JET_bitIndexColumnMustBeNull condicional mostrará las filas que no están marcadas. También es una manera cómoda de realizar una eliminación de marcas y un índice de recolección de elementos no utilizados.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) <strong>y JET_CONDITIONALCOLUMN_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte también

[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)
