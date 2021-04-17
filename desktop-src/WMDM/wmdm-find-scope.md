---
title: Enumeración WMDM_FIND_SCOPE
description: El \_ \_ tipo de enumeración de ámbito de búsqueda de WMDM define el ámbito del objeto de almacenamiento.
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- Enumeración WMDM_FIND_SCOPE Administrador de dispositivos de Windows Media
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
ms.openlocfilehash: 9d6b65489d14a4f1100b1da33238669310a2731f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698697"
---
# <a name="wmdm_find_scope-enumeration"></a>\_Enumeración de ámbito de búsqueda de WMDM \_

El tipo de enumeración de **\_ \_ ámbito de búsqueda de WMDM** define el ámbito del objeto de almacenamiento.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**\_ámbito de \_ búsqueda \_ global de WMDM**
</dt> <dd>

Buscar el objeto coincidente en cualquier parte del dispositivo.

</dd> <dt>

<span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**\_detectar \_ ámbito de \_ \_ elementos secundarios inmediatos de WMDM**
</dt> <dd>

Buscar el objeto coincidente dentro de este almacenamiento y sus elementos secundarios.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





