---
description: Determina si la base de datos especificada es una de las bases de datos estándar (SysMain, apphelp, Drvmain o Msimain).
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: SdbIsStandardDatabase función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbIsStandardDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9e9e445162c2bfc171ccf975981876f81a8bb804
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080089"
---
# <a name="sdbisstandarddatabase-function"></a>SdbIsStandardDatabase función)

Determina si la base de datos especificada es una de las bases de datos estándar (SysMain, apphelp, Drvmain o Msimain).

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*GuidDB* \[ de\]
</dt> <dd>

GUID para la base de datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **true** si el GUID representa una base de datos estándar o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




