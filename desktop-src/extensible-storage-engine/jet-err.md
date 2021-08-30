---
description: 'Más información sobre: JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 684191f574b5c21b61b780a99e8614e801a95bfd
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982588"
---
# <a name="jet_err"></a>JET_ERR


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_err"></a>JET_ERR

El **JET_ERR** tipo de datos contiene un [código de error extensible Storage engine](./extensible-storage-engine-error-codes.md).

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a>Tipo de datos

JET_ERR

Un valor cero (correspondiente a JET_errSuccess) indica que la llamada se ha hecho correctamente. Un valor positivo advierte de una condición no grave que se produjo durante una llamada correcta de otro modo. Un valor negativo indica que se ha fallado la llamada.

### <a name="remarks"></a>Observaciones

Para obtener información sobre cómo devolver errores como HULT, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md). Para obtener información sobre las marcas para configurar la base de datos para controlar errores, vea [Parámetros de control de errores](./error-handling-parameters.md).

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[Errores extensibles Storage motor de instalación](./extensible-storage-engine-errors.md)  
[Códigos de error Storage motor extensibles](./extensible-storage-engine-error-codes.md)  
[Parámetros de control de errores](./error-handling-parameters.md)
