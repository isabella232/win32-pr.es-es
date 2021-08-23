---
description: Contiene información básica del módulo.
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: AUX_MODULE_BASIC_INFO estructura (Auxiliar \_ klib.h)
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
ms.openlocfilehash: e1a25af780016c226acf46348573def8505669e16f1f645fcfce1c9324bb086d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956154"
---
# <a name="aux_module_basic_info-structure"></a>ESTRUCTURA DE \_ INFORMACIÓN \_ BÁSICA DEL \_ MÓDULO AUXILIAR

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

Dirección base del módulo dentro del espacio de direcciones del kernel.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La biblioteca de objetos que implementa esta API se puede descargar desde [aquí.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows Biblioteca de API auxiliar versión 1.0 o posterior<br/>                          |
| Header<br/>          | <dl> <dt>Auxiliar \_ klib.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




