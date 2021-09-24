---
title: BITS_FILE_PROPERTY_VALUE estructura (Deliveryoptimization.h)
description: La BITS_FILE_PROPERTY_VALUE de datos proporciona el valor de propiedad del archivo Optimización de distribución basado en un valor de la enumeración BITS_FILE_PROPERTY_ID datos.
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
ms.openlocfilehash: 10cceedf2e3da2578c9e3f7d0e8131b98f78093b
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520880"
---
# <a name="bits_file_property_value-structure"></a>BITS_FILE_PROPERTY_VALUE estructura

La **BITS_FILE_PROPERTY_VALUE** de datos proporciona el valor de propiedad del archivo Optimización de distribución basado en un valor de la [**enumeración BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) datos.

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

 

 





