---
title: Estructura de STOWED_EXCEPTION_INFORMATION_HEADER
description: Contiene información que identifica la estructura primaria.
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- Estructura de STOWED_EXCEPTION_INFORMATION_HEADER Informe de errores de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079680"
---
# <a name="stowed_exception_information_header-structure"></a>Estructura de \_ \_ encabezado de información de excepción estibada \_

Contiene información que identifica la estructura primaria.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_HEADER {
  ULONG Size;
  ULONG Signature;
} STOWED_EXCEPTION_INFORMATION_HEADER, *PSTOWED_EXCEPTION_INFORMATION_HEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tamaño**
</dt> <dd>

Tipo: **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tamaño, en bytes, de la estructura primaria.

</dd> <dt>

**Signature**
</dt> <dd>

Tipo: **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor de 32 bits que especifica la firma de la estructura primaria.



| Value                                                                                                                                                                                                                                                                                                            | Significado                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> <dt>**\_ Estibada \_ \_ \_ Firma de la información de excepción v1**</dt> <dt>' SE01 '</dt> </dl> | Este valor indica que el elemento primario es una estructura de **información de excepción de estibada \_ \_ \_ v1** .<br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> <dt>**\_ Estibada Firma de información de la \_ \_ versión V2 \_**</dt> <dt>' SE02 '</dt> </dl> | Este valor indica que el elemento primario es una estructura de [**\_ información de excepción \_ \_ 2 estibada**](stowed-exception-information-v2.md) .<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

[**\_ Estibada La \_ información \_ de excepción V2**](stowed-exception-information-v2.md) y el **\_ encabezado de \_ información \_ de excepción estibada** no se definen actualmente en un encabezado que está disponible públicamente, por lo que debe definirlos en el código fuente antes de usarlos.

La estructura V1 de la **\_ información de excepción \_ \_ estibada** es idéntica a esta estructura, salvo que no contiene los miembros **NestedExceptionType** y **NestedException** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>None</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Información de \_ excepción estibada \_ \_ V2**](stowed-exception-information-v2.md)
</dt> </dl>

 

