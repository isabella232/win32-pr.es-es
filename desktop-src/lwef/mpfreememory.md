---
title: Función MpFreeMemory (MpClient.h)
description: Libera memoria para el administrador de protección contra malware.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- Función MpFreeMemory Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MpFreeMemory
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 806795cee45fcfe95473c0961106da074c1157b65ac5c19f5d4813c84865616a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247430"
---
# <a name="mpfreememory-function"></a>Función MpFreeMemory

Libera memoria para el administrador de protección contra malware. El autor de la llamada debe liberar todos los búferes asignados y devueltos por las funciones de protección contra malware mediante esta función.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMemory* \[ En\]
</dt> <dd>

Tipo: **PVOID**

Puntero a la memoria asignada por una función de protección contra malware.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Para facilitar la administración de memoria para los clientes, el administrador de protección contra malware también define macros para liberar memoria asociada a varias estructuras devueltas por las funciones de protección contra malware. Las macros siguientes se definen en el archivo de encabezado mpmemfree.h:



| Nombre                            | Descripción                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| MPRESOURCE \_ INFO \_ FREE          | Libera una información de [**MPRESOURCE \_ asignada.**](mpresource-info.md)                  |
| MPTHREAT \_ INFO \_ FREE            | Libera una información [**de MPTHREAT \_ asignada.**](mpthreat-info.md)                      |
| MPTHREAT \_ LOCALIZED \_ INFO \_ FREE | Libera una información localizada [**de MPTHREAT \_ \_ asignada.**](mpthreat-localized-info.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MPRESOURCE \_ INFO**](mpresource-info.md)
</dt> <dt>

[**INFORMACIÓN DE \_ MPTHREAT**](mpthreat-info.md)
</dt> <dt>

[**INFORMACIÓN LOCALIZADA DE MPTHREAT \_ \_**](mpthreat-localized-info.md)
</dt> </dl>

 

 





