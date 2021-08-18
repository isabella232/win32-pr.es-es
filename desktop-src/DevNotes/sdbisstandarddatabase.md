---
description: Determina si la base de datos especificada es una de las bases de datos estándar (Sysmain, Apphelp, Drvmain o Msimain).
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: Función SdbIsStandardDatabase
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
ms.openlocfilehash: 7ef30f54b4d8eb4df4d8f136de6357a072cdb0183f462cb3af8a9340ce68b0c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045195"
---
# <a name="sdbisstandarddatabase-function"></a>Función SdbIsStandardDatabase

Determina si la base de datos especificada es una de las bases de datos estándar (Sysmain, Apphelp, Drvmain o Msimain).

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*GuidDB* \[ En\]
</dt> <dd>

GUID de la base de datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **TRUE si** el GUID representa una base de datos estándar o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




