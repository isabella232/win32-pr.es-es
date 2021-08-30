---
description: Contiene información extendida del módulo.
ms.assetid: 705769de-0aeb-4a28-b174-8620efa74baf
title: AUX_MODULE_EXTENDED_INFO estructura (Aux \_ klib.h)
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
ms.openlocfilehash: a2fec3554faee39cb965f9b5dabe83e2d436bb7a1b8bc5995ea139cbd5761852
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045335"
---
# <a name="aux_module_extended_info-structure"></a>Estructura AUX \_ MODULE \_ EXTENDED \_ INFO

Contiene información extendida del módulo.

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

Una [**estructura DE INFORMACIÓN BÁSICA DEL MÓDULO \_ \_ \_ AUXILIAR.**](aux-module-basic-info-struct.md)

</dd> <dt>

**ImageSize**
</dt> <dd>

Tamaño, en bytes, del módulo cargado.

</dd> <dt>

**FileNameOffset**
</dt> <dd>

Desplazamiento del nombre de archivo dentro del **búfer FullPathName.**

</dd> <dt>

**FullPathName**
</dt> <dd>

Ruta de acceso completa del módulo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La biblioteca de objetos que implementa esta API se puede descargar desde [aquí.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows Biblioteca de API auxiliar versión 1.0 o posterior<br/>                          |
| Header<br/>          | <dl> <dt>Aux \_ klib.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> <dt>

[**INFORMACIÓN \_ BÁSICA DEL MÓDULO \_ \_ AUXILIAR**](aux-module-basic-info-struct.md)
</dt> </dl>

 

 




