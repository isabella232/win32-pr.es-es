---
description: Contiene información básica del módulo.
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: AUX_MODULE_BASIC_INFO estructura (AUX \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_BASIC_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 1ee7300ec2c2d84e1ddadc4149135dab53d2336b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649967"
---
# <a name="aux_module_basic_info-structure"></a>\_Estructura de \_ información básica del módulo AUX \_

Contiene información básica del módulo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ImageBase**
</dt> <dd>

La dirección base del módulo dentro del espacio de direcciones del kernel.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La biblioteca de objetos que implementa esta API se puede descargar desde [aquí](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | Biblioteca de API auxiliar de Windows versión 1,0 o posterior<br/>                          |
| Encabezado<br/>          | <dl> <dt>AUX \_ klib. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




