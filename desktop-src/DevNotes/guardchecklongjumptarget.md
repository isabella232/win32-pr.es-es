---
UID: ''
title: Función GuardCheckLongJumpTarget
description: Intenta comprobar si el destino de un longjmp es válido.
old-location: ''
ms.assetid: na
ms.date: 04/02/2019
ms.keywords: ''
ms.topic: reference
req.header: guardapiset.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- api-ms-win-core-guard-l1-1-0.dll
api_name:
- GuardCheckLongJumpTarget
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: bcc8565401e09e8a4a3e0dfb221f240255b00bd0e91b9c2611b21db3ee1c0201
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002265"
---
# <a name="guardchecklongjumptarget-function"></a>Función GuardCheckLongJumpTarget

## <a name="description"></a>Descripción

Intenta comprobar si el destino de [un longjmp](/cpp/c-runtime-library/reference/longjmp) es válido para un proceso que tiene [habilitado Control Flow Guard (CFG).](../secbp/control-flow-guard.md)

Si la dirección de destino corresponde a una asignación de imagen, se extraen los destinos válidos para el binario.
La función usa esos destinos para validar el destino.
Si el archivo binario no tiene metadatos que describan el conjunto de destinos *longjmp* válidos, la función devuelve **TRUE.**

Si la dirección de destino corresponde a una asignación que no es de imagen, como en el código JIT, se consulta una directiva de solo lectura global para determinar si se permite el salto.

## <a name="parameters"></a>Parámetros

### <a name="targetaddress-in"></a>TargetAddress [in]

Dirección de destino del salto.

### <a name="flags-in"></a>Flags [in]

Marcas que describen la operación que se va a realizar en la dirección.
Si especifica **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), esta función no finaliza el proceso si el destino no es válido.

## <a name="returns"></a>Devoluciones

**TRUE** si el destino es válido; de lo **contrario, FALSE.**

## <a name="remarks"></a>Comentarios

## <a name="see-also"></a>Vea también
