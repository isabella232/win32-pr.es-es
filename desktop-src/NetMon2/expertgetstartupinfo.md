---
description: La función ExpertGetStartupInfo recupera la información de configuración de inicio del experto.
ms.assetid: 15f080ed-50b7-40c6-b283-dbe416a2b0e9
title: Función ExpertGetStartupInfo (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetStartupInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7e4327965dce1c4bca07846a818609e555c16a3a27b0a19204a9971eaf9d642e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366887"
---
# <a name="expertgetstartupinfo-function"></a>Función ExpertGetStartupInfo

La **función ExpertGetStartupInfo** recupera la información de configuración de inicio del experto.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI ExpertGetStartupInfo(
  _In_  HEXPERTKEY         hExpertKey,
  _Out_ PEXPERTSTARTUPINFO pExpertStartupInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hExpertKey* \[ En\]
</dt> <dd>

Identificador único de experto. Monitor de red pasa *hExpertKey* al experto cuando llama a la [función Run.](run.md)

</dd> <dt>

*pEiqueStartupInfo* \[ out\]
</dt> <dd>

Puntero a una [estructura EXPERTSTARTUPINFO](expertstartupinfo.md) que contiene información de inicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es NMERR.

## <a name="remarks"></a>Comentarios

La **función ExpertGetStartupInfo** se usa si el experto debe determinar la información de inicio que se usa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




