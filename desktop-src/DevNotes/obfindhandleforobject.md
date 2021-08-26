---
description: Recupera un identificador de objeto para el objeto especificado asociado al proceso especificado.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: Función ObFindHandleForObject (Ntosp.h)
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
ms.openlocfilehash: 481def34e3e8656205eefe96058fe3c7558d2c898c7e05ddc78f9a67435c507e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984155"
---
# <a name="obfindhandleforobject-function"></a>Función ObFindHandleForObject

\[Esta función está obsoleta y puede modificarse o no estar disponible en versiones futuras de Windows. Evite usar esta función.\]

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

*Proceso* \[ En\]
</dt> <dd>

Proceso. La función **IoGetCurrentProcess** o **PsGetCurrentProcess** devuelven este identificador.

</dd> <dt>

*Objeto* \[ En\]
</dt> <dd>

Puntero al objeto .

</dd> <dt>

*Reservado1* \[ en, opcional\]
</dt> <dd>

Reservado.

</dd> <dt>

*Reservado2* \[ en, opcional\]
</dt> <dd>

Reservado.

</dd> <dt>

*Identificador* \[ out\]
</dt> <dd>

Identificador de objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **TRUE si** se encuentra una coincidencia y FALSE en **caso** contrario.

## <a name="remarks"></a>Comentarios

Esta función está disponible en Ntoskrnl.exe y solo se puede llamar desde el modo kernel. La biblioteca de importación correspondiente está disponible a través de Windows Driver Kit (WDK).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Ntosp.h</dt> </dl>      |
| Biblioteca<br/>                  | <dl> <dt>Ntoskrnl.lib</dt> </dl> |



 

 




