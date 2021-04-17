---
title: BITS_FILE_PROPERTY_VALUE estructura (Deliveryoptimization. h)
description: La Unión BITS_FILE_PROPERTY_VALUE proporciona el valor de propiedad del archivo DO basado en un valor de la enumeración BITS_FILE_PROPERTY_ID.
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- Estructura de BITS_FILE_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 639ea0523c5b92d9764671cb573497223ef968fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714549"
---
# <a name="bits_file_property_value-structure"></a>Estructura de BITS_FILE_PROPERTY_VALUE

La Unión **BITS_FILE_PROPERTY_VALUE** proporciona el valor de propiedad del archivo do basado en un valor de la enumeración [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  LPWSTR String;
} BITS_FILE_PROPERTY_VALUE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**String**
</dt> <dd>

Este valor se usa cuando se usa el valor de enumeración de ID. de propiedad **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md)
</dt> <dt>

[**IBackgroundCopyFile5. GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[**IBackgroundCopyFile5. SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





