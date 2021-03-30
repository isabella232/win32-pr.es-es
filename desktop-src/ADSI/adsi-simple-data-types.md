---
title: Tipos de datos simples de ADSI (iAds. h)
description: Active Directory interfaces de servicio (ADSI) define y usa los siguientes tipos de datos simples.
ms.assetid: 0bd34f13-269f-4f5d-8a18-74577522e402
ms.tgt_platform: multiple
keywords:
- ADS_BOOLEAN
- ADS_CASE_EXACT_STRING
- ADS_CASE_IGNORE_STRING
- ADS_DN_STRING
- ADS_INTEGER
- ADS_LARGE_INTEGER
- ADS_NUMERIC_STRING
- ADS_OBJECT_CLASS
- ADS_PRINTABLE_STRING
- ADS_SEARCH_HANDLE
- ADS_UTC_TIME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5530fda2ca1f4fe967eaf376b668a0bedc29c4b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079010"
---
# <a name="adsi-simple-data-types"></a>Tipos de datos simples de ADSI

Active Directory interfaces de servicio (ADSI) define y usa los siguientes tipos de datos simples.


```C++
typedef DWORD ADS_BOOLEAN, *PADS_BOOLEAN;
typedef LPWSTR ADS_CASE_EXACT_STRING, *PADS_CASE_EXACT_STRING;
typedef LPWSTR ADS_CASE_IGNORE_STRING, *PADS_CASE_IGNORE_STRING;
typedef LPWSTR ADS_DN_STRING, *PADS_DN_STRING;
typedef DWORD ADS_INTEGER, *PADS_INTEGER;
typedef LARGE_INTEGER ADS_LARGE_INTEGER, *PADS_LARGE_INTEGER;
typedef LPWSTR ADS_NUMERIC_STRING, *PADS_NUMERIC_STRING;
typedef LPWSTR ADS_OBJECT_CLASS, *PADS_OBJECT_CLASS;
typedef LPWSTR ADS_PRINTABLE_STRING, *PADS_PRINTABLE_STRING;
typedef HANDLE ADS_SEARCH_HANDLE, *PADS_SEARCH_HANDLE;
typedef SYSTEMTIME ADS_UTC_TIME, *PADS_UTC_TIME;
```



<dl> <dt>

**ADS \_ booleano**
</dt> <dd>

DWORD

</dd> <dt>

**\_ \_ cadena exacta de caso de ADS \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**caso de ADS \_ \_ omitir \_ cadena**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_cadena DN de ADS \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**entero de ADS \_**
</dt> <dd>

DWORD

</dd> <dt>

**\_entero grande de ADS \_**
</dt> <dd>

[**\_entero grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

**\_cadena numérica de ADS \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_clase de objeto ADS \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_cadena imprimible de ADS \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_identificador de búsqueda de ADS \_**
</dt> <dd>

HANDLE

</dd> <dt>

**\_hora UTC de ADS \_**
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando ADSI Lee un atributo que se ha definido como un **entero** en el esquema LDAP, siempre controlará el entero como un valor de 32 bits y puede truncar los datos. Esto solo es un problema para los servidores LDAP que permiten valores enteros de tamaño arbitrario. Si el atributo es un atributo personalizado que se define extendiendo el esquema, este problema se puede evitar definiendo el atributo personalizado como una cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                    |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl> |



 

