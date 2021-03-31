---
title: Función MpFreeMemory (MpClient. h)
description: Libera memoria para el administrador de protección contra malware de.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- Función MpFreeMemory características de entorno heredado de Windows
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
ms.openlocfilehash: a15a2845b034a3aa739b1ba2f33a023b742b4b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801909"
---
# <a name="mpfreememory-function"></a>MpFreeMemory función)

Libera memoria para el administrador de protección contra malware de. El autor de la llamada debe liberar todos los búferes asignados y devueltos por las funciones de protección contra malware mediante esta función.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMemory* \[ de\]
</dt> <dd>

Tipo: **PVOID**

Puntero a la memoria asignada por una función de protección contra malware.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para facilitar la administración de la memoria para los clientes, el administrador de protección contra malware también define las macros para liberar memoria asociada a las distintas estructuras devueltas por las funciones de protección contra malware. Las siguientes macros se definen en el archivo de encabezado mpmemfree. h:



| Nombre                            | Descripción                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| MPRESOURCE \_ info \_ Free          | Libera una información de [**MPRESOURCE \_**](mpresource-info.md)asignada.                  |
| MPTHREAT \_ info \_ Free            | Libera una información de [**MPTHREAT \_**](mpthreat-info.md)asignada.                      |
| MPTHREAT \_ \_ información localizada \_ gratis | Libera [**\_ \_ información localizada MPTHREAT**](mpthreat-localized-info.md)asignada. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**información de MPRESOURCE \_**](mpresource-info.md)
</dt> <dt>

[**información de MPTHREAT \_**](mpthreat-info.md)
</dt> <dt>

[**\_información localizada de MPTHREAT \_**](mpthreat-localized-info.md)
</dt> </dl>

 

 





