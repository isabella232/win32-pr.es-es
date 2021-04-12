---
UID: ''
title: LsaManageSidNameMapping función)
description: Agrega o quita asignaciones de SID/nombre del conjunto de asignaciones registrado con el servicio de búsqueda de LSA.
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
ms.openlocfilehash: fc0065c3964718d690149693f3c71ec4e9f676ec
ms.sourcegitcommit: 382c7259008374408368c173e0027fb641c848fe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/22/2020
ms.locfileid: "104358759"
---
# <a name="lsamanagesidnamemapping-function"></a>LsaManageSidNameMapping función)

## <a name="description"></a>Descripción

La función **LsaManageSidNameMapping** agrega o quita asignaciones SID/Name del conjunto de asignaciones registrado con el servicio de búsqueda de LSA.

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a>Parámetros

### <a name="optype-in"></a>OpType [in]

Indica si se llama a esta función para agregar o quitar una asignación de SID/nombre.

### <a name="opinput-in"></a>OpInput [in]

Indica los valores de dominio, cuenta y SID que se van a usar durante esta operación. También se pueden establecer marcas adicionales en esta estructura.

### <a name="opoutput-out"></a>OpOutput [out]

Contiene un valor de [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) que indica si la operación se ha realizado correctamente o no.

| Value | Significado |
|-------|---------|
| **Success** | La operación se completó sin errores. |
| **NonMappingError** | Se ha producido un error no relacionado con la asignación de nombre de SID. |
| **NameCollision** | Error de la operación debido a un conflicto de nombres. |
| **SidCollision** | Error de la operación debido a un conflicto de SID. |
| **DomainNotFound** | No se encontró el dominio correspondiente. |
| **DomainSidPrefixMismatch** | El SID proporcionado no tiene el prefijo de dominio correcto. |
| **MappingNotFound** | No se encontró la asignación en la memoria caché. |

## <a name="returns"></a>Devoluciones

Si la asignación se inserta correctamente, el valor devuelto es STATUS_SUCCESS.
De lo contrario, si se produce un error en la función debido a conflictos de SID o de nombre, se devolverá STATUS_INVALID_PARAMETER error.

## <a name="remarks"></a>Observaciones

## <a name="see-also"></a>Vea también
