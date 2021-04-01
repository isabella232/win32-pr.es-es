---
description: Recupera un identificador de objeto para el objeto especificado asociado al proceso especificado.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: Función ObFindHandleForObject (Ntosp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObFindHandleForObject
api_type:
- LibDef
api_location:
- Ntoskrnl.lib
- Ntoskrnl.dll
ms.openlocfilehash: 7ba87d05d4264f3bb160bae16053a338e38e2145
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907060"
---
# <a name="obfindhandleforobject-function"></a>ObFindHandleForObject función)

\[Esta función está obsoleta y puede modificarse o no estar disponible en versiones futuras de Windows. Evite el uso de esta función.\]

Recupera un identificador de objeto para el objeto especificado asociado al proceso especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOLEAN WINAPI ObFindHandleForObject(
  _In_     PEPROCESS Process,
  _In_     PVOID     Object,
  _In_opt_ PVOID     Reserved1,
  _In_opt_ PVOID     Reserved2,
  _Out_    PHANDLE   Handle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Proceso* \[ de de\]
</dt> <dd>

Proceso. Este identificador es devuelto por la función **IoGetCurrentProcess** o **PsGetCurrentProcess** .

</dd> <dt>

*Objeto* \[ de de\]
</dt> <dd>

Puntero al objeto.

</dd> <dt>

*Reserved1* \[ en, opcional\]
</dt> <dd>

Reservado.

</dd> <dt>

*Reserved2* \[ en, opcional\]
</dt> <dd>

Reservado.

</dd> <dt>

*Identificador* \[ de enuncia\]
</dt> <dd>

Identificador del objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **true** si se encuentra una coincidencia y **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Esta función está disponible en Ntoskrnl.exe y solo se puede llamar desde el modo kernel. La biblioteca de importación correspondiente está disponible a través de Windows Driver Kit (WDK).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Ntosp. h</dt> </dl>      |
| Biblioteca<br/>                  | <dl> <dt>Ntoskrnl. lib</dt> </dl> |



 

 




