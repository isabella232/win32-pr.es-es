---
title: SystemMonitor. ReadOnly (propiedad)
description: Recupera o establece un valor que determina si un usuario puede modificar los valores de propiedad del control.
ms.assetid: 6ecfd63a-09b1-46eb-803f-6cb05bdecc25
keywords:
- Propiedad de solo lectura SysMon
- Propiedad de solo lectura SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad ReadOnly
topic_type:
- apiref
api_name:
- SystemMonitor.ReadOnly
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f42481e1bb0df0966f09ee354421af6378969f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996351"
---
# <a name="systemmonitorreadonly-property"></a>SystemMonitor. ReadOnly (propiedad)

Recupera o establece un valor que determina si un usuario puede modificar los valores de propiedad del control.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property ReadOnly As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True si no se desea que el usuario modifique los valores de propiedad del control; en caso contrario, false. El valor predeterminado es false, lo que significa que los usuarios pueden modificar los valores de propiedad del control.

## <a name="remarks"></a>Observaciones

Cuando el valor de esta propiedad es true, se aplican las siguientes condiciones:

-   El usuario no puede utilizar el menú contextual.
-   Los siguientes botones de la barra de herramientas están deshabilitados:
    -   Nuevo conjunto de contadores
    -   Ver la actividad actual
    -   Ver datos del archivo de registro
    -   Sumar
    -   Eliminar
    -   Pegar lista de contadores
    -   Propiedades

Tenga en cuenta que esta propiedad solo afecta a la capacidad del usuario de modificar los valores de propiedad a través de la interfaz de usuario, pero no le impide modificar mediante programación los valores o los contadores de propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





