---
description: 'Más información sobre: JetPrereadKeys (Función)'
title: JetPrereadKeys (Función)
TOCTitle: JetPrereadKeys Function
ms:assetid: fc2f46bc-1f81-4af2-aa63-9757e819efc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294143(v=EXCHG.10)
ms:contentKeyID: 32765757
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrereadKeys
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24547a7970270943546e5fcfbc026ff24be144b0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986648"
---
# <a name="jetprereadkeys-function"></a>JetPrereadKeys (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetprereadkeys-function"></a>JetPrereadKeys (Función)

La **función JetPrereadKeys** lee los valores de clave para mejorar el rendimiento de la limpieza del almacén de versiones.

**Windows 7: la función PrereadKeys** se introdujo en Windows 7.

```cpp
    JET_ERR JET_API JetPrereadKeys(
      __in JET_SESID sesid,
      __in JET_TABLEID tableid,
      __in_ecount(ckeys) const void ** rgpvKeys,
      __in_ecount(ckeys) const unsigned long * rgcbKeys,
      __in long ckeys,
      __out_opt long * pckeysPreread,
      __in JET_GRBIT grbit
     );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*tableid*

Cursor que se va a usar para esta llamada.

*rgpvKeys*

Matriz de punteros a claves. Las claves se pueden crear [con JetMakeKey](./jetmakekey-function.md) o recuperarse [con JetGetBookmark.](./jetgetbookmark-function.md) Las claves deben ordenarse en orden ascendente o descendente, en función del grbit pasado. Las claves se pueden ordenar con memcmp.

*rgcbKeys*

Matriz de longitudes de clave. rgpvKeys \[ n debe apuntar a una clave de longitud \] rgcbKeys \[ n\]

*ckeys*

Número de claves. rgpvKeys y rgcbKeys deben apuntar a una matriz con al menos elementos ckeys.

*pckeysPreread*

Devuelve el número de claves para las que se emitieron las lecturas previas. Este parámetro puede ser NULL.

*grbit*

Debe ser JET_bitPrereadForward o JET_bitPrereadBackward. Si grbit es JET_bitPrereadForward, las claves deben ordenarse en orden ascendente. Si grbit es JET_bitPrereadBackward, las claves deben ordenarse en orden descendente.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).

Se pueden devolver varios errores de E/S junto con estos errores de uso de api:


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errInvalidGrbit</p> | <p>Grbit no era JET_bitPrereadForward ni JET_bitPrereadBackward.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Se ha pasado un tamaño de clave incorrecto. Las claves no pueden ser 0 ni más largas que la longitud máxima de clave de la tabla.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Se ha pasado un parámetro no válido. Esto puede deberse a un valor NULL para un parámetro necesario o puede indicar que la matriz de claves no está ordenada correctamente.</p> | 



**JetPrereadKeys** recorre las páginas internas del árbol b para determinar qué páginas hoja contienen las claves especificadas por rgpvKeys/rgcbKeys. La lista de páginas hoja se ordena y, a continuación, se emiten lecturas previas para los intervalos de páginas. El número de páginas que se pueden leer previamente es limitado, por lo que es posible que no todas las claves se puedan leer previamente. En ese caso, el número de claves que realmente se han leído previamente se devuelve en pckeysPreread.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows 7.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 R2.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 

