---
description: Contiene información del módulo extendido.
ms.assetid: 705769de-0aeb-4a28-b174-8620efa74baf
title: AUX_MODULE_EXTENDED_INFO estructura (AUX \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_EXTENDED_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 9faa706ca3603a1796d70e2f208e9b3b2e518c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650070"
---
# <a name="aux_module_extended_info-structure"></a>\_Estructura de \_ información ampliada del módulo AUX \_

Contiene información del módulo extendido.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _AUX_MODULE_EXTENDED_INFO {
  AUX_MODULE_BASIC_INFO BasicInfo;
  ULONG                 ImageSize;
  USHORT                FileNameOffset;
  UCHAR                 FullPathName[AUX_KLIB_MODULE_PATH_LEN];
} AUX_MODULE_EXTENDED_INFO, *PAUX_MODULE_EXTENDED_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**BasicInfo**
</dt> <dd>

Una estructura de [**\_ \_ \_ información básica del módulo AUX**](aux-module-basic-info-struct.md) .

</dd> <dt>

**ImageSize**
</dt> <dd>

Tamaño, en bytes, del módulo cargado.

</dd> <dt>

**FileNameOffset**
</dt> <dd>

Desplazamiento del nombre de archivo dentro del búfer de **FullPathName** .

</dd> <dt>

**FullPathName**
</dt> <dd>

Ruta de acceso completa del módulo.

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
</dt> <dt>

[**\_ \_ información básica del módulo AUX \_**](aux-module-basic-info-struct.md)
</dt> </dl>

 

 




