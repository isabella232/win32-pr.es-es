---
UID: ''
title: Función LsaManageSidNameMapping
description: Agrega o quita las asignaciones de SID o nombre del conjunto de asignaciones registrado con el servicio de búsqueda LSA.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: ''
ms.topic: reference
req.header: Ntsecapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Secur32.lib
req.dll:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
- API-MS-Win-security-lsalookup-l2-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name:
- LsaManageSidNameMapping
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 6c2a66a318076588b725f74e9f03a23b8a134595b196dbf140850e72a7d78d8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921864"
---
# <a name="lsamanagesidnamemapping-function"></a>Función LsaManageSidNameMapping

## <a name="description"></a>Descripción

La **función LsaManageSidNameMapping** agrega o quita las asignaciones de SID o nombre del conjunto de asignaciones registrado con el servicio de búsqueda de LSA.

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a>Parámetros

### <a name="optype-in"></a>OpType [in]

Indica si se llama a esta función para agregar o quitar una asignación de SID o nombre.

### <a name="opinput-in"></a>OpInput [in]

Indica los valores de dominio, cuenta y SID que se usarán durante esta operación. También se pueden establecer marcas adicionales dentro de esta estructura.

### <a name="opoutput-out"></a>OpOutput [out]

Contiene un valor de [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) que indica que la operación se ha correcto o no.

| Valor | Significado |
|-------|---------|
| **Success** | La operación se completa sin errores. |
| **NonMappingError** | Se ha producido un error no relacionado con la asignación de nombres de SID. |
| **NameCollision** | Error de operación debido a una colisión de nombres. |
| **SidCollision** | Error de operación debido a una colisión de SID. |
| **DomainNotFound** | No se encontró el dominio correspondiente. |
| **DomainSidPrefixMismatch** | El SID proporcionado no tiene el prefijo de dominio correcto. |
| **MappingNotFound** | Asignación no encontrada en la memoria caché. |

## <a name="returns"></a>Devoluciones

Si la asignación se inserta correctamente, el valor devuelto es STATUS_SUCCESS.
De lo contrario, si se produce un error en la función debido a conflictos de nombre o SID, STATUS_INVALID_PARAMETER error se devolverá.

## <a name="remarks"></a>Comentarios

## <a name="see-also"></a>Consulte también
