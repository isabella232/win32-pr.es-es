---
title: Estructura de WINBIO_BIR (Winbio \_ Types. h)
description: Representa un registro de información biométrica (BIR).
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- Plataforma de biometría de Windows API de WINBIO_BIR Structure
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686214"
---
# <a name="winbio_bir-structure"></a>WINBIO \_ estructura Bir

La estructura **WINBIO \_ Bir** representa un registro de información biométrica (BIR). El registro de información contiene los bloques de encabezado, de datos y de firma.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_BIR {
  WINBIO_BIR_DATA HeaderBlock;
  WINBIO_BIR_DATA StandardDataBlock;
  WINBIO_BIR_DATA VendorDataBlock;
  WINBIO_BIR_DATA SignatureBlock;
} WINBIO_BIR;
```



## <a name="members"></a>Miembros

<dl> <dt>

**HeaderBlock**
</dt> <dd>

Una estructura de [**\_ \_ datos de WINBIO Bir**](winbio-bir-data.md) que contiene el tamaño, en bytes, y el desplazamiento del encabezado Bir. El encabezado contiene información que describe el contenido del registro de información.

</dd> <dt>

**StandardDataBlock**
</dt> <dd>

Una estructura de [**\_ \_ datos de WINBIO Bir**](winbio-bir-data.md) que contiene el tamaño, en bytes, y el desplazamiento de la información biométrica procesada o no procesada creada por el plataforma de biometría de Windows (WBF).

</dd> <dt>

**VendorDataBlock**
</dt> <dd>

Una estructura de [**\_ \_ datos de WINBIO Bir**](winbio-bir-data.md) que contiene el tamaño, en bytes, y el desplazamiento de la información biométrica procesada o no procesada proporcionada por los sensores y el software del proveedor.

</dd> <dt>

**SignatureBlock**
</dt> <dd>

Una estructura [**de \_ \_ datos WINBIO Bir**](winbio-bir-data.md) opcional que contiene el tamaño, en bytes, y el desplazamiento del código de autenticación de mensajes (Mac) de firma digital que se puede usar para comprobar la integridad de la Bir. Si está presente, la firma o el MAC deben cubrir el encabezado y los bloques de datos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El uso de desplazamientos en lugar de punteros permite una sencilla serialización de BIR y para una traducción menos complicada entre los entornos 32 y 64-bit o entre el modo de usuario y kernel.

BIR es compatible con el marco de trabajo de intercambio biométrico común (CBEFF) definido por NIST 6529-A.

Si esta estructura contiene un valor *StandardDataBlock* , el parámetro de *tipo* del encabezado especificado por el parámetro *HeaderBlock* debe establecerse en **el \_ \_ tipo de \_ formato \_ WINBIO ANSI 381**. Este es el único formato de datos estándar que admite la versión actual de la Plataforma de biometría de Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> <dt>

[**datos de WINBIO \_ Bir \_**](winbio-bir-data.md)
</dt> <dt>

[**WINBIO \_ \_ encabezado Bir**](winbio-bir-header.md)
</dt> </dl>

 

 





