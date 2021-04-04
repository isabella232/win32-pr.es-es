---
description: 'Más información acerca de: estructura de JET_RSTINFO'
title: Estructura de JET_RSTINFO
TOCTitle: JET_RSTINFO Structure
ms:assetid: 2f144d68-dcd9-4d0d-9d9e-a7d2a5c350fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269216(v=EXCHG.10)
ms:contentKeyID: 32765519
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
ms.openlocfilehash: 3a776c84d89dfc97272c65bb0c0684faba814fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154020"
---
# <a name="jet_rstinfo-structure"></a>Estructura de JET_RSTINFO


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_rstinfo-structure"></a>Estructura de JET_RSTINFO

La estructura **JET_RSTINFO** contiene información sobre el control del proceso de recuperación, como la información de reubicación de la base de datos y la capacidad de controlar la detención de la recuperación.

**Windows Vista:** La estructura de **JET_RSTINFO** se introduce en Windows Vista.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_RSTMAP* rgrstmap;
      long crstmap;
      JET_LGPOS lgposStop;
      JET_LOGTIME logtimeStop;
      JET_PFNSTATUS pfnStatus;
    } JET_RSTINFO;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de la estructura.

**rgrstmap**

La estructura que describe la ruta de acceso antigua y nueva de una base de datos restaurada.

**crstmap**

Recuento de entradas de matriz en rgrstmap.

**lgposStop**

La posición del registro en la que detener la recuperación. No se realizará la operación de deshacer.

**logtimeStop**

Reservado para uso futuro.

**pfnStatus**

Función de estado para notificar el estado de recuperación.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JET_RSTINFO_W</strong> (Unicode) y <strong>JET_RSTINFO_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JetInit3](./jetinit3-function.md)
