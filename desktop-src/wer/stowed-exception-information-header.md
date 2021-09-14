---
title: STOWED_EXCEPTION_INFORMATION_HEADER estructura
description: Contiene información que identifica la estructura primaria.
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- STOWED_EXCEPTION_INFORMATION_HEADER estructura Informe de errores de Windows
- PSTOWED_EXCEPTION_INFORMATION_HEADER puntero de estructura Informe de errores de Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_HEADER
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101bb1fb1555c829622a42c17fdfb01488c57636
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251847"
---
# <a name="stowed_exception_information_header-structure"></a>ESTRUCTURA STOWED \_ EXCEPTION \_ INFORMATION \_ HEADER

Contiene información que identifica la estructura primaria.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_HEADER {
  ULONG Size;
  ULONG Signature;
} STOWED_EXCEPTION_INFORMATION_HEADER, *PSTOWED_EXCEPTION_INFORMATION_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**Tamaño**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tamaño, en bytes, de la estructura primaria.

</dd> <dt>

**Signature**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor de 32 bits que especifica la firma de la estructura primaria.



| Value                                                                                                                                                                                                                                                                                                            | Significado                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> <dt>**STOWED \_ INFORMACIÓN \_ DE \_ EXCEPCIÓN FIRMA V1 \_**</dt> <dt>'SE01'</dt> </dl> | Este valor indica que el elemento primario es una **estructura STOWED \_ EXCEPTION INFORMATION \_ \_ V1.**<br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> <dt>**STOWED \_ EXCEPTION \_ INFORMATION \_ V2 \_ SIGNATURE**</dt> <dt>'SE02'</dt> </dl> | Este valor indica que el elemento primario es una [**estructura STOWED \_ EXCEPTION INFORMATION \_ \_ V2.**](stowed-exception-information-v2.md)<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

[**STOWED \_ EXCEPTION \_ INFORMATION \_ V2**](stowed-exception-information-v2.md) y **STOWED EXCEPTION INFORMATION \_ \_ \_ HEADER** no están definidos actualmente en un encabezado que esté disponible públicamente, por lo que debe definirlos en el código fuente antes de usarlos.

La **estructura STOWED \_ EXCEPTION INFORMATION \_ \_ V1** es idéntica a esta estructura, salvo que no contiene los miembros **NestedExceptionType** y **NestedException.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                      |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Ninguna</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INFORMACIÓN DE \_ EXCEPCIÓN \_ STOWED \_ V2**](stowed-exception-information-v2.md)
</dt> </dl>

 

