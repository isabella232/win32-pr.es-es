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
ms.openlocfilehash: f34ecc3d0c3eeb085d2a7c0f8c4cb0426663093c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069345"
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

Identificador experto único. Monitor de red pasa *hE expert al* experto cuando llama a la [función Run.](run.md)

</dd> <dt>

*pEcialStartupInfo* \[ out\]
</dt> <dd>

Puntero a una [estructura EXPERTSTARTUPINFO](expertstartupinfo.md) que contiene información de inicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es NMERR.

## <a name="remarks"></a>Observaciones

La **función ExpertGetStartupInfo** se usa si el experto debe determinar la información de inicio que se usa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




