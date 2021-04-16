---
UID: ''
title: GuardCheckLongJumpTarget función)
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
ms.openlocfilehash: 02f659f77ab2bace129c9b9d9011b4c93e59b2f4
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2020
ms.locfileid: "105656323"
---
# <a name="guardchecklongjumptarget-function"></a>GuardCheckLongJumpTarget función)

## <a name="description"></a>Descripción

Intenta comprobar si el destino de un [longjmp](/cpp/c-runtime-library/reference/longjmp) es válido para un proceso que tiene habilitada la [protección de flujo de control (cfg)](../secbp/control-flow-guard.md) .

Si la dirección de destino corresponde a una asignación de imagen, se extraen los destinos válidos para el archivo binario.
La función utiliza esos destinos para validar el destino.
Si el binario no tiene metadatos que describan el conjunto de destinos *longjmp* válidos, la función devuelve **true**.

Si la dirección de destino corresponde a una asignación que no es de imagen, como en el código JIT, se consulta una directiva global de solo lectura para determinar si se permite el salto.

## <a name="parameters"></a>Parámetros

### <a name="targetaddress-in"></a>TargetAddress [in]

Dirección de destino del salto.

### <a name="flags-in"></a>Flags [in]

Marcas que describen la operación que se va a realizar en la dirección.
Si especifica **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), esta función no finaliza el proceso si el destino no es válido.

## <a name="returns"></a>Devoluciones

**True** si el destino es válido; en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

## <a name="see-also"></a>Vea también
