---
title: Enumeración BITS_FILE_PROPERTY_ID (Deliveryoptimization. h)
description: La enumeración BITS_FILE_PROPERTY_ID especifica valores que definen los valores de identificador correspondientes a las propiedades BackgroundCopyFile.
ms.assetid: 47EFD160-7CA8-48E6-A18E-38D85F7C6E47
keywords:
- Enumeración BITS_FILE_PROPERTY_ID
- Enumeración BITS_FILE_PROPERTY_ID
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b6c6b8a4de359e8313e3127080f2cc17ae6478c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714570"
---
# <a name="bits_file_property_id-enumeration"></a>Enumeración BITS_FILE_PROPERTY_ID

La enumeración **BITS_FILE_PROPERTY_ID** especifica valores que definen los valores de identificador correspondientes a las propiedades **BackgroundCopyFile** .

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _BITS_FILE_PROPERTY_ID { 
  BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS  = 1
} BITS_FILE_PROPERTY_ID;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS"></span><span id="bits_file_property_id_http_response_headers"></span>**BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**
</dt> <dd>

Conjunto completo de encabezados de respuesta HTTP del último paquete de respuesta HTTP del servidor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 





