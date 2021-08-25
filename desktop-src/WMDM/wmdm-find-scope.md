---
title: WMDM_FIND_SCOPE enumeración
description: El tipo de enumeración FIND SCOPE de WMDM \_ define el ámbito del objeto de \_ almacenamiento.
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- WMDM_FIND_SCOPE enumeración windows Media Administrador de dispositivos
topic_type:
- apiref
api_name:
- WMDM_FIND_SCOPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb7d4902b1acd4223f25bdc5e8a7ca76d4495b5f465687a56b295ad2d5fbfa0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863015"
---
# <a name="wmdm_find_scope-enumeration"></a>Enumeración \_ FIND SCOPE de WMDM \_

El **tipo de \_ enumeración FIND SCOPE \_ de WMDM** define el ámbito del objeto de almacenamiento.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**ÁMBITO DE \_ BÚSQUEDA \_ GLOBAL DE \_ WMDM**
</dt> <dd>

Buscar el objeto correspondiente en cualquier lugar del dispositivo.

</dd> <dt>

<span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM \_ FIND \_ SCOPE \_ IMMEDIATE \_ CHILDREN**
</dt> <dd>

Buscar el objeto correspondiente dentro de este almacenamiento y sus secundarios.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





