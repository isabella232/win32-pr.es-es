---
title: WINBIO_BIR estructura (Tipos de \_ Winbio.h)
description: Representa un registro de información biométrica (BIR).
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- WINBIO_BIR estructura Windows API de marco biométrico
topic_type:
- apiref
api_name:
- WINBIO_BIR
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422bbe59414d75541127b41e5e2cc1829adaaa7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071157"
---
# <a name="winbio_bir-structure"></a>Estructura DE \_ WINBIO BIR

La **estructura BIR \_ de WINBIO** representa un registro de información biométrica (BIR). El registro de información contiene bloques de encabezado, datos y firmas.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_BIR {
  WINBIO_BIR_DATA HeaderBlock;
  WINBIO_BIR_DATA StandardDataBlock;
  WINBIO_BIR_DATA VendorDataBlock;
  WINBIO_BIR_DATA SignatureBlock;
} WINBIO_BIR;
```



## <a name="members"></a>Members

<dl> <dt>

**HeaderBlock**
</dt> <dd>

Estructura [**DE DATOS DE \_ WINBIO BIR \_**](winbio-bir-data.md) que contiene el tamaño, en bytes y el desplazamiento del encabezado BIR. El encabezado contiene información que describe el contenido del registro de información.

</dd> <dt>

**StandardDataBlock**
</dt> <dd>

Estructura DE DATOS BIR de [**WINBIO \_ \_**](winbio-bir-data.md) que contiene el tamaño, en bytes y el desplazamiento de la información biométrica procesada o no procesada creada por Windows Biometric Framework (WBF).

</dd> <dt>

**VendorDataBlock**
</dt> <dd>

Estructura [**DE DATOS DE \_ WINBIO BIR \_**](winbio-bir-data.md) que contiene el tamaño, en bytes y el desplazamiento de la información biométrica procesada o no procesada que proporcionan los sensores y el software del proveedor.

</dd> <dt>

**SignatureBlock**
</dt> <dd>

Estructura [**opcional WINBIO \_ BIR \_ DATA**](winbio-bir-data.md) que contiene el tamaño, en bytes y el desplazamiento del código de autenticación de mensajes de firma digital (MAC) que se puede usar para comprobar la integridad de LA BIR. Si está presente, la firma o mac deben cubrir los bloques de encabezado y de datos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El uso de desplazamientos en lugar de punteros permite una serialización sencilla de BIR y una traducción menos complicada entre entornos de 32 y 64 bits o entre el modo de usuario y kernel.

BIR es compatible con Common Biometric Exchange Format Framework (CBEFF) definido por NIST 6529-A.

Si esta estructura contiene un valor *StandardDataBlock,* el parámetro *Type* del encabezado especificado por el parámetro *HeaderBlock* debe establecerse en **WINBIO \_ ANSI \_ 381 \_ FORMAT \_ TYPE**. Este es el único formato de datos estándar admitido por la versión actual de Windows Biometric Framework.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> <dt>

[**DATOS DE WINBIO \_ BIR \_**](winbio-bir-data.md)
</dt> <dt>

[**ENCABEZADO WINBIO \_ BIR \_**](winbio-bir-header.md)
</dt> </dl>

 

 





