---
title: BITS_FILE_PROPERTY_VALUE estructura (Deliveryoptimization.h)
description: La BITS_FILE_PROPERTY_VALUE de datos proporciona el valor de propiedad del archivo DO basado en un valor de la BITS_FILE_PROPERTY_ID enumeración.
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- BITS_FILE_PROPERTY_VALUE estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567165"
---
# <a name="bits_file_property_value-structure"></a>BITS_FILE_PROPERTY_VALUE estructura

La **BITS_FILE_PROPERTY_VALUE** de datos proporciona el valor de propiedad del archivo DO basado en un valor de la [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) enumeración.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  LPWSTR String;
} BITS_FILE_PROPERTY_VALUE;
```



## <a name="members"></a>Members

<dl> <dt>

**String**
</dt> <dd>

Este valor se usa cuando se usa el valor de enumeración de identificador de **propiedad BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md)
</dt> <dt>

[**IBackgroundCopyFile5.GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[**IBackgroundCopyFile5.SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





