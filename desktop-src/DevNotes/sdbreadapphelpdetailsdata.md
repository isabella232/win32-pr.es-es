---
Description: Recupera datos de la base de datos de detalles de Apphelp.
ms.assetid: f3731561-bf3f-4139-9890-bd4ce73d83fa
title: Función SdbReadApphelpDetailsData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadApphelpDetailsData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a9e116080ffbfd81cff7dca8674b6be6fc977f3f7b3024bf32779887bde04d03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404414"
---
# <a name="sdbreadapphelpdetailsdata-function"></a>Función SdbReadApphelpDetailsData

Recupera datos de la base de datos de detalles de Apphelp.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbReadApphelpDetailsData(
  _In_  PDB           pdb,
  _Out_ PAPPHELP_DATA pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdb* \[ En\]
</dt> <dd>

Identificador de la base de datos de detalles de Apphelp, Apphelp.sdb.

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Una [**estructura DE DATOS \_ APPHELP.**](apphelp-data.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **TRUE si** se ejecuta correctamente o **FALSE** en caso de error.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




